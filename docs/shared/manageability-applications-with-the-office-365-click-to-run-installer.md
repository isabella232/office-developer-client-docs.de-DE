---
title: Integrieren von Verwaltbarkeitsanwendungen Microsoft 365 Apps Klick-und-Ausführen-Installationsprogramm
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Erfahren Sie, wie Sie Microsoft 365 Apps Klick-und-Ausführen-Installationsprogramm in eine Softwareverwaltungslösung integrieren.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297314"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Integrieren von Verwaltbarkeitsanwendungen Microsoft 365 Apps Klick-und-Ausführen-Installationsprogramm

Erfahren Sie, wie Sie Microsoft 365 Apps Klick-und-Ausführen-Installationsprogramm in eine Softwareverwaltungslösung integrieren.
  
Das Microsoft 365 Apps -Klick-und-Ausführen-Installationsprogramm bietet eine COM-Schnittstelle, die IT-Experten und Softwareverwaltungslösungen programmgesteuerte Kontrolle über die Updateverwaltung ermöglicht. Diese Schnittstelle bietet zusätzliche Verwaltungsfunktionen, die über die vom Bereitstellungstool bereitgestellten Office hinausgehen.
  
> [!NOTE]
> Dieser Artikel gilt für Office Apps, die das Click-to-Run-Installationsprogramm verwenden. 
  
## <a name="integrating-with-the-click-to-run"></a>Integration in das Klick-und-Ausführen

Um diese Schnittstelle zu verwenden, ruft eine Verwaltbarkeitsanwendung die COM-Schnittstelle auf und ruft verfügbar gemachte APIs auf, die direkt mit dem Click-to-Run-Installationsdienst kommunizieren. 
  
> [!NOTE]
> Das Office-Klick-und-Ausführen-Installationsprogramm kann über die Befehlszeile mit Parametern ausgeführt werden, die das Verhalten steuern können, wie in [Office Deployment Tool for Click-to-Run](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)dokumentiert. 
  
**Nachfolgend finden Sie ein konzeptionelles Diagramm der COM-Schnittstelle**

