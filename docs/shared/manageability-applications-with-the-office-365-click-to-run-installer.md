---
title: Integrieren von Office 365 Klick-und-Los-Installer Verwaltbarkeit Applikationen
manager: kelbow
ms.date: 10/22/2017
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: Erfahren Sie, wie das Installationsprogramm von Office 365 Klick-und-Los in eine Software Management-Lösung zu integrieren.
ms.openlocfilehash: abe941e3e3818eed1f18108f1678e46e8156b08c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796320"
---
# <a name="integrating-manageability-applications-with-office-365-click-to-run-installer"></a>Integrieren von Office 365 Klick-und-Los-Installer Verwaltbarkeit Applikationen

Erfahren Sie, wie das Installationsprogramm von Office 365 Klick-und-Los in eine Software Management-Lösung zu integrieren.
  
Der Office 365 Klick-und-Los-Installer bietet eine COM-Schnittstelle, die IT-Spezialisten und Software-Management-Lösungen programmgesteuerte Kontrolle über die Verwaltung von ermöglicht. Diese Schnittstelle bietet zusätzliche Verwaltungsfunktionen außerhalb von Office-Bereitstellungstool bereitgestellt werden.
  
> [!NOTE]
> Dieser Artikel bezieht sich auf Office 2016 und höher, Office 365. 
  
## <a name="integrating-with-the-click-to-run"></a>Integrieren von Klick-und-los

Wenn diese Schnittstelle verwenden möchten, eine Verwaltbarkeit-Anwendung die COM-Schnittstelle aufgerufen, und Aufrufe verfügbar gemacht, APIs, die direkt mit der Klick-und-Los-Installationsdienst kommunizieren. 
  
