---
title: Integrieren von Verwaltbarkeitsanwendungen in Microsoft 365 Apps Klick-und-Los-Installationsprogramm
manager: lindalu
ms.date: 09/14/2021
ms.audience: ITPro
ms.localizationpriority: medium
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Erfahren Sie, wie Sie das Microsoft 365 Apps Klick-und-Los-Installationsprogramm in eine Softwareverwaltungslösung integrieren.
ms.openlocfilehash: 65f601dc81562a6aad8f19546f22f9948117d1af
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59554978"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Integrieren von Verwaltbarkeitsanwendungen in Microsoft 365 Apps Klick-und-Los-Installationsprogramm

Erfahren Sie, wie Sie das Microsoft 365 Apps Klick-und-Los-Installationsprogramm in eine Softwareverwaltungslösung integrieren.
  
Das Microsoft 365 Apps Klick-und-Los-Installationsprogramm bietet eine COM-Schnittstelle, die IT-Experten und Softwareverwaltungslösungen programmgesteuerte Kontrolle über die Updateverwaltung ermöglicht. Diese Schnittstelle bietet zusätzliche Verwaltungsfunktionen, die über das Office-Bereitstellungstool hinausgehen.
  
> [!NOTE]
> Dieser Artikel bezieht sich auf Office Apps, die das Klick-und-Los-Installationsprogramm verwenden. 
  
## <a name="integrating-with-the-click-to-run"></a>Integration in Klick-und-Los

Um diese Schnittstelle zu verwenden, ruft eine Verwaltbarkeitsanwendung die COM-Schnittstelle auf und ruft die verfügbar gemachten APIs auf, die direkt mit dem Klick-und-Los-Installationsdienst kommunizieren. 
  
> [!NOTE]
> Das Office Klick-und-Los-Installationsprogramm kann über die Befehlszeile mit Parametern ausgeführt werden, die das Verhalten steuern können, wie in [Office Bereitstellungstool für Klick-und-Los](/DeployOffice/overview-office-deployment-tool.md)dokumentiert. 
  
**Es folgt ein konzeptionelles Diagramm der COM-Schnittstelle.**