![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm der Verwendung der COM-Schnittstelle im Office -Klick-und-Ausführen-Installationsprogramm")
  
Das Microsoft 365 Apps -Klick-und-Ausführen-Installationsprogramm implementiert eine COM-basierte Schnittstelle, **IUpdateNotify** registriert bei CLSID **CLSID_UpdateNotifyObject**.
  
Diese Schnittstelle kann wie folgt aufgerufen werden:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

Der Aufruf ist nur erfolgreich, wenn der Anrufer mit erhöhten Rechten ausgeführt wird, da das Klick-und-Ausführen-Installationsprogramm mit erhöhten Rechten ausgeführt werden muss.
  
Die **IUpdateNotify** -COM-Schnittstelle macht drei asynchrone Funktionen verfügbar, die für die Validierung der Befehle und Parameter und die Planung der Ausführung mit dem Klick-und-Ausführen-Installationsdienst verantwortlich sind. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Eine vierte Methode, **Status**, kann verwendet werden, um Informationen über den Status des zuletzt ausgeführten Befehls oder den Status des aktuell ausgeführten Befehls (d. h. Erfolg, Fehler, detaillierte Fehlercodes) zu erhalten.
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Es gibt vier Zustände, in denen sich der Klick-und-Ausführen-Installationsdienst während seines Lebenszyklus befinden kann, während dessen **IUpdateNotify-Methoden** aufgerufen werden können. Neustart, Leerlauf, Herunterladen und Anwenden. 
  
**Im Folgenden finden Sie das Diagramm com Interface State Machine**

![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Ein Zustandsdiagramm für die COM-Schnittstelle")
  
> [!NOTE]
> **Neustart:** Wenn der Computer gestartet wird, gibt es einen Zeitraum, zu dem der Klick-und-Ausführen-Installationsprogrammdienst nicht verfügbar ist. Ein erfolgreicher Aufruf der Status-Methode nach einem Neustart gibt eUPDATE_UNKNOWN. 
  
**Leerlauf:** Wenn sich das Click-to-Run-Installationsprogramm im Leerlaufzustand befindet, können Sie dies aufrufen: 
  
- **Apply**: Installieren sie zuvor heruntergeladene Inhalte.
    
- **Cancel**: Gibt  `0x800000e` zurück , "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen."
    
- **Download**: Lädt neue Inhalte für die spätere Installation auf den Client herunter.
    
- **Status**: Gibt das Ergebnis der letzten abgeschlossenen Aktion oder eine Fehlermeldung zurück, wenn die Aktion zu einem Fehler endete. Wenn keine vorherige Aktion vorkommt, **gibt Status**  `eUPDATE_UNKNOWN` zurück.
    
**Herunterladen:** Wenn sich das Click-to-Run-Installationsprogramm im Downloadstatus befindet, können Sie: 
  
- **Apply**: Gibt ein **HRESULT mit** dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen" zurück.
    
- **Abbrechen**: Beendet den Download und entfernt die teilweise heruntergeladenen Inhalte.
    
- **Download**: Gibt ein **HRESULT mit** dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen" zurück. 
    
- **Status**: **Gibt** DOWNLOAD_WIP zurück, um anzugeben, dass Downloadarbeiten ausgeführt werden. 
    
**Anwenden:** Wenn das Click-to-Run-Installationsprogramm bereits Inhalte heruntergeladen hat: 
  
- **Apply**: Gibt ein **HRESULT mit** dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen" zurück.
    
- **Cancel**: Gibt  `0x800000e` zurück, die Aktion Anwenden kann nicht abgebrochen werden.
    
- **Download**: Gibt ein **HRESULT mit** dem Wert  `0x800000e` "Eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen" zurück. 
    
- **Status**: **Gibt** APPLY_WIP zurück, um anzugeben, dass die angewendete Arbeit ausgeführt wird. 
    
> [!NOTE]
> Da OfficeC2RCOM ein COM+-Dienst ist und dynamisch geladen wird, müssen Sie **CoCreateInstance** jedes Mal aufrufen, wenn Sie eine Methode für diese Klasse aufrufen, um sicherzustellen, dass Sie das erwartete Ergebnis erhalten. Der COM+-Dienst übert die Erstellung einer neuen Instanz, falls erforderlich. Wenn eine der Methoden zum ersten Mal aufgerufen wird, wird das **IUpdateNotify-Objekt** von COM+ geladen und in einer der dllhost.exe ausgeführt. Das neue Objekt bleibt ca. 3 Minuten im Leerlauf aktiv. Wenn innerhalb von drei Minuten nach dem letzten Aufruf ein nachfolgender Aufruf erfolgt, bleibt das **IUpdateNotify-Objekt** geladen, und eine neue Instanz wird nicht erstellt. Wenn innerhalb von drei Minuten kein Aufruf erfolgt, wird das IUpdateNotify-Objekt entladen, und beim nächsten Aufruf wird ein neues **IUpdateNotify-Objekt** erstellt. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Handbuch zur Com-API-Referenz für das Installationsprogramm mit Klick-und-Ausführen

In der folgenden API-Referenzdokumentation:
  
- Parameter befinden sich in einem Schlüssel-Wert-Paarformat, das durch ein Leerzeichen getrennt ist.
    
- Bei den Parametern wird die Zwischenschreibung nicht beachtet.
    
- Es ist eine [Liste der Parameter mit](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) Dokumentation verfügbar. 
    
- Die Zusammenfassung der IUpdateNotify2-Schnittstelle ist jetzt enthalten.
    
### <a name="apply"></a>Anwenden

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parameter

-  _displaylevel_: **true,** um den Installationsstatus, einschließlich Fehler, während des Updateprozesses zu zeigen; **false,** um den Installationsstatus, einschließlich Fehler, während des Updatevorgangs auszublenden. Der Standardwert ist **false**.
    
-  _forceappshutdown_: **true,** um zu erzwingen, Office Anwendungen sofort heruntergefahren werden, wenn die **Apply-Aktion** ausgelöst wird; **false,** um zu fehlschlagen, wenn Office anwendungen ausgeführt werden. Der Standardwert ist **false**. Weitere [Informationen finden Sie unter](#bk_ApplyRemark) Hinweise. 
    
  Wenn eine Office ausgeführt wird, wenn die **Apply-Aktion** ausgelöst wird, tritt bei der **Apply-Aktion** in der Regel ein Fehler auf. Wenn  `forceappshutdown=true` sie an die **Apply-Methode** übergeben werden, wird der **OfficeClickToRun-Dienst** die Anwendungen sofort herunterfahren und das Update anwenden. In diesem Fall kann es zu Datenverlusten für den Benutzer führen. 
    
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|||
|:-----|:-----|
|**S_OK** <br/> |Die Aktion wurde erfolgreich zur Ausführung an den Click-To-Run-Dienst übermittelt.  <br/> |
|**E_ACCESSDENIED** <br/> |Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.  <br/> |
|**E_INVALIDARG** <br/> |Ungültige Parameter wurden übergeben.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Aktion ist derzeit nicht zulässig. Weitere [Informationen finden Sie unter](#bk_ApplyRemark) Hinweise.  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Hinweise

- Wenn eine Office ausgeführt wird, wenn die **Apply-Aktion** ausgelöst wird, kann die **Apply-Aktion** nicht ausgeführt werden. Wenn Sie an die Apply-Methode übergeben, wird der `forceappshutdown=true` **OfficeClickToRun-Dienst** sofort alle Office heruntergefahren, die ausgeführt werden und das Update anwenden.  Dem Benutzer werden möglicherweise Daten angezeigt, da er nicht aufgefordert wird, Änderungen an geöffneten Dokumenten zu speichern. 
    
- Diese Aktion kann nur ausgelöst werden, wenn der COM-Status einer der folgenden Ist: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Wenn Sie die **Apply-Methode** aufrufen, ohne zuvor Inhalte herunterzuladen, wird von der **Apply-Methode** **erfolgreich** berichtet, da sie keine Anwendung erkannt hat und den **Apply-Prozess** erfolgreich abgeschlossen hat. 
    
### <a name="cancel"></a>Abbrechen

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|||
|:-----|:-----|
|S_OK  <br/> |Die Aktion wurde erfolgreich zur Ausführung an den Klick-und-Ausführen-Dienst übermittelt.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |Aktion ist derzeit nicht zulässig. Weitere Informationen [finden Sie](#bk_CancelRemarks) im Abschnitt "Hinweise".  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Hinweise

- Diese Methode kann nur ausgelöst werden, wenn die COM-Status-ID **eDOWNLOAD_WIP.** Es wird versucht, die aktuelle Downloadaktion abbricht. Der COM-Status wird in **eDOWNLOAD_CANCELLING** geändert und schließlich in **eDOWNLOAD_CANCELED**. Der COM-Status **gibt** E_ILLEGAL_METHOD_CALL, wenn es zu einem anderen Zeitpunkt ausgelöst wird. 
    
### <a name="download"></a>Herunterladen

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parameter

-  _displaylevel_: **true,** um den Installationsstatus, einschließlich Fehler, während des Updateprozesses zu zeigen; **false,** um den Installationsstatus, einschließlich Fehler, während des Updatevorgangs auszublenden. Der Standardwert ist **false**.
    
-  _updatebaseurl_: URL zur alternativen Downloadquelle.
    
-  _updatetoversion_: Die Version, auf die Office aktualisiert werden soll. Definieren Sie diesen Parameter, wenn Sie auf eine ältere Version aktualisieren möchten als die derzeit installierte Version.
    
-  _downloadsource_: CLSID der angepassten **IBackgroundCopyManager-Implementierung** (BITS-Manager). 
    
-  _contentid_: Identifiziert den Inhalt, der vom Inhaltsserver über den angepassten BITS-Manager heruntergeladen werden soll. Dieser Wert wird zur Interpretation über die BITS-Schnittstelle übergeben.
    
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|||
|:-----|:-----|
|**S_OK** <br/> |Die Aktion wurde erfolgreich zur Ausführung an den Click-To-Run-Dienst übermittelt.  <br/> |
|**E_ACCESSDENIED** <br/> |Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.  <br/> |
|**E_INVALIDARG** <br/> |Ungültige Parameter wurden übergeben.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Aktion ist derzeit nicht zulässig. Weitere [Informationen finden Sie unter](#bk_DownloadRemark) Hinweise.  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Hinweise

- Sie müssen  _downloadsource und_  _contentid als_ Paar angeben. Andern falls nicht, gibt die **Download-Methode** einen **fehler E_INVALIDARG** zurück. 
    
- Wenn  _downloadsource,_  _contentid_ und  _updatebaseurl_ bereitgestellt werden,  _wird updatebaseurl_ ignoriert. 
    
- Diese Aktion kann nur ausgelöst werden, wenn der COM-Status einer der folgenden Ist: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Wenn Sie die **Apply-Methode** ohne zuvor heruntergeladenen Inhalt aufrufen, wird von der **Apply-Methode** **Erfolgreich** berichtet, da sie keine anwendungsfingen erkannt hat und den **Apply-Prozess** erfolgreich abgeschlossen hat. 
    
#### <a name="examples"></a>Beispiele

- So laden Sie den Inhalt aus dem angepassten BITS-Manager herunter: Rufen Sie die **download()-Funktion** auf, die die folgenden Parameter übertritt: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- So laden Sie den Inhalt aus Office Content Delivery Network (CDN): Rufen Sie die **download()-Funktion** auf, ohne die Parameter _downloadsource,_ _contentid_ oder _updatebaseurl_ anzugeben. 
    
- So laden Sie den Inhalt von einem benutzerdefinierten Speicherort herunter: Rufen Sie die **Download()-Funktion** auf, die den folgenden Parameter übertritt: 
    
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

|||
|:-----|:-----|
| _pUpdateStatusReport_ <br/> |Zeiger auf eine UPDATE_STATUS_REPORT Struktur.  <br/> |
   
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|||
|:-----|:-----|
|**S_OK** <br/> |Die **Status-Methode** gibt immer dieses Ergebnis zurück. Überprüfen Sie die  `UPDATE_STATUS_RESULT` Struktur auf den Status der aktuellen Aktion.  <br/> |
   
#### <a name="remarks"></a>Hinweise

- Das Statusfeld von  `UPDATE_STATUS_REPORT` enthält den Status der aktuellen Aktion. Einer der folgenden Statuswerte wird zurückgegeben: 
    
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

- Wenn der letzte Befehl zu einem Fehler geführt hat, enthält das Fehlerfeld detaillierte  `UPDATE_STATUS_REPORT` Informationen zum Fehler. Von der Status-Methode werden zwei Typen von **Fehlercodes** zurückgegeben. 
    
- Wenn der Fehler kleiner als ist, ist der Fehler einer der folgenden  `UPDATE_ERROR_CODE::eUNKNOWN` vordefinierten Fehlercodes:
    
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

  Wenn der Rückgabefehlercode größer als der  `UPDATE_ERROR_CODE::eUNKNOWN` **HRESULT eines** fehlgeschlagenen Funktionsaufrufs ist. So extrahieren Sie das HRESULT-Subtrahieren aus dem wert, der  `UPDATE_ERROR_CODE::eUNKNOWN` im Fehlerfeld der zurückgegeben  `UPDATE_STATUS_REPORT` wird.
    
  Die vollständige Liste der Status- und Fehlerwerte kann durch Überprüfen der **IUpdateNotify-Typbibliothek** angezeigt werden, die in die OfficeC2RCom.dll. 
    
- Das Feld contentid wird für Aufrufe von **Status** verwendet, nachdem **Download** initiiert wurde, und gibt die contentid zurück, die an den **Downloadaufruf übergeben** wurde. Es ist eine bewährte Methode, dieses Feld auf **NULL zu initialisieren,** bevor Sie die **Status-Methode** aufrufen und dann den Wert überprüfen, nachdem **Status** zurückgegeben wurde. Wenn der Wert immer noch **null** ist, bedeutet dies, dass keine contentid zurückgegeben werden kann. Wenn der Wert nicht **null** ist, müssen Sie ihn mit einem Aufruf von **SysFreeString() frei machen.** Hier ist ein Codeausschnitt zum Aufrufen von **Status** nach **Download**.
    
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

Ab Version [16.0.8208.6352] wurde eine neue **IUpdateNotify2-Schnittstelle** hinzugefügt. 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Diese Schnittstelle hat auch die ursprüngliche IUpdateNotify-Schnittstelle gehostet, um abwärtskompatibel zu sein. Das heißt, wenn Sie diese Schnittstelle verwenden, haben Sie Zugriff auf alle Methoden, die in der **UpdateNotifyObject-Schnittstelle bereitgestellt** werden. 
    
- Neue Methoden, die IUpdateNotify2 hinzugefügt wurden:
    
  - **HRESULT** GetBlockingApps([out] BSTR \* AppsList). Holen Sie sich updates blocking apps list. Dieser Aufruf gibt die Ausführung Office zurück, die den Updatevorgang blockieren. 
    
  - **HRESULT** GetOfficeDeploymentData([in] int dataType, [in] **LPCWSTR** pcwszName, [out] BSTR * OfficeData). Get Office deployment Data. 
    
- Wenn Sie die neuen Methoden verwenden möchten, müssen Sie sicherstellen, dass:
    
  - Ihre #A0 ist neuer als der obige Build ( \> = Juni-Fork-Build).
    
  - Verwenden Sie UpdateNotifyObject2 anstelle von **UpdateNotifyObject,** um **CoCreateInstance auf aufruft.**
    
Wenn Sie keine der neuen Methoden verwenden, müssen Sie nichts ändern. Alle vorhandenen Methoden funktionieren genauso wie zuvor.
  
## <a name="implementing-the-bits-interface"></a>Implementieren der BITS-Schnittstelle

Die [Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) (BITS) ist ein Von Microsoft bereitgestellter Dienst zum Übertragen von Dateien zwischen einem Client und einem Server. BITS ist einer der Kanäle, die Office Click-To-Run-Installationsprogramm zum Herunterladen von Inhalten verwenden kann. Standardmäßig verwendet das Microsoft 365 Apps-Klick-und-Ausführen-Installationsprogramm die integrierte Windows-Implementierung von BITS, um den Inhalt aus dem CDN. 
  
Durch die Bereitstellung einer angepassten BITS-Implementierung für die **Download()-Methode** der **IUpdateNotify-Schnittstelle** kann Ihre Verwaltbarkeitssoftware steuern, wo und wie der Client die Inhalte herunterlädt. Eine angepasste BITS-Schnittstelle ist hilfreich, wenn sie einen anderen benutzerdefinierten Inhaltsverteilungskanal als die integrierten Klick-und-Ausführen-Kanäle, z. B. die CDN-, IIS-Server- oder Dateifreigaben, zur Verfügung stellt. 
  
Die Mindestanforderung für eine angepasste #A0 für die Office C2R-Dienst ist:
  
- Für **IBackgroundCopyManager**:
    
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

- Für **IBackgroundCopyJob**:
    
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

- Für **IBackgroundCopyJob3**:
    
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

  - cmbits ist hart codiert und steht für angepasste BITS.
    
  -  _\<contentid\>_ ist der _contentid-Parameter_ für die **Download()-Methode.** 
    
  -  _\<relative path to target file\>_ stellt den Speicherort und dateinamen der datei bereit, die heruntergeladen werden soll. 
    
    Wenn Sie z. B. eine _contentid_ der Download()-Methode bereitgestellt haben und Office C2R die Versions-Cab-Datei herunterladen möchte, z. B. Datei, wird `f732af58-5d86-4299-abe9-7595c35136ef`  `v32.cab` **AddFile()** mit folgendem Aufruf `RemoteUrl` angezeigt:
    
  ```cpp
  cmbits://f732af58-5d86-4299-abe9-7595c35136ef/Office/Data/V32.cab
  ```

- Für **IBackgroundCopyError**:
    
  ```cpp
  HRESULT _stdcall GetErrorDescription(
        [in]  DWORD  LanguageId,
        [out] LPWSTR *ppErrorDescription);
  
  ```

- Für **IBackgroundCopyFile**:
    
  ```cpp
  HRESULT _stdcall GetLocalName([out] LPWSTR *ppName); 
  HRESULT _stdcall GetRemoteName([out] LPWSTR *ppName);
  
  ```
## <a name="automating-content-staging"></a>Automatisieren der Inhaltsbereitstellung

IT-Administratoren können festlegen, dass Desktopclients automatisch Updates empfangen können, wenn sie direkt über die CDN verfügbar sind, oder sie können die Bereitstellung von Updates steuern, die über die Updatekanäle mit dem Office Deployment Tool oder Microsoft Endpoint Configuration Manager verfügbar sind.
  
Der Dienst unterstützt die Möglichkeit für Verwaltungstools, den Download der Inhalte zu erkennen und zu automatisieren, wenn Updates verfügbar gemacht werden.
  
**Die folgende Abbildung bietet eine Übersicht über das Herunterladen eines benutzerdefinierten Bilds**

![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm der Verwendung der COM-Schnittstelle im Office -Klick-und-Ausführen-Installationsprogramm")
  
### <a name="overview-of-downloading-a-custom-image"></a>Übersicht über das Herunterladen eines benutzerdefinierten Bilds
  
Im vorherigen Diagramm sehen Sie, dass ein Microsoft 365 Apps bild auf der CDN. Zusammen mit dem Microsoft 365 Apps steht eine API zur Verfügung, die über die erforderlichen Informationen verfügt, um verwaltbarkeitssoftware zu ermöglichen, benutzerdefinierte Bilder direkt zu erstellen, die die Notwendigkeit der Verwendung des Office-Bereitstellungstools ersetzen.

Ein Unternehmen konfiguriert seine WSUS so, dass die Microsoft 365 Apps werden. Diese Updates enthalten nicht die tatsächliche Bildnutzlast, lassen jedoch zu, dass die Verwaltbarkeitssoftware erkennt, wann neue Inhalte verfügbar sind. Die Verwaltbarkeitssoftware kann dann die Microsoft 365 Apps Updatemetadaten lesen, um zu verstehen, auf welche Version Office Update angewendet wird.

Wenn das Update anwendbar ist, kann die Verwaltbarkeitssoftware den CDN-Inhalt und die Dateiliste verwenden, um das benutzerdefinierte Image zu erstellen und es an dem Dateifreigabespeicherort zu speichern, für den es konfiguriert ist.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Verwenden der Microsoft 365 Apps-Dateilisten-API

Die Microsoft 365 Apps-Dateilisten-API wird verwendet, um die Namen der Dateien abzurufen, die für ein bestimmtes Update Microsoft 365 Apps werden.

HTTP-Anforderung

GET https://config.office.com/api/filelist

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

Optionale Abfrageparameter

|**Name**|**Beschreibung**|
|:-----|:-----|
| channel <br/>| Gibt den Kanalnamen an  <br/> Optional – Standardeinstellung "SemiAnnual" <br/> Unterstützte Werte https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| Version <br/>| Gibt die Updateversion an <br/> Optional – standardmäßig die neueste Version, die für den angegebenen Kanal verfügbar ist |
| arch <br/>| Gibt die Clientarchitektur an <br/> Optional – standardmäßig "x64" <br/> Unterstützte Werte: x64, x86 |
| lid <br/>| Gibt die zu verwendenden Sprachdateien an. <br/> Optional – Standardmäßig keine <br/> Um mehrere Sprachen anzugeben, fügen Sie einen Deckelabfrageparameter für jede Sprache ein. <br/> Verwenden Sie das Sprachbezeichnerformat ex. "en-us", "fr-fr" |
| alllanguages <br/>| Gibt an, dass alle Sprachdateien enthalten sind <br/> Optional – Standardmäßig false |

HTTP-Antwort

Wenn die Methode erfolgreich ist, werden der Antwortcode 200 OK und eine Auflistung von Dateiobjekten im Antworttext zurückgegeben.

Führen Sie die folgenden Schritte aus, um ein Bild zu erstellen:
1.  Rufen Sie die API auf, und geben Sie die entsprechenden Abfrageparameter für den Kanal, die Version und die Architektur des Updates an, an dem Sie interessiert sind.
Hinweis: File-Objekte mit dem Attribut "lcid": "0" sind sprachneutrale Dateien und müssen in das Bild eingeschlossen werden.
2.  Erstellen Sie ein lokales Bild des CDN, indem Sie die Dateiobjekte durch iterieren und die CDN-Dateien kopieren und gleichzeitig die Ordnerstruktur erstellen, wie durch das relativePath-Attribut angegeben, das für jedes der Dateiobjekte definiert ist.

Im folgenden Beispiel wird die Dateiliste für den aktuellen Kanal und version 16.0.4229.1004 für 64bit abgerufen und enthält die Dateien in französischer und englischer Sprache:

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Hashüberprüfung von #A0

Bilderstellungstools können die Integrität der heruntergeladenen .dat-Dateien überprüfen, indem ein berechneter Hashwert mit dem angegebenen Hashwert verglichen wird, der jeder #A0 zugeordnet ist. Es folgt ein Beispiel für ein Dateiobjekt, das hashLocation- und hashAlgorithm-Werte angibt:
  
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

- Das **hashLocation-Attribut** gibt den relativen Pfadspeicherort der .cab an, die den Hashwert enthält. Erstellen Sie den Speicherort der Hashdatei, indem Sie URL + relativePath + hashLocation verketten. Im folgenden Beispiel würde der speicherort stream.x64.bg-bg.hash sein: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- Das **hashAlgorithm-Attribut** gibt an, welcher Hashalgorithmus verwendet wurde. 
    
  Um die Integrität der datei stream.x64.bg-bg.dat zu überprüfen, öffnen Sie den stream.x64.bg-bg.hash, und lesen Sie den HASH-Wert, der die erste Textzeile in der Hashdatei ist. Vergleichen Sie dies mit dem berechneten Hashwert (mithilfe des angegebenen Hashalgorithmus), um die Integrität der heruntergeladenen #A0 zu überprüfen.
    
  Im folgenden Beispiel wird C# Code zum Lesen des Hashs gezeigt.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Microsoft 365 Apps Updates

Alle Microsoft 365 Apps werden im Microsoft [Update Catalog veröffentlicht.](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)
  
Microsoft 365 Apps Updates ermöglichen es der Verwaltbarkeitssoftware, Microsoft 365 Apps Updates auf eine Weise zu behandeln, die jedem anderen #A0 mit einer Ausnahme sehr ähnlich ist. Die Clientupdates enthalten keine tatsächliche Nutzlast. Die Microsoft 365 Apps Updates sollten nicht auf Clients installiert werden, sondern zum Auslösen der Workflows verwendet werden, indem die Verwaltbarkeitssoftware den Installationsbefehl durch den oben gezeigten COM-basierten Installationsmechanismus ersetzt.

**Die folgende Abbildung zeigt ein Diagramm des Office 365 Clientupdateworkflows.**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflowdiagramm für O365PP-Clientupdates")
  
Jedes Microsoft 365 Apps update, das veröffentlicht wird, enthält Metadaten zum Update. Diese Metadaten enthalten den Parameter MoreInfoUrl, der zum Ableitung des API-Aufrufs an die Dateilisten-API für dieses spezifische Update verwendet werden kann.

Im folgenden Beispiel wird die Dateilisten-API in die MoreInfoURL eingebettet und beginnt mit "ServicePath="

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath=https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Zusätzliche Metadaten für die Automatisierung der Inhaltsbereitstellung

**Veröffentlichungsverlaufs-API**
  
Die Microsoft 365 Apps Versionsverlaufs-API wird verwendet, um Details für jedes auf dem CDN veröffentlichte Update zusammen mit den Kanalnamen und anderen Kanalattributen abzurufen.

HTTP-Anforderung

```http
GET https://config.office.com/api/filelist/channels 
```

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

HTTP-Antwort

Wenn die Methode erfolgreich ist, werden der Antwortcode 200 OK und eine Auflistung von Dateiobjekten im Antworttext zurückgegeben.

**SKUs-API**
  
Die SKUs-API gibt Informationen zurück, die nützlich sind, um zu bestimmen, welche Produkte für die Bereitstellung und Wartung Office CDN verschiedenen Optionen für die einzelnen Produkte verfügbar sind.

HTTP-Anforderung

```http
GET https://config.office.com/api/filelist/skus 
```

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

HTTP-Antwort

Wenn die Methode erfolgreich ist, werden der Antwortcode 200 OK und eine Auflistung von Dateiobjekten im Antworttext zurückgegeben.