> [!NOTE]
> Das Installationsprogramm von Office Klick-und-Los kann über die Befehlszeile aufgerufen mit Parametern, die das Verhalten steuern können ausgeführt werden, wie in der [Office-Bereitstellungstool für Klick-und-Los](https://www.microsoft.com/en-us/download/details.aspx?id=49117)dokumentiert. 
  
**Nachfolgend sehen Sie ein konzeptionelles Diagramm der COM-Schnittstelle**

![Ein Diagramm der Verwendung der COM-Schnittstelle auf das Installationsprogramm von Office Klick-und-los.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm der Verwendung der COM-Schnittstelle auf die Office Klick-und-Los-installer")
  
Die Office 365-Klick-und-Los-Installer implementiert, die ein COM-basiertes Schnittstelle **IUpdateNotify** registriert für CLSID **CLSID_UpdateNotifyObject**.
  
Diese Schnittstelle kann wie folgt aufgerufen werden:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

Der Anruf nur erfolgreich, wenn der Aufrufer unter erhöhten Berechtigungen ausgeführt wird wie das Klick-und-Los-Installationsprogramm mit erhöhten Rechten ausgeführt werden muss.
  
Die **IUpdateNotify** COM-Schnittstelle werden drei asynchrone Funktionen verantwortlich für die Überprüfung der Befehle und Parameter und planen die Ausführung mit der Klick-und-Los-Installationsdienst verfügbar gemacht. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Eine Methode, **Status**, kann vorwärts zum Abrufen von Informationen über den Status des letzten ausgeführten Befehl oder den Status der derzeit ausgeführten Befehl (d. h. Erfolg, Fehler, detaillierten Fehlercodes) verwendet werden.
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Es gibt vier Zustände, die die Klick-und-Los-Installationsdienst in während ihres Lebenszyklus möglicherweise während der möglicherweise **IUpdateNotify** Methoden aufgerufen werden. Neustart Leerlauf, herunterladen und anwenden. 
  
**Nachfolgend sehen Sie das COM-Schnittstelle Zustandsautomat-Diagramm**

![Ein Zustandsdiagramm für die COM-Schnittstelle.] (media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Ein Zustandsdiagramm für die COM-Schnittstelle")
  
> [!NOTE]
> **Rebooting**: beim Starten des Computers ist eine bestimmte Zeitspanne bei der Klick-und-Los-Installer-Dienst nicht verfügbar ist ist. Ein erfolgreicher Aufruf an die Status-Methode nach einem Neustart wird eUPDATE_UNKNOWN zurückgegeben. 
  
**Im Leerlauf:** Wenn das Klick-und-Los-Installationsprogramm im Leerlauf ist, können Sie aufrufen: 
  
- **Übernehmen**: Install zuvor Inhalte heruntergeladen.
    
- **Abbrechen**: Gibt `0x800000e`, "wurde eine Methode aufgerufen zu einem unerwarteten Zeitpunkt."
    
- **Herunterladen**: neuen Inhalte an den Client für spätere Installation Downloads.
    
- **Status**: Gibt das Ergebnis der letzten abgeschlossenen Aktion oder eine Fehlermeldung zurück, wenn die Aktion Fehler beendet. Wenn keine vorherige Aktion vorhanden ist, gibt **Status** `eUPDATE_UNKNOWN`.
    
**Herunterladen:** Wenn das Klick-und-Los-Installationsprogramm im Download Zustand befindet, können Sie aufrufen: 
  
- **Übernehmen**: Gibt ein **HRESULT** mit dem Wert `0x800000e`, "wurde eine Methode aufgerufen zu einem unerwarteten Zeitpunkt."
    
- **Abbrechen**: stoppt das Herunterladen und die teilweise heruntergeladene Inhalte entfernt.
    
- **Herunterladen**: Gibt ein **HRESULT** mit dem Wert `0x800000e`, "wurde eine Methode aufgerufen zu einem unerwarteten Zeitpunkt." 
    
- **Status**: Gibt **DOWNLOAD_WIP** , um anzugeben, dass der Download Arbeit ausgeführt wird. 
    
**Anwenden:** Wenn der Klick-und-Los-Installer ist während der Installation zuvor Download von Inhalten: 
  
- **Übernehmen**: Gibt ein **HRESULT** mit dem Wert `0x800000e`, "wurde eine Methode aufgerufen zu einem unerwarteten Zeitpunkt."
    
- **Abbrechen**: Gibt `0x800000e`, die Apply-Aktion kann nicht abgebrochen werden.
    
- **Herunterladen**: Gibt ein **HRESULT** mit dem Wert `0x800000e`, "wurde eine Methode aufgerufen zu einem unerwarteten Zeitpunkt." 
    
- **Status**: Gibt **APPLY_WIP** , um anzugeben, die Arbeit gelten wird gerade durchgeführt. 
    
> [!NOTE]
> Da OfficeC2RCOM ein COM-+-Dienst ist und dynamisch geladen wird, müssen Sie **CoCreateInstance** aufrufen, jedes Mal, wenn Sie eine Methode aufrufen, klicken Sie auf diese Klasse, um sicherzustellen, dass das erwartete Ergebnis zu erhalten. Erstellen einer neuen Instanz bei Bedarf behandelt dem COM + Service. Wenn eine der Methoden zum ersten Mal aufgerufen wird, COM + lädt das **IUpdateNotify** -Objekt und führen Sie es in einem der dllhost.exe Instanzen. Das neue Objekt wird für etwa 3 Minuten im Leerlauf aktiv bleiben. Wenn ein nachfolgender Aufruf innerhalb von drei Minuten des letzten Aufrufs erfolgt, bleibt das **IUpdateNotify** -Objekt geladen, und eine neue Instanz wird nicht erstellt. Wenn kein Aufruf innerhalb von drei Minuten ausgeführt wird, das IUpdateNotify-Objekt wird nicht geladen, und ein neues **IUpdateNotify** -Objekt erstellt werden, wenn beim nächste Aufruf erfolgt. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Klick-und-Los-Installer COM-API (engl.)

In der folgenden API-Dokumentation:
  
- Parameter sind in einem Schlüssel/Wert-Paar Format durch Leerzeichen getrennt ein.
    
- Der Parameter/Kleinschreibung nicht beachtet.
    
- Es ist eine [Liste der Parameter](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) -Dokumentation verfügbar. 
    
- Zusammenfassung der IUpdateNotify2-Schnittstelle ist nun enthalten.
    
### <a name="apply"></a>Anwenden

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parameter

-  _Displaylevel_: **true** , wenn der Installationsstatus angezeigt, einschließlich Fehler, während des Aktualisierungsvorgangs; anzeigen **false** , wenn der Installationsstatus angezeigt, einschließlich Fehler, während des Aktualisierungsvorgangs ausblenden. Der Standardwert ist **false**.
    
-  _Forceappshutdown_: **true,** um das Office-Clientanwendungen heruntergefahren, wenn die Aktion **Übernehmen** sofort ausgelöst wird; zu erzwingen **false** , wenn Fehler auftreten, wenn Office-Clientanwendungen ausgeführt werden. Der Standardwert ist **false**. Weitere Informationen finden Sie unter ["Hinweise"](#bk_ApplyRemark) . 
    
  Wenn eine beliebige Office-Anwendung ausgeführt wird, wenn die Aktion **Übernehmen** ausgelöst wird, schlägt die **Apply** -Aktion in der Regel fehl. Übergeben von `forceappshutdown=true` zu **Übernehmen** Methode bewirkt, dass den Dienst **OfficeClickToRun** sofort Herunterfahren der Anwendung und das Update installieren. Der Benutzer kann in diesem Fall zu Datenverlusten kommen. 
    
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|||
|:-----|:-----|
|**S_OK** <br/> |Aktion wurde erfolgreich an den Klick-und-Los-Dienst für die Ausführung übermittelt.  <br/> |
|**E_ACCESSDENIED** <br/> |Der Anrufer wird nicht mit erhöhten Rechten ausgeführt.  <br/> |
|**E_INVALIDARG** <br/> |Es wurden ungültige Parameter übergeben.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Aktion ist zu diesem Zeitpunkt nicht zulässig. Weitere Informationen finden Sie unter ["Hinweise"](#bk_ApplyRemark) .  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Hinweise

- Wenn eine beliebige Office-Anwendung ausgeführt wird, wenn die Aktion **Übernehmen** ausgelöst wird, wird die Aktion **Übernehmen** fehl. Übergeben von `forceappshutdown=true` für die **Apply** Methode bewirkt, dass den Dienst **OfficeClickToRun** sofort alle Office-Clientanwendungen Herunterfahren, die ausgeführt werden, und wenden Sie das Update. Der Benutzer kann Daten auftreten, wenn sie nicht, zum Speichern von Änderungen zum Öffnen von Dokumenten aufgefordert werden. 
    
- Diese Aktion kann nur ausgelöst werden, wenn der COM-Status auf einen der folgenden ist: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Wenn Sie die **Apply** -Methode aufrufen, ohne zuvor Herunterladen von Inhalten, meldet die **Apply** -Methode nothing anzuwendende erkannt und den Prozess **Übernehmen** erfolgreich abgeschlossen wurde **erfolgreich beendet** . 
    
### <a name="cancel"></a>Cancel

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|||
|:-----|:-----|
|S_OK  <br/> |Aktion wurde erfolgreich an den Klick-und-Los-Dienst für die Ausführung übermittelt.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |Aktion ist zu diesem Zeitpunkt nicht zulässig. Finden Sie im Abschnitt ["Hinweise"](#bk_CancelRemarks) Weitere Informationen  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Hinweise

- Diese Methode kann nur dann ausgelöst, wenn die COM-Status Id **eDOWNLOAD_WIP**. Es wird versucht, die aktuelle Downloadaktion Abbrechen. Der COM-Status wird ändern, **eDOWNLOAD_CANCELLING** und schließlich auf **eDOWNLOAD_CANCELED**. Der COM-Status wird **E_ILLEGAL_METHOD_CALL** zurück, wenn Sie zu einem anderen Zeitpunkt ausgelöst. 
    
### <a name="download"></a>Download

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parameter

-  _Displaylevel_: **true** , wenn der Installationsstatus angezeigt, einschließlich Fehler, während des Aktualisierungsvorgangs; anzeigen **false** , wenn der Installationsstatus angezeigt, einschließlich Fehler, während des Aktualisierungsvorgangs ausblenden. Der Standardwert ist **false**.
    
-  _Updatebaseurl_: URL auf die Quelle alternative herunterladen.
    
-  _Updatetoversion_: die Version Office zu aktualisieren. Definieren Sie dieser Parameter, wenn Sie zu einer älteren Version als die Version zu aktualisieren, die derzeit installierten möchten.
    
-  _Downloadsource_: CLSID der angepassten **IBackgroundCopyManager** -Implementierung (BITS Manager). 
    
-  _Contentid_: identifiziert den Inhalt, den Content Server über die benutzerdefinierten BITS-Manager heruntergeladen werden. Dieser Wert wird über die BITS-Schnittstelle für die Interpretation übergeben.
    
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|||
|:-----|:-----|
|**S_OK** <br/> |Aktion wurde erfolgreich an den Klick-und-Los-Dienst für die Ausführung übermittelt.  <br/> |
|**E_ACCESSDENIED** <br/> |Der Anrufer wird nicht mit erhöhten Rechten ausgeführt.  <br/> |
|**E_INVALIDARG** <br/> |Es wurden ungültige Parameter übergeben.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Aktion ist zu diesem Zeitpunkt nicht zulässig. Weitere Informationen finden Sie unter ["Hinweise"](#bk_DownloadRemark) .  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Hinweise

- Sie müssen als ein Paar _Downloadsource_ und _Contentid_ angeben. Wenn dies nicht der Fall ist, wird die **Download** -Methode wird ein **E_INVALIDARG** -Fehler zurückgegeben. 
    
- Wenn _Downloadsource_, _Contentid_und _Updatebaseurl_ angegeben werden, werden _Updatebaseurl_ ignoriert. 
    
- Diese Aktion kann nur ausgelöst werden, wenn der COM-Status auf einen der folgenden ist: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Wenn Sie die **Apply** -Methode ohne zuvor heruntergeladenen Inhalte aufrufen, meldet die **Apply** -Methode nothing anzuwendende erkannt und den Prozess **Übernehmen** erfolgreich abgeschlossen wurde **erfolgreich beendet** . 
    
#### <a name="examples"></a>Beispiele

- Zum Herunterladen des Inhalts aus dem angepassten BITS-Manager: Rufen Sie die **download()** -Funktion, indem Sie die folgenden Parameter übergeben: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- Zum Herunterladen des Inhalts aus dem Microsoft CDN: Rufen Sie die Funktion **download()** ohne Angabe von _Downloadsource_, _Contentid_oder _Updatebaseurl_ -Parameter. 
    
- Zum Herunterladen des Inhalts von einem benutzerdefinierten Speicherort: Rufen Sie die **download()** -Funktion, indem Sie den folgenden Parameter übergeben: 
    
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
| _pUpdateStatusReport_ <br/> |Zeiger auf eine UPDATE_STATUS_REPORT-Struktur.  <br/> |
   
#### <a name="return-results"></a>Zurückgeben von Ergebnissen

|||
|:-----|:-----|
|**S_OK** <br/> |Die **Status** -Methode gibt immer dieses Ergebnis zurück. Überprüfen Sie die `UPDATE_STATUS_RESULT` Struktur für den Status der aktuellen Aktion.  <br/> |
   
#### <a name="remarks"></a>Hinweise

- Im Statusfeld der `UPDATE_STATUS_REPORT` enthält den Status der aktuellen Aktion. Die folgenden Status-Werte zurückgegeben: 
    
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

- Wenn ein Fehler auftritt, die Fehler dar, der im letzte Befehl zur Folge der `UPDATE_STATUS_REPORT` enthält detaillierte Informationen zu dem Fehler. Zwei Arten von Fehlercodes werden von der **Status** -Methode zurückgegeben. 
    
- Wenn der Fehler weniger als `UDPATE_ERROR_CODE::eUNKNOWN`, der Fehler befindet sich eine der folgenden vordefinierten Fehlercodes:
    
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

  Wenn der zurückgegebenen Fehlercode übersteigt `UDPATE_ERROR_CODE::eUNKNOWN` **HRESULT** eines Funktionsaufrufs fehlgeschlagen ist. So extrahieren Sie das HRESULT subtrahieren `UDPATE_ERROR_CODE::eUNKNOWN` aus der im Fehlerfeld der zurückgegebene Wert der `UPDATE_STATUS_REPORT`.
    
  Die vollständige Liste der Status- und Fehlerinformationen Werte kann durch die **IUpdateNotify** -Typbibliothek in OfficeC2RCom.dll eingebettet überprüfen angezeigt werden. 
    
- Feld Contentid wird für Anrufe beim **Status** nach dem **Download** wurde initiiert, und gibt die Contentid, die für den Aufruf der **herunterladen** übergeben wurde. Es ist ratsam, initialisiert dieses Feld auf **einen Nullwert fest** , bevor Sie die **Status** -Methode aufrufen, und überprüfen Sie den Wert an, nach dem **Status** zurückgegeben wurde. Wenn der Wert immer noch **null**ist, bedeutet dies, dass keine Contentid zurückzugebenden vorhanden ist. Wenn der Wert nicht **null**ist, müssen Sie es mit einem Aufruf von **SysFreeString() frei**frei. Nachfolgend finden Sie ein Codeausschnitt zum **Status** nach dem **herunterladen**aufrufen.
    
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

> [!NOTE]
> Diese Zusammenfassung wird als eine Ergänzung-Info für [Integrating Verwaltbarkeit Clientanwendungen mit dem Office 365 Klick-und-Los-Installationsprogramm](https://msdn.microsoft.com/EN-US/library/office/mt608768.aspx)bereitgestellt. Nachdem die öffentlichen Doc aktualisiert wird, kann dieses Dokument als veraltet betrachtet werden. 
  
Von C2RTenant [16.0.8208.6352](http://oloop/BuildGroup/Details/tenantc2rclient#3519/1255278) (erste öffentlich zugänglichen Build sollte Juni Verzweigung Build – 8326.*) haben wir eine neue **IUpdateNotify2** Schnittstelle hinzugefügt. Nachfolgend finden Sie einige grundlegende Informationen über diese Schnittstelle: 
  
- CLSID_UpdateNotifyObject2 {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Diese Schnittstelle gehostet auch die ursprüngliche IUpdateNotify-Schnittstelle, um die Abwärtskompatibilität zu gewährleisten. D. h., wenn Sie diese Schnittstelle verwenden, haben Sie Zugriff auf alle Methoden, die in **UpdateNotifyObject** -Schnittstelle bereitgestellt. 
    
- Neue Methoden IUpdateNotify2 hinzugefügt:
    
  - **HRESULT** GetBlockingApps ([out] BSTR \* AppsList). Rufen Sie Updates blockieren apps-Liste ab. Dieses Anrufs gibt ausgeführten Office-apps zurück, die den Aktualisierungsprozess aus fortfahren blockiert wird. 
    
  - **HRESULT** GetOfficeDeploymentData (Int unter DataType **LPCWSTR** PcwszName, BSTR [out] [in] [in] * OfficeData). Möchten Sie Office-Bereitstellung Daten erhalten. 
    
- Wenn Sie die neuen Methoden verwenden möchten, müssen Sie dafür sorgen:
    
  - Ihre C2R Version ist neuer als die oben genannten Build (\>= Juni Verzweigung Build).
    
  - Verwenden Sie UpdateNotifyObject2, anstatt **UpdateNotifyObject** **CoCreateInstance**aufrufen.
    
Wenn Sie eine der neuen Methoden nicht verwenden, müssen Sie nichts ändern. Alle vorhandenen Methoden funktioniert als genau die gleiche Weise wie vor.
  
## <a name="implementing-the-bits-interface"></a>Implementieren der BITS-Schnittstelle

Den [Intelligenten Hintergrundübertragungsdienst](https://msdn.microsoft.com/en-us/library/bb968799(v=vs.85).aspx) (BITS) ist ein Dienst von Microsoft zum Übertragen von Dateien zwischen einem Client und Server bereitgestellt. BITS ist einer der Kanäle, die Office Klick-und-Los-Installer verwenden können, um Inhalte herunterzuladen. In der Standardeinstellung integriert der Office Klick-und-Los Installer verwendet die Windows Implementierung von BITS zum Herunterladen des Inhalts aus dem CDN. 
  
Durch eine benutzerdefinierte Implementierung BITS an **der Download()-Methode** der **IUpdateNotify** -Schnittstelle bereitstellen, kann Ihre Software Verwaltbarkeit steuern, wo und wie der Client den Inhalt downloads. Eine benutzerdefinierte BITS-Schnittstelle ist nützlich, wenn einen benutzerdefinierte Verteilung von Inhalten Channel als integrierte Klick-und-Los-Kanäle, wie beispielsweise dem Office-CDN IIS-Servern bereitstellen oder Dateifreigaben. 
  
Die Mindestanforderung für eine benutzerdefinierte BITS-Schnittstelle zum Arbeiten mit Office C2R-Dienst ist:
  
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

- Für die `Addfile` und `AddFileWithRanges` Funktionen, die remote-URL ist im folgenden Format: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - Cmbits ist schwierig codiert und steht für angepasste BITS.
    
  -  _ \<Contentid\> _ ist der Parameter _Contentid_ für **die Download()-Methode** . 
    
  -  _ \<relativen Pfad zur Zieldatei\> _ stellt den Speicherort und den Namen der Datei zum Herunterladen bereit. 
    
    Beispielsweise, wenn Sie eine _Contentid_ des bereitgestellt haben `f732af58-5d86-4299-abe9-7595c35136ef` der **Download()** -Methode und Office C2R möchte, laden Sie die Version CAB-Datei wie `v32.cab` Datei, wird es **AddFile()** aufrufen, durch den folgenden `RemoteUrl`:
    
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

<!--## Automating content staging

IT administrators can choose to have desktop clients enabled to automatically receive updates when they are available directly from the Microsoft Content Delivery Network (CDN) or they can choose to control the deployment of updates available from the [update channels](https://support.office.com/en-us/article/Overview-of-update-channels-for-Office-365-ProPlus-9ccf0f13-28ff-4975-9bd2-7e4ea2fefef4?ui=en-US&rs=en-US&ad=US) using the [Office 2016 Deployment Tool](https://www.microsoft.com/en-us/download/details.aspx?id=49117) or [System Center Configuration Manager](https://support.office.com/en-us/article/Manage-updates-to-Office-365-ProPlus-with-System-Center-Configuration-Manager-b4a17328-fcfe-40bf-9202-58d7cbf1cede).
  
The service supports the ability for management tools to recognize and automate the download of the content when updates are made available.
  
**Following is a diagram showing the overview of downloading a custom image**

![An overview of downloading Office updates from the CDN.](media/9afac230-6b22-4526-a800-0562708cc436.png "An overview of downloading Office updates from the CDN")
  
In the above diagram you see that a new Office 365 ProPlus image is available on the Office Content Distribution Network (CDN). Along with the Office 365 ProPlus image, an XML-formatted file list is also available which has the information needed to enable manageability software to directly create customized images replacing the need for using the Office Deployment Tool.
  
An enterprise configures their WSUS to sync the Office 365 Client Updates. These updates do not contain the actual image payload but does allow the manageability software to recognize when new content is available. The manageability software can then read the Client Update metadata to understand what version of Office the update applies to.
  
If the update is applicable, the manageability software can use the CDN content and the file list to create the custom image and store it onto the file share location that it is configured to use.
  
### Format of the XML file list

There are two file lists available in a cab file on the CDN. One lists the files for the 32-bit version of Office and one for the 64-bit version of Office. The URL of the location of the Office File List (OFL.CAB) file is [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab). The two file lists are called:
  
- O365Client_32bit.xml
    
- O365Client_64bit.xml
    
Within the XML for each of the file lists is an  `UpdateFiles` node which contains a version attribute.  `UpdateFiles version="1.4"`.
  
This version is incremented if changes are made to the file lists.
  
There are two parameters that need to be combined with the XML to make a custom image: 
  
- Replace  _%version%_ with the build version of Office. This can be derived from the Client Update metadata  `MoreInfoURL` field, see below. 
    
- Define  _baseURL_ by using the URL value associated with the branch the image is being created for. This can be derived from the Client Update metadata, see below. 
    
The steps for creating an image are:
  
1. Open the XML file list.
    
2. Replace occurrences of  _%version%_ with the applicable Office build version. The build version can be acquired from releasehistory.xml as described later in this article. 
    
3. Read the URL attribute for the target branch.
    
4. Remove language nodes for any languages not required in the custom image.
    
   > [!NOTE]
   > Nodes with language='0' are language neutral and must be included in the image. 
  
5. Construct a local image of the CDN by iterating through the XML file list and copying the CDN files, while creating the folder structure as needed. 
    
   - If the  _rename_ attribute is provided, then rename the copied file to the value provided in the  _rename_ attribute. This used to create the top-level default v64.cab and v32.cab files. These are the renamed versions of the top-level build cab file and are used as the default installation version if the version is not specified. 
    
   - Use URL + relativePath + filename to construct the CDN location.
    
The following examples use the Monthly channel (as defined by the  `baseURL` node) and build version 16.0.4229.1004 from releasehistory.xml. 
  
```cpp
baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" /
```

- The following is a language neutral file needed for all languages. The name of the file is v64_16.0.4229.1004.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab and renamed to …/office/data/v64.cab.
    
  ```cpp
  baseURL branch="Business" URL="http://officecdn.microsoft.com/pr/7ffbc6bf-bc32-4f92-8982-f9dd17fd3114" /
  File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/
  
  ```

- The following is a file to be included in the en-US image as designated by the language LCID=1033. The name of the file is s641033.cab and it should be copied from http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab and not renamed.
    
  ```cpp
  File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" /
  ```

### Hash verification of data files

Image creation tools may verify the integrity of the downloaded .dat files by comparing a computed HASH value with the supplied HASH value associated with each of the .dat files. Below is an example of a .dat file from the Monthly channel with build version 16.0.4229.1004 and language set to Bulgarian.
  
```cpp
File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"
```

- The  _hashLocation_ attribute specifies the relative path location of the stream.x64.bg-bg.hash for the stream.x64.bg-bg.dat file. Construct the hash file location by concatenating URL + relativePath + hashLocation. In this example the stream.x64.bg-bg.hash location would be http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
    
- The  _hashAlgo_ attribute specifies what hashing algorithm was used. In this case the Sha256 algorithm was used. 
    
To validate the integrity of the stream.x64.bg-bg.dat file, open the stream.x64.bg-bg.hash and read the hash value from the first line of text in the hash file. Compare this to the has value that you computed using the specified hashing algorithm to verify that the values match. Use the following C# code to read the hash.
  
```cs
string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
string readHash = readHashes.First();

```

### Office 365 Client Updates

Office 365 Client Updates enable manageability software to treat the Office 365 Client Updates in a manner very similar to any other WU update with one exception; the client updates do not contain an actual payload. The Office 365 Client Updates should not be installed on any clients but rather used to trigger the workflows with the manageability software replacing the installation command with the COM based installation mechanism shown above.
  
**Office 365 Client Update workflow**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow diagram for O365PP client updates")
  
Each Office 365 Client Update that is published includes metadata about the update. This metadata includes a parameter called  _MoreInfoUrl_ which can be used to derive the following information: 
  
-  _Ver_: Identifies the Office version associated with this update. For example 16.0.4229.1004.
    
-  _Branch_: Identifies the Update Channel for this update. Values include InsiderFast, Insiders, Monthly, Targeted, Broad. Additional values may be added in the future.
    
-  _Arch_: Identifies the processor architecture associated with this update.
    
-  _xmlVer_: Identifies the version of the XML file lists to use to construct the base image for this update.
    
-  _xmlPath_: Path to the OFL.CAB file that contains the XML file lists.
    
-  _xmlFile_: The name of the file list that should be used for this update. The value will be  `O365Client_32bit` or  `O365Client_64bit` and will match the value in  _Arch_.
    
The following is an example of the  _MoreInfoURL_ parameter which refers to the Office 365 Client Update for the 32-bit version of Office with build version of 16.0.2342.2343 on the Current channel. 
  
```http
http://officecdn.microsoft.com/pr/wsus/ofl.cab is the location of the XML file lists for this update, specifically the O365Client_32bit.xml from within the OFL.CAB.
http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml 

```
THE ABOVE SECTION APPEARS TO BE A DUPLICATE OF THE FOLLOWING SECTION; TEMPORARILY COMMENTING IT OUT.-->

## <a name="automating-content-staging"></a>Automatisieren von staging

IT-Administratoren können festlegen, dass Desktopclients aktiviert, um Updates automatisch zu erhalten, wenn sie direkt aus dem Microsoft Content Delivery Network (CDN) verfügbar sind oder sie verhindern können, dass die Bereitstellung von Updates von der Update steuern mit dem Office-Bereitstellungstools oder System Center Configuration Manager Kanäle.
  
Der Dienst unterstützt die Möglichkeit für Verwaltungstools zu erkennen und das Herunterladen des Inhalts automatisieren, wenn Updates verfügbar gemacht werden.
  
**In der folgenden Abbildung wird eine Übersicht über ein benutzerdefiniertes Bild herunterladen**

![Ein Diagramm der Verwendung der COM-Schnittstelle auf das Installationsprogramm von Office Klick-und-los.] (media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm der Verwendung der COM-Schnittstelle auf die Office Klick-und-Los-installer")
  
### <a name="overview-of-downloading-a-custom-image"></a>Übersicht über ein benutzerdefiniertes Bild herunterladen
  
Im vorherigen Diagramm sehen Sie, dass ein neues Office 365 ProPlus Bild auf der Office Content Verteilung Network (CDN) verfügbar ist. Zusammen mit der Office 365 ProPlus Bild ist eine XML-formatierte Dateiliste auch verfügbar hat die Informationen für die Verwaltbarkeit Software direkt angepassten Bilder ersetzen die Notwendigkeit für die Verwendung von Office-Bereitstellungstool erstellt werden kann.
  
Ein Unternehmen konfiguriert ihre WSUS, um die Office 365-Clientupdates synchronisieren. Diese Updates lässt die Verwaltbarkeit Software zu erkennen, wenn neuer Inhalt verfügbar ist jedoch keine tatsächliche Bild Nutzlast enthalten. Die Verwaltbarkeit Software können Sie lesen, die Metadaten zu aktualisieren, um verstehen, welche Version von Office, das Update angewendet wird.
  
Wenn das Update anwendbar ist, die Verwaltbarkeit Software mit den CDN-Inhalt und der Dateiliste können Sie das benutzerdefinierte Bild erstellen und speichern Sie sie auf den Speicherort der Freigabe, die sie konfiguriert ist verwenden.
  
### <a name="format-of-the-xml-file-list"></a>Format der Liste der XML-Datei

Es stehen zwei Dateilisten in einer CAB-Datei auf dem CDN. Eine Listet die Dateien für die 32-Bit-Version von Office und einen für 64-Bit-Version von Office. Die URL des Speicherorts der Liste der Office-Datei (OFL. CAB-Datei) Datei ist [http://officecdn.microsoft.com/pr/wsus/ofl.cab](http://officecdn.microsoft.com/pr/wsus/ofl.cab). Die zwei Dateilisten heißen:
  
- O365Client_32bit.Xml
    
- O365Client_64bit.Xml
    
In den XML-Code für jede der Datei Listen ist ein <UpdateFiles> Knoten, der ein Versionsattribut enthält.  `<UpdateFiles version="1.4">`. Diese Version wird erhöht, wenn die Dateilisten geändert werden.
  
Es gibt zwei Parameter, die mit den XML-Code zu einem benutzerdefinierten Bild kombiniert werden müssen: 
  
- Ersetzen Sie *Version %* durch die Version von Office. Dies kann aus den Client-Update-Metadaten (im nächsten Abschnitt erläutert) abgeleitet werden. 
    
- Definieren von *BaseURL* mithilfe von URL-Wert der zugeordneten der Verzweigung, die, der für das Bild erstellt wird. Dies ist die Client-Update-Metadaten, die im folgenden Abschnitt erläutert abgeleitet. 
    
Die Schritte zum Erstellen eines Images sind:
  
1. Öffnen Sie die Liste der XML-Datei.
    
2. Ersetzen Sie Vorkommen von *Version %* mit der entsprechenden Version des Office-Build. Die Build-Version kann von releasehistory.xml erworben werden, wie weiter unten in diesem Artikel beschrieben. 
    
3. Lesen Sie das URL-Attribut für die Ziel-Verzweigung.
    
4. Entfernen Sie Knoten für alle Sprachen in benutzerdefinierten Bilds nicht erforderlich.
    
   > [!NOTE]
   > Knoten mit Language = "0" Sprache neutral werden und muss in das Bild enthalten sein. 
  
5. Erstellen eines lokalen Bilds von dem CDN durch Durchlaufen der Liste der XML-Datei, und kopieren die CDN-Dateien beim Erstellen der Ordnerstruktur, je nach Bedarf. 
    
   - Wenn das *rename* -Attribut angegeben ist, bereitgestellt dann *Umbenennen* die kopierte Datei auf den Wert in das Attribut umbenennen. Hiermit wird die v64.cab und v32.cab-Dateien auf oberster Ebene erstellen. Dies sind die umbenannten Versionen der CAB-Datei auf oberster Ebene erstellen und als die Standardversion der Installation verwendet werden, wenn die Version nicht angegeben ist. 
    
   - Verwenden Sie URL RelativePath + Dateiname, um den Speicherort CDN erstellen.
    
Im folgenden finden Sie Beispiele für die Verwendung den monatlichen DDE-Kanal (gemäß Definition durch die `<baseURL>` Knoten) und Buildversion 16.0.4229.1004 aus releasehistory.xml. 
  
```xml
<baseURL branch="Monthly" URL="http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60" />
```

- Es folgt eine neutrale Language-Datei für alle Sprachen erforderlich ist. Der Name der Datei v64_16.0.4229.1004.cab und es aus kopiert werden sollte `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/v64_16.0.4229.1004.cab` und umbenannt in `…/office/data/v64.cab`. 
    
  ```xml
  <File name="v64_%version%.cab" rename="v64.cab" relativePath="/office/data/" language="0"/>
  
  ```

- Im folgenden finden Sie eine Datei in das Bild En-US enthalten sein, von der Sprache LCID Datenbankverzeichnis = 1033. Der Name der Datei s641033.cab und es aus kopiert werden sollte `http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641033.cab` und nicht umbenannt.
    
  ```xml
  <File name="s641033.cab" relativePath="/office/data/%version%/" language="1033" />
  ```

### <a name="hash-verification-of-dat-files"></a>Hash-Prüfung der .dat-Dateien

Bild-Erstellungstools können die Integrität der heruntergeladenen .dat-Dateien überprüfen, indem ein berechneter Hashwert mit dem angegebenen Hashwert gehörenden der .dat-Dateien vergleichen. Es folgt ein Beispiel einer .dat-Datei aus dem monatlichen Channel mit Buildversion 16.0.4229.1004 und Sprache Bulgarisch:
  
```xml
<File name="stream.x64.bg-bg.dat" hashLocation="s641026.cab/stream.x64.bg-bg.hash" hashAlgo="Sha256" relativePath="/office/data/%version%/" language="1026"/>
```

- Das **HashLocation** -Attribut gibt den relativen pfadspeicherort der die stream.x64.bg-bg.hash für die Datei stream.x64.bg bg.dat. Erstellen Sie den Speicherort der Hash durch Verketten URL RelativePath + HashLocation. Im folgenden Beispiel wäre der stream.x64.bg bg.hash-Speicherort: 
    
  ```http
  http://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- Das **HashAlgo** -Attribut gibt an, welcher Hashalgorithmus verwendet wurde. In diesem Fall diente Sha256. 
    
  Überprüfen Sie die Integrität der Datei stream.x64.bg bg.dat, öffnen Sie die stream.x64.bg-bg.hash, und Lesen Sie den HASH-Wert, der die erste Zeile des Texts in der Hashdatei ist. Vergleichen Sie dies mit den berechneten Hashwert (mit dem angegebenen Hashalgorithmus), um die Integrität der heruntergeladenen .dat-Datei zu überprüfen.
    
  Das folgende Beispiel zeigt den C#-Code zum Lesen von des Hashs.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="office-365-client-updates"></a>Office 365-Clientupdates

Alle Office 365-Clientupdates werden mit dem [Microsoft Update-Katalog](http://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)veröffentlicht.
  
Office 365-Clientupdates aktivieren Verwaltbarkeit Software, die Office 365-Clientupdates sehr ähnlich wie andere WU Update mit einer Ausnahme behandeln. Die Clientupdates enthalten keine tatsächliche Nutzlast. Die Office 365-Clientupdates sollten nicht auf allen Clients installiert, sondern vielmehr verwendet, um die Workflows mit der Verwaltbarkeit Software ersetzen den Installationsbefehl mit dem COM-Installationsmechanismus oben gezeigten basierend Trigger. 
  
**Die folgende Abbildung zeigt ein Diagramm des Office 365-Clientupdate Workflows.**

![Workflowdiagramm für O365PP Clientupdates.] (media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflowdiagramm für O365PP Clientupdates")
  
Jeder Office 365-Client zu aktualisieren, die veröffentlicht wird enthält Metadaten zum Update. Diese Metadaten enthält einen Parameter namens *MoreInfoUrl* die abgeleitet werden die folgende Informationen verwendet werden kann: 
  
-  *Ver*: identifiziert die Office-Version dieses Update zugeordnet. 
    
-  *Branch*: der Update-Kanal für dieses Update identifiziert. Werte enthalten InsiderFast, Insider, monatlich, gezielte, Broad. Zusätzliche Werte können in der Zukunft hinzugefügt werden. 
    
-  *Bogen*: identifiziert die Prozessorarchitektur dieses Update zugeordnet. 
    
-  *XmlVer*: die Version der XML-Dateilisten, die zum Erstellen des Basis Bilds für dieses Update verwendet werden soll. 
    
-  *XmlPath*: Pfad zu der OFL. CAB-Datei, die die XML-Datei enthält enthält. 
    
-  *MlFile*: der Name der Dateiliste, die für dieses Update verwendet werden soll. Der Wert ist O365Client_32bit oder O365Client_64bit und entspricht den Bogen. 
    
Die folgende URL ist ein Beispiel des Parameters *MoreInfoURL* bezieht sich auf die Office 365-Client-Updates für die 32-Bit-Version von Office mit Buildversion von 16.0.2342.2343 auf dem aktuellen Kanal. 
  
http://officecdn.microsoft.com/pr/wsus/ofl.cabist der Speicherort der XML-Dateilisten für dieses Update, insbesondere die O365Client_32bit.xml aus, die sich innerhalb der OFL. CAB-DATEI.
  
[Office 365-Client-Kanal Updateversionen](http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.8326.2096&Branch=Current&Arch=64&XMLVer=1.4&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml)
  
### <a name="additional-metadata-for-automating-content-staging"></a>Zusätzliche Metadaten für die Automatisierung von Content staging

Zusätzlich zu den Metadaten, die veröffentlicht wird definiert die vorhanden sind, auch zusätzliche XML-Dateien veröffentlicht das CDN kann, die zusätzliche Informationen zu den Office 365-Clients zu ermöglichen, die aus dem CDN Office verfügbar sind.
  
**SKUS. XML**
  
Dieser XML-Datei in einer signierten CAB-Datei enthalten ist und auf dem Office CDN unter der folgenden URL veröffentlicht: [http://officecdn.microsoft.com/pr/wsus/skus.cab](http://officecdn.microsoft.com/pr/wsus/skus.cab).
  
Die Metadaten, die in der XML-Datei veröffentlicht eignet sich für bestimmen, welche Produkte für die Bereitstellung verfügbar sind und aus dem CDN Office zusammen mit verschiedenen Optionen für die einzelnen warten. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseInfo PublishedDate="08/07/2017 16:34">
  <!-- Suite / App catalog -->
  <Suite>
    <SKU Name="Office 365 ProPlus" ProductID="O365ProPlusRetail" Default="True">
      <Apps>
        <App Name="Access" AppID="Access" />
        <App Name="Excel" AppID="Excel" />
        <App Name="OneDrive for Business (Groove)" AppID="Groove" />
        <App Name="OneDrive for Business (Next Gen Sync Client)" AppID="OneDrive" />
        <App Name="OneNote" AppID="OneNote" />
        <App Name="Outlook" AppID="Outlook" />
        <App Name="PowerPoint" AppID="PowerPoint" />
        <App Name="Publisher" AppID="Publisher" />
        <App Name="Skype for Business" AppID="Lync" />
        <App Name="Word" AppID="Word" />
      </Apps>
      <Channels>
        <Channel ID="Monthly"/>
        <Channel ID="Insiders"/>
        <Channel ID="Targeted"/>
        <Channel ID="Broad"/>
      </Channels>
    </SKU>
```

** \<ReleaseInfo\> ** Stammknoten enthält das PublishedDate-Attribut das das Datum identifiziert, die diese Datei veröffentlicht wurde. 
  
** \<SKU\> ** Knoten identifiziert eine einzelne SKU. 
  
- Das *Produkt-ID* -Attribut identifiziert die ID, die als ID-Attribut in der Datei "Configuration.xml" übergeben wird, wenn die ODT verwenden. Beispiel: `<Product ID="O365ProPlusRetail">`. 
    
- Die *Standard* -Attributs, wenn auf true ist, identifiziert die empfohlene SKU festgelegt. 
    
** \<App\> ** Knoten werden verwendet, um die einzelnen Office-apps zu definieren, die jede SKU unterstützt. 
  
- *Name* -Attributs ist der angezeigten Anwendungsname. 
    
- Das Attribut *AppID* ist das ID-Attribut in der Datei "Configuration.xml" für übergeben der ** \<ExcludeApp\> ** Knoten, wenn die ODT verwenden. Beispiel: `<ExcludeApp ID="Publisher" />`. 
    
**RELEASEHISTORY. XML**
  
Diese XML-Datei in einer signierten CAB-Datei enthalten ist und auf dem Office CDN am folgenden Speicherort veröffentlicht: [http://officecdn.microsoft.com/pr/wsus/releasehistory.cab](http://officecdn.microsoft.com/pr/wsus/releasehistory.cab). 
  
Die Metadaten, die in der XML-Datei veröffentlicht ist nützlich für die Bestimmung, welche Kanäle für die Wartung der Updates aus dem CDN Office zusammen mit Informationen zum Verlauf Build für jeden unterstützten Kanäle unterstützt werden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<ReleaseHistory PublishedDate="10/22/2017 00:48">
  <UpdateChannel Name="Current" ID="Monthly" DisplayName="Monthly Channel">
    <Update Latest="True" Version="1709" LegacyVersion="16.0.8528.2139" Build="8528.2139" PubTime="2017-10-16T19:45:50.743Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2107" Build="8431.2107" PubTime="2017-10-11T01:52:33.793Z" />
    <Update Latest="False" Version="1708" LegacyVersion="16.0.8431.2079" Build="8431.2079" PubTime="2017-09-18T22:26:13.673Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2107" Build="8326.2107" PubTime="2017-09-12T18:56:53.657Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2096" Build="8326.2096" PubTime="2017-08-30T00:10:25.253Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2076" Build="8326.2076" PubTime="2017-08-19T00:13:01.787Z" />
    <Update Latest="False" Version="1707" LegacyVersion="16.0.8326.2073" Build="8326.2073" PubTime="2017-08-11T19:35:42.173Z" />
  </UpdateChannel>
```

Die ** \<ReleaseHistory\> ** Stammknoten enthält das PublishedDate-Attribut das das Datum identifiziert, die diese Datei veröffentlicht wurde. 
  
Die ** \<UpdateChannel\> ** Knoten definiert einen unterstützten Kanal. 
  
- Das *Name* -Attribut definiert die DDE-Kanal-ID, die zum Übergeben an die ODT in der Datei "Configuration.xml" als Channel-Attribut verwendet wird. 
    
  Beispiel: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Current">` 
    
  > [!NOTE] 
  > Dieses Attribut ist veraltet und wird nur für Abwärtskompatibilität verwendet. Verwenden Sie das ID-Attribut anstelle des Name-Attributs. 
    
- Das *ID* -Attribut definiert die DDE-Kanal-ID, die zum Übergeben an die ODT in der Datei "Configuration.xml" als Channel-Attribut verwendet wird. 
    
  Beispiel: `<Add SourcePath="\\Server\Share" OfficeClientEdition="32" Channel="Deferred">` 
    
- Das **DisplayName** -Attribut wird als Anzeigename verwendet. 
    
Die ** \<aktualisieren\> ** Knoten wird verwendet, um jedes Update zu definieren, die für den bestimmten Kanal veröffentlicht wurde. 
  
- Die- **neueste** Attributs, wenn auf true ist, definiert die Version, die die neueste Version für diesen Kanal ist festgelegt. 
    
- Das **Version** -Attribut definiert die Versionsnummer für dieses bestimmte Update. 
    
- Das **LegacyVersion** -Attribut definiert die vollständige Versionsnummer für dieses bestimmte Update. 
    
- Das **Build** -Attribut definiert die Buildnummer für dieses bestimmte Update. 
    
- Das **PubTime** -Attribut definiert das Datum und die Uhrzeit, an dem dieses Update auf dem Office-CDN veröffentlicht wurde. 
    