![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramm der Verwendung der COM-Schnittstelle im Office Klick-und-Los-Installationsprogramm")
  
Das Microsoft 365 Apps Klick-und-Los-Installationsprogramm implementiert eine COM-basierte Schnittstelle, **IUpdateNotify,** die in CLSID **CLSID_UpdateNotifyObject** registriert ist.
  
Diese Schnittstelle kann wie folgt aufgerufen werden:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

Der Aufruf ist nur erfolgreich, wenn der Aufrufer unter erhöhten Rechten ausgeführt wird, da das Klick-und-Los-Installationsprogramm mit erhöhten Rechten ausgeführt werden muss.
  
Die **COM-Schnittstelle IUpdateNotify** macht drei asynchrone Funktionen verfügbar, die für die Überprüfung der Befehle und Parameter und die Planung der Ausführung mit dem Klick-und-Los-Installationsdienst verantwortlich sind. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Eine vierte Methode, **Status**, kann verwendet werden, um Informationen über den Status des zuletzt ausgeführten Befehls oder den Status des aktuell ausgeführten Befehls (z. B. Erfolg, Fehler, detaillierte Fehlercodes) abzurufen.
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Es gibt vier Zustände, in denen sich der Klick-und-Los-Installationsdienst während seines Lebenszyklus befindet, in dem **IUpdateNotify-Methoden** aufgerufen werden können. Neustart, Leerlauf, Herunterladen und Anwenden. 
  
**Im Folgenden ist das Com Interface State Machine-Diagramm dargestellt.**

![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Ein Zustandsdiagramm für die COM-Schnittstelle")
  
> [!NOTE]
> **Neustart:** Wenn der Computer gestartet wird, ist der Klick-und-Los-Installationsdienst nicht verfügbar. Ein erfolgreicher Aufruf der Status-Methode nach einem Neustart gibt eUPDATE_UNKNOWN zurück. 
  
**Leerlauf:** Wenn sich das Klick-und-Los-Installationsprogramm im Leerlaufzustand befindet, können Sie Folgendes aufrufen: 
  
- **Anwenden:** Installieren Sie zuvor heruntergeladene Inhalte.
    
- **Cancel**: Gibt  `0x800000e` zurück : "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen."
    
- **Download:** Lädt neue Inhalte zur späteren Installation auf den Client herunter.
    
- **Status:** Gibt das Ergebnis der letzten abgeschlossenen Aktion oder eine Fehlermeldung zurück, wenn die Aktion fehlgeschlagen ist. Wenn keine vorherige Aktion vorhanden ist, gibt **Status**  `eUPDATE_UNKNOWN` zurück.
    
**Herunterladen:** Wenn sich das Klick-und-Los-Installationsprogramm im Downloadstatus befindet, können Sie Folgendes aufrufen: 
  
- **Apply**: Gibt ein **HRESULT** mit dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen."
    
- **Abbrechen:** Beendet den Download und entfernt den teilweise heruntergeladenen Inhalt.
    
- **Download:** Gibt ein **HRESULT** mit dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen". 
    
- **Status:** Gibt **DOWNLOAD_WIP** zurück, um anzugeben, dass der Download ausgeführt wird. 
    
**Anwenden von:** Wenn das Klick-und-Los-Installationsprogramm bereits heruntergeladene Inhalte installiert: 
  
- **Apply**: Gibt ein **HRESULT** mit dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen."
    
- **Abbrechen:** Gibt  `0x800000e` zurück, dass die Apply-Aktion nicht abgebrochen werden kann.
    
- **Download:** Gibt ein **HRESULT** mit dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen". 
    
- **Status:** Gibt **APPLY_WIP** zurück, um anzugeben, dass die Anwendung ausgeführt wird. 
    
> [!NOTE]
> Da OfficeC2RCOM ein COM+-Dienst ist und dynamisch geladen wird, müssen Sie **CoCreateInstance** jedes Mal aufrufen, wenn Sie eine Methode für diese Klasse aufrufen, um sicherzustellen, dass Sie das erwartete Ergebnis erhalten. Der COM+-Dienst übernimmt bei Bedarf das Erstellen einer neuen Instanz. Wenn eine der Methoden zum ersten Mal aufgerufen wird, lädt COM+ das **IUpdateNotify-Objekt** und führt es in einer der dllhost.exe Instanzen aus. Das neue Objekt bleibt etwa 3 Minuten im Leerlauf aktiv. Wenn innerhalb von drei Minuten nach dem letzten Aufruf ein nachfolgender Aufruf erfolgt, bleibt das **IUpdateNotify-Objekt** geladen, und es wird keine neue Instanz erstellt. Wenn innerhalb von drei Minuten kein Aufruf erfolgt, wird das IUpdateNotify-Objekt entladen, und beim nächsten Aufruf wird ein neues **IUpdateNotify-Objekt** erstellt. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Referenzhandbuch zur COM-API für Klick-und-Los-Installationsprogramme

In der folgenden API-Referenzdokumentation:
  
- Parameter haben ein Schlüssel-Wert-Paarformat, das durch ein Leerzeichen getrennt ist.
    
- Bei den Parametern wird die Groß-/Kleinschreibung nicht beachtet.
    
- Weitere Informationen finden Sie unter [Informationen zu Office Klick-und-Los-Installationen und zu verwandten Antischadsoftware-Anwendungen.](/office/troubleshoot/office-suite-issues/office-click-to-run-installation.md)
    
- Die Zusammenfassung der IUpdateNotify2-Schnittstelle ist jetzt enthalten.
    
### <a name="apply"></a>Anwenden

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parameter

-  _Displaylevel:_ **"true",** um den Installationsstatus, einschließlich Fehlern, während des Updatevorgangs anzuzeigen; **false,** um den Installationsstatus, einschließlich Fehlern, während des Updateprozesses auszublenden. Der Standardwert ist **false**.
    
-  _forceappshutdown:_ **true,** um zu erzwingen, dass Office Anwendungen sofort heruntergefahren werden, wenn die **Apply-Aktion** ausgelöst wird; **"false",** wenn Office Anwendungen ausgeführt werden. Der Standardwert ist **false**. Weitere Informationen finden Sie [in den Anmerkungen.](#bk_ApplyRemark) 
    
  Wenn eine Office Anwendung ausgeführt wird, wenn **die** Apply-Aktion ausgelöst wird, schlägt die **Apply-Aktion** in der Regel fehl. Die Übergabe  `forceappshutdown=true` an die **Apply-Methode** bewirkt, dass der **OfficeClickToRun-Dienst** die Anwendungen sofort herunterfahren und das Update anwendet. In diesem Fall kann es zu Datenverlusten für den Benutzer führen. 
    
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|**Ergebnis**|**Beschreibung**|
|:-----|:-----|
|**S_OK** <br/> |Die Aktion wurde zur Ausführung erfolgreich an den Klick-und-Los-Dienst übermittelt.  <br/> |
|**E_ACCESSDENIED** <br/> |Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.  <br/> |
|**E_INVALIDARG** <br/> |Ungültige Parameter wurden übergeben.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Aktion ist derzeit nicht zulässig. Weitere Informationen finden Sie [in den Anmerkungen.](#bk_ApplyRemark)  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>HinwBemerkungeneise

- Wenn eine Office Anwendung ausgeführt wird, wenn **die** Apply-Aktion ausgelöst wird, schlägt die **Apply-Aktion** fehl. Wenn `forceappshutdown=true` Sie an die **Apply-Methode** übergeben, wird der **OfficeClickToRun-Dienst** alle Office Anwendungen, die ausgeführt werden, sofort heruntergefahren und das Update angewendet. Der Benutzer kann Daten anzeigen, da er nicht aufgefordert wird, Änderungen an geöffneten Dokumenten zu speichern. 
    
- Diese Aktion kann nur ausgelöst werden, wenn der COM-Status einer der folgenden Ist: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Wenn Sie die **Apply-Methode aufrufen,** ohne zuvor Inhalte heruntergeladen zu haben, meldet die **Apply-Methode** **"Erfolgreich",** da sie nichts gefunden hat, um den **Apply-Prozess** erfolgreich anzuwenden und abzuschließen. 
    
### <a name="cancel"></a>Abbrechen

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|**Ergebnis**|**Description**|
|:-----|:-----|
|S_OK  <br/> |Die Aktion wurde zur Ausführung erfolgreich an den Klick-und-Los-Dienst übermittelt.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |Aktion ist derzeit nicht zulässig. Weitere Informationen finden Sie im Abschnitt ["Hinweise"](#bk_CancelRemarks)  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>HinwBemerkungeneise

- Diese Methode kann nur ausgelöst werden, wenn die COM-Status-ID **eDOWNLOAD_WIP.** Es wird versucht, die aktuelle Downloadaktion abzubrechen. Der COM-Status wird in **eDOWNLOAD_CANCELLING** und schließlich in **eDOWNLOAD_CANCELED** geändert. Der COM-Status gibt **E_ILLEGAL_METHOD_CALL** zurück, wenn er zu einem anderen Zeitpunkt ausgelöst wird. 
    
### <a name="download"></a>Herunterladen

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parameter

-  _Displaylevel:_ **"true",** um den Installationsstatus, einschließlich Fehlern, während des Updatevorgangs anzuzeigen; **false,** um den Installationsstatus, einschließlich Fehlern, während des Updateprozesses auszublenden. Der Standardwert ist **false**.
    
-  _updatebaseurl:_ URL zur alternativen Downloadquelle.
    
-  _updatetoversion:_ Die Version, auf die Office aktualisiert werden soll. Definieren Sie diesen Parameter, wenn Sie auf eine ältere Version als die aktuell installierte Version aktualisieren möchten.
    
-  _downloadsource_: CLSID der angepassten **IBackgroundCopyManager-Implementierung** (BITS-Manager). 
    
-  _contentid:_ Identifiziert den Inhalt, der über den angepassten BITS-Manager vom Inhaltsserver heruntergeladen werden soll. Dieser Wert wird zur Interpretation über die BITS-Schnittstelle übergeben.
    
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|**Ergebnis**|**Beschreibung**|
|:-----|:-----|
|**S_OK** <br/> |Die Aktion wurde zur Ausführung erfolgreich an den Klick-und-Los-Dienst übermittelt.  <br/> |
|**E_ACCESSDENIED** <br/> |Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.  <br/> |
|**E_INVALIDARG** <br/> |Ungültige Parameter wurden übergeben.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Aktion ist derzeit nicht zulässig. Weitere Informationen finden Sie [in den Anmerkungen.](#bk_DownloadRemark)  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>HinwBemerkungeneise

- Sie müssen  _downloadsource_ und  _contentid_ als Paar angeben. Wenn nicht, gibt die **Downloadmethode** einen **E_INVALIDARG** Fehler zurück. 
    
- Wenn  _downloadsource,_  _contentid_ und  _updatebaseurl_ bereitgestellt werden, wird  _updatebaseurl_ ignoriert. 
    
- Diese Aktion kann nur ausgelöst werden, wenn der COM-Status einer der folgenden Ist: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Wenn Sie die **Apply-Methode** ohne zuvor heruntergeladenen Inhalt aufrufen, meldet die **Apply-Methode** **"Erfolgreich",** da sie nichts gefunden hat, um den **Apply-Prozess** erfolgreich anzuwenden und abzuschließen. 
    
#### <a name="examples"></a>Beispiele

- So laden Sie den Inhalt aus dem angepassten BITS-Manager herunter: Rufen Sie die **download()-Funktion** auf, indem Sie die folgenden Parameter übergeben: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Um den Inhalt aus dem Office Content Delivery Network (CDN) herunterzuladen, rufen Sie die **download()-Funktion** auf, ohne die _Parameter downloadsource,_ _contentid_ oder _updatebaseurl_ anzugeben. 
    
- So laden Sie den Inhalt von einem angepassten Speicherort herunter: Rufen Sie die **download()-Funktion** auf, indem Sie den folgenden Parameter übergeben: 
    
  ```cpp
  "updatebaseurl=yourcontentserverurl"
  ```

### <a name="status"></a>Status

```cpp
typdef struct _UPDATE_STATUS_REPORT
{
    UPDATE_STATUS status;
    UINT error;
    LPCWSTR contentid;
}UPDATE_STATUS_REPORT;
HRESULT status([out] _UPDATE_STATUS_REPORT& pUpdateStatusReport) // Get status of current action
```

#### <a name="parameters"></a>Parameter

|**Parameter**|**Beschreibung**|
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Zeiger auf eine UPDATE_STATUS_REPORT Struktur.  <br/> |
   
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|**Ergebnis**|**Beschreibung**|
|:-----|:-----|
|**S_OK** <br/> |Die **Status-Methode** gibt immer dieses Ergebnis zurück. Überprüfen Sie die  `UPDATE_STATUS_RESULT` Struktur auf den Status der aktuellen Aktion.  <br/> |
   
#### <a name="remarks"></a>HinwBemerkungeneise

- Das Statusfeld des  `UPDATE_STATUS_REPORT` Felds enthält den Status der aktuellen Aktion. Einer der folgenden Statuswerte wird zurückgegeben: 
    
  ```cpp
  typedef enum _UPDATE_STATUS
  {
  eUPDATE_UNKNOWN = 0,
  eDOWNLOAD_PENDING,
  eDOWNLOAD_WIP,
  eDOWNLOAD_CANCELLING,
  eDOWNLOAD_CANCELLED,
  eDOWNLOAD_FAILED,
  eDOWNLOAD_SUCCEEDED,
  eAPPLY_PENDING,
  eAPPLY_WIP,
  eAPPLY_SUCCEEDED,
  eAPPLY_FAILED,
  } UPDATE_STATUS;
  
  ```

- Wenn der letzte Befehl zu einem Fehler geführt hat, enthält das Fehlerfeld des Befehls  `UPDATE_STATUS_REPORT` detaillierte Informationen zu dem Fehler. Von der **Status-Methode** werden zwei Arten von Fehlercodes zurückgegeben. 
    
- Wenn der Fehler kleiner als  `UPDATE_ERROR_CODE::eUNKNOWN` ist, ist der Fehler einer der folgenden vordefinierten Fehlercodes:
    
  ```cpp
  typedef enum _UPDATE_ERROR_CODE
  {
  eOK = 0,
  eFAILED_UNEXPECTED,
  eTRIGGER_DISABLED,
  ePIPELINE_IN_USE,
  eFAILED_STOP_C2RSERVICE,
  eFAILED_GET_CLIENTUPDATEFOLDER,
  eFAILED_LOCK_PACKAGE_TO_UPDATE,
  eFAILED_CREATE_STREAM_SESSION,
  eFAILED_PUBLISH_WORKING_CONFIGURATION,
  eFAILED_DOWNLOAD_UPGRADE_PACKAGE,
  eFAILED_APPLY_UPGRADE_PACKAGE,
  eFAILED_INITIALIZE_RSOD,
  eFAILED_PUBLISH_RSOD,
  // Keep this one as the last
  eUNKNOWN
  } UPDATE_ERROR_CODE;
  
  ```

  Wenn der Rückgabefehlercode größer ist als  `UPDATE_ERROR_CODE::eUNKNOWN` der **HRESULT-Wert** eines fehlgeschlagenen Funktionsaufrufs. So extrahieren Sie den HRESULT-Subtrahieren  `UPDATE_ERROR_CODE::eUNKNOWN` aus dem Wert, der im Fehlerfeld der  `UPDATE_STATUS_REPORT` zurückgegeben wird.
    
  Die vollständige Liste der Status- und Fehlerwerte kann angezeigt werden, indem die in OfficeC2RCom.dll eingebettete **IUpdateNotify-Typbibliothek** überprüft wird. 
    
- Das Inhalts-ID-Feld wird für **Aufrufe** von Status verwendet, nachdem **der Download** initiiert wurde, und gibt die Inhalts-ID zurück, die an den **Download-Aufruf** übergeben wurde. Es empfiehlt sich, dieses Feld auf **NULL** zu initialisieren, bevor Sie die **Status-Methode** aufrufen und dann den Wert überprüfen, nachdem **Status** zurückgegeben wurde. Wenn der Wert immer noch **NULL** ist, bedeutet dies, dass keine Inhalts-ID zurückgegeben werden muss. Wenn der Wert nicht **NULL** ist, müssen Sie ihn mit einem Aufruf von **SysFreeString()** freigeben. Nachfolgend finden Sie einen Codeausschnitt zum Aufrufen von **Status** nach **dem Download.**
    
  ```cpp
  std::wstring contentID;
  UPDATE_STATUS_REPORT statusReport;
  statusReport.status = eUPDATE_UNKNOWN;
  statusReport.error = eOK;
  statusReport.contentid = NULL;
  hr = p->Status(&statusReport);
  if (statusReport.contentid != NULL)
  {
  contentID = statusReport.contentid;
  SysFreeString(statusReport.contentid);
  }
  wprintf(L"ContentID: %s, Status: %d, LastError: %d", contentID.c_str(), statusReport.status, statusReport.error);
  
  ```

### <a name="summary-of-iupdatenotify2-interface"></a>Zusammenfassung der IUpdateNotify2-Schnittstelle

Ab Version [16.0.8208.6352] haben wir eine neue **IUpdateNotify2-Schnittstelle** hinzugefügt. 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Diese Schnittstelle gehostet auch die ursprüngliche IUpdateNotify-Schnittstelle, um Abwärtskompatibilität bereitzustellen. Das heißt, wenn Sie diese Schnittstelle verwenden, haben Sie Zugriff auf alle Methoden, die in der **UpdateNotifyObject-Schnittstelle** bereitgestellt werden. 
    
- Neue Methoden, die zu IUpdateNotify2 hinzugefügt wurden:
    
  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList). Dient zum Abrufen der Liste der Updates, die Apps blockieren. Dieser Aufruf gibt die Ausführung Office Apps zurück, die verhindern, dass der Updatevorgang fortgesetzt wird. 
    
  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Rufen Sie Office Bereitstellungsdaten ab. 
    
- Wenn Sie die neuen Methoden verwenden möchten, müssen Sie Folgendes sicherstellen:
    
  - Ihre C2R-Version ist neuer als der obige Build ( \> = Verzweigungsbuild vom Juni).
    
  - Verwenden Sie UpdateNotifyObject2 anstelle von **UpdateNotifyObject,** um **CoCreateInstance** aufzurufen.
    
Wenn Sie keine der neuen Methoden verwenden, müssen Sie nichts ändern. Alle vorhandenen Methoden funktionieren genau wie zuvor.
  
## <a name="implementing-the-bits-interface"></a>Implementieren der BITS-Schnittstelle

Der [intelligente Hintergrundübertragungsdienst (Background Intelligent Transfer Service,](/windows/win32/bits/background-intelligent-transfer-service-portal.md) BITS) ist ein Dienst, der von Microsoft bereitgestellt wird, um Dateien zwischen einem Client und einem Server zu übertragen. BITS ist einer der Kanäle, die Office Klick-und-Los-Installationsprogramm zum Herunterladen von Inhalten verwenden kann. Standardmäßig verwendet das Microsoft 365 Apps Klick-und-Los-Installationsprogramm die integrierte Bits-Implementierung des Windows, um den Inhalt aus dem CDN herunterzuladen. 
  
Durch die Bereitstellung einer benutzerdefinierten BITS-Implementierung für die **Download()-Methode** der **IUpdateNotify-Schnittstelle** kann Ihre Verwaltbarkeitssoftware steuern, wo und wie der Client den Inhalt herunterlädt. Eine angepasste BITS-Schnittstelle ist nützlich, wenn Sie einen benutzerdefinierten Inhaltsverteilungskanal bereitstellen, der nicht den integrierten Klick-und-Los-Kanälen entspricht, z. B. die CDN, IIS-Server oder Dateifreigaben. 
  
Die Mindestanforderung für eine angepasste BITS-Schnittstelle für die Arbeit mit Office C2R-Dienst ist:
  
- Für **IBackgroundCopyManager:**
    
  ```cpp
  HRESULT _stdcall CreateJob(
                      [in] LPWSTR DisplayName, 
                      [in] BG_JOB_TYPE Type, 
                      [out] GUID* pJobId, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall GetJob(
                      [in] GUID* jobID, 
                      [out] IBackgroundCopyJob** ppJob)
  HRESULT _stdcall EnumJobs(
                      [in] unsigned long dwFlags, 
                      [out] IEnumBackgroundCopyJobs** ppenum)
  
  ```

- Für **IBackgroundCopyJob:**
    
  ```cpp
  HRESULT _stdcall AddFile(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName)
  HRESULT _stdcall Resume()
  HRESULT _stdcall Complete()
  HRESULT _stdcall Cancel();
  HRESULT _stdcall GetState([out] BG_JOB_STATE* pVal);
  HRESULT GetProgress( [out] BG_JOB_PROGRESS *pProgress);
  
  ```

- Für **IBackgroundCopyJob3:**
    
  ```cpp
  HRESULT _stdcall AddFileWithRanges(
                      [in] LPWSTR RemoteUrl, 
                      [in] LPWSTR LocalName,
                      [in] DWORD RangeCount,
                      [in] BG_FILE_RANGE Ranges[])
  
  ```

- Für die  `Addfile`  `AddFileWithRanges` Und-Funktionen hat die Remote-URL das folgende Format: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - Cmbits ist hartcodiert und steht für benutzerdefinierte BITS.
    
  -  _\<contentid\>_ ist der _contentid-Parameter_ für die **Download()-Methode.** 
    
  -  _\<relative path to target file\>_ stellt den Speicherort und den Dateinamen der herunterzuladenden Datei bereit. 
    
    Wenn Sie beispielsweise eine _Inhalts-ID_ `f732af58-5d86-4299-abe9-7595c35136ef` der **Download()-Methode** bereitgestellt haben und Office C2R die Cab-Versionsdatei herunterladen möchte, z. B. `v32.cab` datei, wird **AddFile()** mit folgendem Code `RemoteUrl` aufgerufen:
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- Für **IBackgroundCopyError:**
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- Für **IBackgroundCopyFile:**
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a>Automatisieren der Inhaltsbereitstellung

IT-Administratoren können auswählen, ob Desktopclients für den automatischen Empfang von Updates aktiviert sind, wenn sie direkt im CDN verfügbar sind, oder sie können die Bereitstellung von Updates, die über die Updatekanäle verfügbar sind, mithilfe des Office-Bereitstellungstools oder Microsoft Endpoint Configuration Manager steuern.
  
Der Dienst unterstützt die Möglichkeit für Verwaltungstools, den Download der Inhalte zu erkennen und zu automatisieren, wenn Updates zur Verfügung gestellt werden.
  
**Die folgende Abbildung enthält eine Übersicht über das Herunterladen eines benutzerdefinierten Bilds.**

![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Diagramm der Verwendung der COM-Schnittstelle im Office Klick-und-Los-Installationsprogramm")
  
### <a name="overview-of-downloading-a-custom-image"></a>Übersicht über das Herunterladen eines benutzerdefinierten Bilds
  
Im vorherigen Diagramm sehen Sie, dass ein neues Microsoft 365 Apps Bild auf dem CDN verfügbar ist. Zusammen mit dem Microsoft 365 Apps Image ist eine API verfügbar, die über die erforderlichen Informationen verfügt, damit Die Verwaltbarkeitssoftware direkt angepasste Images erstellen kann, die die Notwendigkeit der Verwendung des Office-Bereitstellungstools ersetzen.

Ein Unternehmen konfiguriert seine WSUS so, dass die Microsoft 365 Apps Updates synchronisiert werden. Diese Updates enthalten nicht die tatsächliche Imagenutzlast, aber die Verwaltbarkeitssoftware erkennt, wann neue Inhalte verfügbar sind. Die Verwaltbarkeitssoftware kann dann die Microsoft 365 Apps Updatemetadaten lesen, um zu verstehen, für welche Version von Office das Update gilt.

Wenn das Update anwendbar ist, kann die Verwaltbarkeitssoftware den CDN Inhalt und die Dateiliste verwenden, um das benutzerdefinierte Bild zu erstellen und im Speicherort der Dateifreigabe zu speichern, für die es konfiguriert ist.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Verwenden der Microsoft 365 Apps-Dateilisten-API

Die Microsoft 365 Apps Dateilisten-API wird verwendet, um die Namen der Dateien abzurufen, die für ein bestimmtes Microsoft 365 Apps Update erforderlich sind.

HTTP-Anforderung

GET https://config.office.com/api/filelist

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

Optionale Abfrageparameter

|**Name**|**Beschreibung**|
|:-----|:-----|
| Kanal <br/>| Gibt den Kanalnamen an.  <br/> Optional – Standardeinstellung ist "SemiAnnual" <br/> Unterstützte Werte https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| Version <br/>| Gibt die Updateversion an. <br/> Optional – standardmäßig die neueste Version, die für den angegebenen Kanal verfügbar ist |
| Arch <br/>| Gibt die Clientarchitektur an <br/> Optional – standardmäßig "x64" <br/> Unterstützte Werte: x64, x86 |
| lid <br/>| Gibt die einzuschließenden Sprachdateien an. <br/> Optional – standardmäßig keine <br/> Um mehrere Sprachen anzugeben, fügen Sie einen Deckel-Abfrageparameter für jede Sprache ein <br/> Verwenden Sie das Sprachenbezeichnerformat, z. B. 'en-us', 'fr-fr' |
| alllanguages <br/>| Gibt an, dass alle Sprachdateien eingeschlossen werden sollen. <br/> Optional – standardwertt auf "false" |

**HTTP-Antwort**

Bei erfolgreicher Ausführung gibt die Methode den Antwortcode 200 OK und eine Sammlung von Dateiobjekten im Antworttext zurück.

Führen Sie die folgenden Schritte aus, um ein Bild zu erstellen:
1.  Rufen Sie die API auf, und stellen Sie die entsprechenden Abfrageparameter für den Kanal, die Version und die Architektur des Updates bereit, an dem Sie interessiert sind.
Hinweis: Dateiobjekte mit dem Attribut "lcid": "0" sind sprachneutrale Dateien und müssen in das Bild eingeschlossen werden.
2.  Erstellen Sie ein lokales Bild des CDN, indem Sie die Dateiobjekte durchlaufen und die CDN Dateien kopieren, während Sie die Ordnerstruktur gemäß dem für jedes Dateiobjekt definierten Attribut "relativePath" erstellen.

Im folgenden Beispiel wird die Dateiliste für den aktuellen Kanal und version 16.0.4229.1004 für 64bit abgerufen und enthält die Französisch- und Englisch-Sprachdateien.

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Hashüberprüfung von DAT-Dateien

Bilderstellungstools können die Integrität der heruntergeladenen DAT-Dateien überprüfen, indem sie einen berechneten Hashwert mit dem angegebenen Hashwert vergleichen, der jeder DAT-Datei zugeordnet ist. Es folgt ein Beispiel für ein Dateiobjekt, das hashLocation- und hashAlgorithm-Werte angibt:
  
```xml
{
  "url": "https://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114/office/data/16.0.1234.1001/stream.x64.x-none.dat",
  "name": "stream.x64.x-none.dat",
  "relativePath": "/office/data/16.0.1234.1001/",
  "hashLocation": "s640.cab/stream.x64.x-none.hash",
  "hashAlgorithm": "Sha256",
  "lcid": "0"
},
```

- Das **hashLocation-Attribut** gibt den relativen Pfadspeicherort .cab Datei an, die den Hashwert enthält. Erstellen Sie den Speicherort der Hashdatei, indem Sie URL + relativePath + hashLocation verketten. Im folgenden Beispiel würde der Speicherort "stream.x64.bg-bg.hash" wie folgt aussehen: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- Das **HashAlgorithm-Attribut** gibt an, welcher Hashalgorithmus verwendet wurde. 
    
  Um die Integrität der Datei stream.x64.bg-bg.dat zu überprüfen, öffnen Sie die Datei stream.x64.bg-bg.hash, und lesen Sie den HASH-Wert, der die erste Textzeile in der Hashdatei ist. Vergleichen Sie dies mit dem berechneten Hashwert (unter Verwendung des angegebenen Hashalgorithmus), um die Integrität der heruntergeladenen DAT-Datei zu überprüfen.
    
  Das folgende Beispiel zeigt den C#-Code zum Lesen des Hashs.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Microsoft 365 Apps Updates

Alle Microsoft 365 Apps Updates werden im [Microsoft Update-Katalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)veröffentlicht.
  
Microsoft 365 Apps Updates ermöglichen die Verwaltung von Software, um Microsoft 365 Apps Updates auf eine Weise zu behandeln, die einem anderen WU-Update mit einer Ausnahme sehr ähnlich ist. Die Clientupdates enthalten keine tatsächliche Nutzlast. Die Microsoft 365 Apps Updates sollten nicht auf Clients installiert werden, sondern zum Auslösen der Workflows mit der Verwaltbarkeitssoftware verwendet werden, die den Installationsbefehl durch den oben gezeigten COM-basierten Installationsmechanismus ersetzt.

**Die folgende Abbildung zeigt ein Diagramm des Office 365 Clientupdate-Workflows.**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflowdiagramm für O365PP-Clientupdates")
  
Jedes veröffentlichte Microsoft 365 Apps Update enthält Metadaten zu dem Update. Diese Metadaten enthalten einen Parameter namens MoreInfoUrl, der verwendet werden kann, um den API-Aufruf der Dateilisten-API für dieses spezifische Update abzuleiten.

Im folgenden Beispiel ist die Dateilisten-API in die MoreInfoURL eingebettet und beginnt mit "ServicePath=".

https://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Zusätzliche Metadaten für die Automatisierung der Inhaltsbereitstellung

**Versionsverlaufs-API**
  
Die Microsoft 365 Apps-Versionsverlaufs-API wird verwendet, um Details zu den einzelnen Updates abzurufen, die im CDN veröffentlicht wurden, zusammen mit den Kanalnamen und anderen Kanalattributen.

HTTP-Anforderung

```http
GET https://config.office.com/api/filelist/channels 
```

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

HTTP-Antwort

Bei erfolgreicher Ausführung gibt die Methode den Antwortcode 200 OK und eine Sammlung von Dateiobjekten im Antworttext zurück.

**SKUs-API**
  
Die SKUs-API gibt Informationen zurück, die nützlich sind, um zu bestimmen, welche Produkte für die Bereitstellung und Wartung über die Office CDN verfügbar sind, sowie verschiedene Optionen für die einzelnen.

HTTP-Anforderung

```http
GET https://config.office.com/api/filelist/skus 
```

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

HTTP-Antwort

Bei erfolgreicher Ausführung gibt die Methode den Antwortcode 200 OK und eine Sammlung von Dateiobjekten im Antworttext zurück.
