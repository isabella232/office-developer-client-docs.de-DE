---
title: Integrieren von Verwaltbarkeit-Anwendungen mit dem Click-to-Run-Installationsprogramm von Microsoft 365 apps
manager: lindalu
ms.date: 09/28/2020
ms.audience: ITPro
localization_priority: Normal
ms.assetid: c0fa8fed-1585-4566-a9be-ef6d6d1b4ce8
description: In diesem Artikel erfahren Sie, wie Sie das Click-to-Run-Installationsprogramm von Microsoft 365 apps mit einer Software Verwaltungslösung integrieren.
ms.openlocfilehash: eccd634f7906acf25b521ed2deb456ca914f37da
ms.sourcegitcommit: c8c51bd3f51c0a59fe44c014c8e56f1ba7c7aa03
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/28/2020
ms.locfileid: "48297314"
---
# <a name="integrating-manageability-applications-with-microsoft-365-apps-click-to-run-installer"></a>Integrieren von Verwaltbarkeit-Anwendungen mit dem Click-to-Run-Installationsprogramm von Microsoft 365 apps

In diesem Artikel erfahren Sie, wie Sie das Click-to-Run-Installationsprogramm von Microsoft 365 apps mit einer Software Verwaltungslösung integrieren.
  
Das Klick-und-Los-Installationsprogramm von Microsoft 365 apps stellt eine COM-Schnittstelle bereit, die IT-Experten und Software Verwaltungslösungen die programmgesteuerte Steuerung der Updateverwaltung ermöglicht. Diese Schnittstelle stellt zusätzliche Verwaltungsfunktionen bereit, die über das Office-Bereitstellungs Tool hinausgehen.
  
> [!NOTE]
> Dieser Artikel bezieht sich auf Office-Apps, die das Klick-und-Los-Installationsprogramm verwenden. 
  
## <a name="integrating-with-the-click-to-run"></a>Integrieren in das Klick-und-Los

Um diese Schnittstelle zu verwenden, ruft eine verwaltbare Anwendung die COM-Schnittstelle auf und ruft freigegebene APIs auf, die direkt mit dem Klick-und-Los-Installationsdienst kommunizieren. 
  
> [!NOTE]
> Das Office-Klick-und-Los-Installationsprogramm kann über die Befehlszeile mit Parametern ausgeführt werden, die das Verhalten steuern können, wie im [Office-Bereitstellungs Tool für Klick-und-Los](https://docs.microsoft.com/DeployOffice/overview-office-deployment-tool)dokumentiert. 
  
**Es folgt ein konzeptionelles Diagramm der COM-Schnittstelle.**

![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm zur Verwendung der COM-Schnittstelle im Office-Klick-und-Los-Installationsprogramm")
  
Das Klick-und-Los-Installationsprogramm von Microsoft 365 apps implementiert eine COM-basierte Schnittstelle, die **IUpdateNotify** für CLSID **CLSID_UpdateNotifyObject**registriert ist.
  
Diese Schnittstelle kann wie folgt aufgerufen werden:
  
```cpp
hr = CoCreateInstance(CLSID_UpdateNotifyObject, NULL, CLSCTX_ALL,
       IID_IUpdateNotify, 
      (void **)&p); 
```

Der Anruf ist nur erfolgreich, wenn der Anrufer unter erhöhten Rechten ausgeführt wird, da das Installationsprogramm für die Klick-und-Los-Installation mit erhöhten Rechten ausgeführt werden muss.
  
Die **IUpdateNotify** -com-Schnittstelle stellt drei asynchrone Funktionen zur Verfügung, die für die Überprüfung der Befehle und Parameter und die Planung der Ausführung mit dem Klick-und-Los-Installationsdienst verantwortlich sind. 
  
```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
HRESULT Cancel() // Cancel the download action.

```

Eine Forth-Methode, **Status**, kann verwendet werden, um Informationen über den Status des zuletzt ausgeführten Befehls oder den Status des derzeit ausgeführten Befehls abzurufen (also Erfolg, Fehler, detaillierte Fehlercodes).
  
```cpp
HRESULT status([out] _UPDATE_STATUS_REPORT* pUpdateStatusReport) // Get status of current action. 
typedef struct _UPDATE_STATUS_REPORT  
{  
UPDATE_STATUS status;  
UINT error; 
BSTR contentid;  
} UPDATE_STATUS_REPORT;

```

Es gibt vier Zustände, in denen der Klick-und-Los-Installationsdienst während seines Lebenszyklus möglicherweise vorliegt, während dessen **IUpdateNotify** -Methoden aufgerufen werden können. Neustarten, Leerlauf, herunterladen und anwenden. 
  
**Im folgenden finden Sie das Diagramm "Statuscomputer" der COM-Schnittstelle**

![A state diagram for the COM interface.](media/a409003e-6876-4ab3-bb4c-cd0c0fed5cbb.png "Ein Statusdiagramm für die COM-Schnittstelle")
  
> [!NOTE]
> **Neustart: beim**Booten des Computers gibt es einen Zeitraum, in dem der Klick-und-Los-Installationsdienst nicht verfügbar ist. Ein erfolgreicher Aufruf der Status-Methode nach einem Neustart wird eUPDATE_UNKNOWN zurückgegeben. 
  
**Leerlauf:** Wenn sich das Klick-und-Los-Installationsprogramm im Leerlauf befindet, können Sie Folgendes aufrufen: 
  
- **Apply**: Installieren Sie zuvor heruntergeladenen Inhalt.
    
- **Cancel**: Gibt zurück  `0x800000e` , "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen."
    
- **Download**: lädt neue Inhalte zur späteren Installation auf den Client herunter.
    
- **Status**: gibt das Ergebnis der letzten abgeschlossenen Aktion oder eine Fehlermeldung zurück, wenn die Aktion mit einem Fehler beendet wurde. Wenn keine vorherige Aktion vorliegt, wird der **Status** zurückgegeben  `eUPDATE_UNKNOWN` .
    
**Herunterladen:** Wenn sich das Klick-und-Los-Installationsprogramm im Download Zustand befindet, können Sie Folgendes aufrufen: 
  
- **Apply**: gibt ein **HRESULT** mit dem Wert  `0x800000e` "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.
    
- **Abbrechen**: beendet den Download und entfernt die teilweise heruntergeladenen Inhalte.
    
- **Download**: gibt ein **HRESULT** mit dem Wert  `0x800000e` "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück. 
    
- **Status**: gibt **DOWNLOAD_WIP** zurück, um anzugeben, dass die Download Arbeit ausgeführt wird. 
    
**Anwendung:** Wenn das Klick-und-Los-Installationsprogramm den Download Inhalt bereits installiert hat: 
  
- **Apply**: gibt ein **HRESULT** mit dem Wert  `0x800000e` "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück.
    
- **Cancel**: Gibt zurück  `0x800000e` , die Apply-Aktion kann nicht abgebrochen werden.
    
- **Download**: gibt ein **HRESULT** mit dem Wert  `0x800000e` "eine Methode wurde zu einem unerwarteten Zeitpunkt aufgerufen." zurück. 
    
- **Status**: gibt **APPLY_WIP** zurück, um anzugeben, dass die Anwendung "Arbeit" ausgeführt wird. 
    
> [!NOTE]
> Da OfficeC2RCOM ein com+-Dienst ist und dynamisch geladen wird, müssen Sie **CoCreateInstance** jedes Mal aufrufen, wenn Sie eine Methode für diese Klasse aufrufen, um sicherzustellen, dass Sie das erwartete Ergebnis erhalten. Der com+-Dienst behandelt das Erstellen einer neuen Instanz, wenn dies erforderlich ist. Wenn eine der Methoden zum ersten Mal aufgerufen wird, lädt com+ das **IUpdateNotify** -Objekt, und es wird in einer der dllhost.exe-Instanzen ausgeführt. Das neue Objekt bleibt im Leerlauf etwa 3 Minuten aktiv. Wenn ein anschließender Aufruf innerhalb von drei Minuten nach dem letzten Aufruf erfolgt, bleibt das **IUpdateNotify** -Objekt geladen, und es wird keine neue Instanz erstellt. Wenn innerhalb von drei Minuten kein Aufruf erfolgt, wird das IUpdateNotify-Objekt entladen, und ein neues **IUpdateNotify** -Objekt wird erstellt, wenn der nächste Aufruf erfolgt. 
  
## <a name="click-to-run-installer-com-api-reference-guide"></a>Leitfaden zur com-API-Referenz für Klick-und-Los-Installer

In der folgenden API-Referenzdokumentation:
  
- Parameter befinden sich in einem Schlüssel-Wert-Paar Format, das durch ein Leerzeichengetrennt ist.
    
- Bei den Parametern wird die Groß-/Kleinschreibung nicht beachtet.
    
- Es gibt eine [Liste von Parametern](https://blogs.technet.microsoft.com/odsupport/2014/03/03/the-new-update-now-feature-for-office-2013-click-to-run-for-office365-and-its-associated-command-line-and-switches/) mit verfügbarer Dokumentation. 
    
- Zusammenfassung der IUpdateNotify2-Schnittstelle ist jetzt enthalten.
    
### <a name="apply"></a>Anwenden

```cpp
HRESULT Apply([in] LPWSTR pcwszParameters) // Apply update content.
```

#### <a name="parameters"></a>Parameter

-  _Display Level_: **true** , um den Installationsstatus, einschließlich Fehlern, während des Updateprozesses anzuzeigen; **false** , um den Installationsstatus, einschließlich Fehlern, während des Aktualisierungsvorgangs auszublenden. Der Standardwert ist **false**.
    
-  _forceappshutdown_: **true** , um zu erzwingen, dass Office-Anwendungen sofort heruntergefahren werden, wenn die **Apply** -Aktion ausgelöst wird; **false** , wenn ein Fehler auftritt, wenn Office-Anwendungen ausgeführt werden. Der Standardwert ist **false**. Weitere Informationen finden Sie unter [Hinweise](#bk_ApplyRemark) . 
    
  Wenn eine Office-Anwendung ausgeführt wird, wenn die **Apply** -Aktion ausgelöst wird, tritt in der Regel die **Apply** -Aktion nicht mehr auf. Die Übergabe  `forceappshutdown=true` an die **Apply** -Methode führt dazu, dass der **OfficeClickToRun** -Dienst die Anwendungen sofort herunterfährt und das Update anwendet. Der Benutzer kann in diesem Fall Datenverlust auftreten. 
    
#### <a name="return-results"></a>Ergebnisse zurückgeben

|||
|:-----|:-----|
|**S_OK** <br/> |Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.  <br/> |
|**E_ACCESSDENIED** <br/> |Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.  <br/> |
|**E_INVALIDARG** <br/> |Ungültige Parameter wurden übergeben.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Die Aktion ist zu diesem Zeitpunkt nicht zulässig. Weitere Informationen finden Sie unter [Hinweise](#bk_ApplyRemark) .  <br/> |

<a name="bk_ApplyRemark"></a>

#### <a name="remarks"></a>Bemerkungen

- Wenn eine Office-Anwendung ausgeführt wird, wenn die **Apply** -Aktion ausgelöst wird, tritt bei der **Apply** -Aktion ein Fehler auf. Die Übergabe  `forceappshutdown=true` an die **Apply** -Methode führt dazu, dass der **OfficeClickToRun** -Dienst sofort alle Office-Anwendungen herunterfährt, die ausgeführt werden und das Update anwenden. Dem Benutzer treten möglicherweise Daten auf, da Sie nicht zum Speichern von Änderungen an geöffneten Dokumenten aufgefordert werden.. 
    
- Diese Aktion kann nur ausgelöst werden, wenn der com-Status einer der folgenden ist: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Wenn Sie die **Apply** -Methode aufrufen, ohne Inhalt zuvor herunterzuladen, wird die **Apply** -Methode den Bericht **erfolgreich ausgeführt** , da Sie festgestellt hat, dass nichts angewendet und der **Apply** -Prozess erfolgreich abgeschlossen wurde. 
    
### <a name="cancel"></a>Abbrechen

```cpp
HRESULT Cancel() // Cancel the download action.
```

#### <a name="return-results"></a>Ergebnisse zurückgeben

|||
|:-----|:-----|
|S_OK  <br/> |Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.  <br/> |
|E_ILLEGAL_METHOD_CALL  <br/> |Die Aktion ist zu diesem Zeitpunkt nicht zulässig. Weitere Informationen finden Sie im Abschnitt " [Hinweise](#bk_CancelRemarks) ".  <br/> |

<a name="bk_CancelRemarks"></a>

#### <a name="remarks"></a>Bemerkungen

- Diese Methode kann nur ausgelöst werden, wenn die com-Status-ID **eDOWNLOAD_WIP**. Es wird versucht, die aktuelle Download Aktion abzubrechen. Der com-Status wechselt in **eDOWNLOAD_CANCELLING** und ändert sich schließlich in **eDOWNLOAD_CANCELED**. Der com-Status gibt **E_ILLEGAL_METHOD_CALL** zurück, wenn Sie zu einem anderen Zeitpunkt ausgelöst wird. 
    
### <a name="download"></a>Herunterladen

```cpp
HRESULT Download([in] LPWSTR pcwszParameters) // Download update content.
```

#### <a name="parameters"></a>Parameter

-  _Display Level_: **true** , um den Installationsstatus, einschließlich Fehlern, während des Updateprozesses anzuzeigen; **false** , um den Installationsstatus, einschließlich Fehlern, während des Aktualisierungsvorgangs auszublenden. Der Standardwert ist **false**.
    
-  _updatebaseurl_: URL zur alternativen Download Quelle.
    
-  _updatetoversion_: die Version, auf der Office aktualisiert werden soll. Definieren Sie diesen Parameter, wenn Sie eine ältere Version als die aktuell installierte Version aktualisieren möchten.
    
-  _downloadsource_: CLSID der angepassten **IBackgroundCopyManager** -Implementierung (Bits-Manager). 
    
-  _Content_-Kennung: gibt den Inhalt an, der vom Inhaltsserver über den angepassten Bits-Manager heruntergeladen werden soll. Dieser Wert wird über die Bits-Schnittstelle zur Interpretation übergeben.
    
#### <a name="return-results"></a>Ergebnisse zurückgeben

|||
|:-----|:-----|
|**S_OK** <br/> |Aktion wurde erfolgreich an den Klick-und-Los-Dienst zur Ausführung übermittelt.  <br/> |
|**E_ACCESSDENIED** <br/> |Der Aufrufer wird nicht mit erhöhten Rechten ausgeführt.  <br/> |
|**E_INVALIDARG** <br/> |Ungültige Parameter wurden übergeben.  <br/> |
|**E_ILLEGAL_METHOD_CALL** <br/> |Die Aktion ist zu diesem Zeitpunkt nicht zulässig. Weitere Informationen finden Sie unter [Hinweise](#bk_DownloadRemark) .  <br/> |

<a name="bk_DownloadRemark"></a>

#### <a name="remarks"></a>Bemerkungen

- Sie müssen  _downloadsource_ und  _Content_ -Nr als Paar angeben. Wenn dies nicht der Fall ist, gibt die **Download** -Methode einen **E_INVALIDARG** Fehler zurück. 
    
- Wenn  _downloadsource_,  _Content_-und  _updatebaseurl_ bereitgestellt werden, wird  _updatebaseurl_ ignoriert. 
    
- Diese Aktion kann nur ausgelöst werden, wenn der com-Status einer der folgenden ist: 
    
  - **eUPDATE_UNKNOWN**
    
  - **eDOWNLOAD_CANCELLED**
    
  - **eDOWNLOAD_FAILED**
    
  - **eDOWNLOAD_SUCCEEDED**
    
  - **eAPPLY_SUCCEEDED**
    
  - **eAPPLY_FAILED**
    
- Wenn Sie die **Apply** -Methode ohne zuvor heruntergeladenen Inhalt aufrufen, wird die **Apply** -Methode den Bericht **erfolgreich ausgeführt** , da Sie festgestellt hat, dass nichts angewendet und der **Apply** -Prozess erfolgreich abgeschlossen wurde. 
    
#### <a name="examples"></a>Beispiele

- So laden Sie den Inhalt aus dem angepassten Bits-Manager herunter: Rufen Sie die **Download ()** -Funktion auf, indem Sie die folgenden Parameter übergeben: 
    
  ```cpp
  "downloadsource=CLSIDofBITSInterface contentid=BITSServerContentIdentifier"
  ```

- So laden Sie die Inhalte aus dem Office Content Delivery Network (CDN) herunter: Rufen Sie die **Download ()** -Funktion ohne Angabe der Parameter  _downloadsource_,  _contentbar_oder  _updatebaseurl_ . 
    
- So laden Sie die Inhalte von einem benutzerdefinierten Speicherort herunter: Rufen Sie die **Download ()-** Funktion auf, indem Sie den folgenden Parameter übergeben: 
    
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
   
#### <a name="return-results"></a>Ergebnisse zurückgeben

|||
|:-----|:-----|
|**S_OK** <br/> |Die **Status** -Methode gibt immer dieses Ergebnis zurück. Überprüfen Sie die  `UPDATE_STATUS_RESULT` Struktur auf den Status der aktuellen Aktion.  <br/> |
   
#### <a name="remarks"></a>Bemerkungen

- Das Feld Status des  `UPDATE_STATUS_REPORT` enthält den Status der aktuellen Aktion. Einer der folgenden Statuswerte wird zurückgegeben: 
    
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

- Wenn der letzte Befehl zu einem Fehler geführt hat, enthält das Feld Error des-Fehlers  `UPDATE_STATUS_REPORT` detaillierte Informationen zu dem Fehler. Zwei Arten von Fehlercodes werden von der **Status** -Methode zurückgegeben. 
    
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

  Wenn der Rückgabefehlercode größer als  `UPDATE_ERROR_CODE::eUNKNOWN` der **HRESULT** -Wert eines fehlgeschlagenen Funktionsaufrufs ist. So extrahieren Sie das HRESULT subtrahieren  `UPDATE_ERROR_CODE::eUNKNOWN` aus dem Wert, der im Feld Error von zurückgegeben wird  `UPDATE_STATUS_REPORT` .
    
  Die vollständige Liste der Status-und Fehlerwerte kann angezeigt werden, indem die in OfficeC2RCom.dll eingebettete **IUpdateNotify** -Typbibliothek überprüft wird. 
    
- Das Feld "Content-Nr" wird für Aufrufe von **Status** verwendet, nachdem der **Download** initiiert wurde, und gibt die Inhalts-Nr zurück, die an den **Download** Aufruf übergeben wurde. Es wird empfohlen, dieses Feld vor dem Aufrufen der **Status** -Methode auf **null** zu initialisieren und anschließend den Wert nach dem Zurückgeben des **Status** zu überprüfen. Wenn der Wert immer noch **null**ist, bedeutet dies, dass keine Inhalts-Nr vorhanden ist, die zurückgegeben werden soll. Wenn der Wert nicht **null**ist, müssen Sie ihn mit einem Aufruf von **sysfree String ()** freigeben. Im folgenden finden Sie einen Codeausschnitt zum Aufrufen des **Status** nach dem **Download**.
    
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

In Version [16.0.8208.6352] wurde eine neue **IUpdateNotify2** -Schnittstelle hinzugefügt. 
  
- CLSID_UpdateNotifyObject2, {52C2F9C2-F1AC-4021-BF50-756A5FA8DDFE}
    
- Diese Schnittstelle hat auch die ursprüngliche IUpdateNotify-Schnittstelle gehostet, um Abwärtskompatibilität zu gewährleisten. Das heißt, wenn Sie diese Schnittstelle verwenden, haben Sie Zugriff auf alle Methoden, die in der **UpdateNotifyObject** -Schnittstelle bereitgestellt werden. 
    
- Neue Methoden zu IUpdateNotify2 hinzugefügt:
    
  - **HRESULT** GetBlockingApps (BSTR \* -appsliste). Updates blockieren apps-Liste abrufen. Bei diesem Aufruf werden ausgeführte Office-Apps zurückgegeben, wodurch der Aktualisierungsprozess blockiert wird. 
    
  - **HRESULT** GetOfficeDeploymentData ([in] int DataType, [in] **ein LPCWSTR** pcwszName, [out] BSTR * OfficeData). Abrufen von Office-Bereitstellungsdaten 
    
- Wenn Sie die neuen Methoden verwenden möchten, müssen Sie Folgendes sicherstellen:
    
  - Ihre C2R-Version ist neuer als der obige Build ( \> = June Fork Build).
    
  - Verwenden Sie UpdateNotifyObject2 anstelle von **UpdateNotifyObject** , um **CoCreateInstance**aufzurufen.
    
Wenn Sie keine der neuen Methoden verwenden, müssen Sie nichts ändern. Alle vorhandenen Methoden funktionieren genauso genau wie zuvor.
  
## <a name="implementing-the-bits-interface"></a>Implementieren der Bits-Schnittstelle

Der [intelligente Hintergrundübertragungsdienst (Background Intelligent Transfer Service](https://docs.microsoft.com/windows/win32/bits/background-intelligent-transfer-service-portal) , Bits) ist ein von Microsoft bereitgestellter Dienst zum Übertragen von Dateien zwischen einem Client und einem Server. Bits ist einer der Kanäle, die von einem Office-Klick-und-Los-Installationsprogramm zum Herunterladen von Inhalten verwendet werden können. Standardmäßig verwendet das Click-to-Run-Installationsprogramm von Microsoft 365 Apps die in der Implementierung von Bits integrierte Windows-Datei, um den Inhalt aus dem CDN herunterzuladen. 
  
Durch die Bereitstellung einer angepassten Bits-Implementierung für die **Download ()** -Methode der **IUpdateNotify** -Schnittstelle kann Ihre Verwaltbarkeit-Software steuern, wo und wie der Client den Inhalt herunterlädt. Eine angepasste Bits-Schnittstelle ist nützlich, wenn ein benutzerdefinierter Inhalts Verteilungskanal als die integrierten Klick-und-Los-Kanäle bereitgestellt wird, beispielsweise die CDN-, IIS-Server oder Dateifreigaben. 
  
Die Mindestanforderung für eine angepasste Bits-Schnittstelle für die Verwendung des Office C2R-Diensts lautet:
  
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

- Für die  `Addfile` -und-  `AddFileWithRanges` Funktionen hat die Remote-URL folgendes Format: 
    
  ```cpp
  cmbits://<contentid>/<relative path to target file>
  ```

  - cmbits ist hart codiert und steht für angepasste Bits.
    
  -  _\<contentid\>_ ist der  _Inhaltstyp_ -Parameter für die **Download ()** -Methode. 
    
  -  _\<relative path to target file\>_ Gibt den Speicherort und den Dateinamen der herunterzuladenden Datei an. 
    
    Wenn Sie beispielsweise eine  _Inhalts_ -Nr für  `f732af58-5d86-4299-abe9-7595c35136ef` die **Download ()** -Methode bereitgestellt haben und Office C2R die Version der CAB-Datei (beispielsweise Datei) herunterladen möchte,  `v32.cab` wird **AddFile ()** mit folgendem Aufruf aufgerufen  `RemoteUrl` :
    
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

IT-Administratoren können festlegen, dass Desktop Clients automatisch Updates erhalten, wenn Sie direkt im CDN zur Verfügung stehen, oder Sie können auswählen, ob die Bereitstellung von Updates gesteuert werden soll, die über die Update Kanäle mit dem Office-Bereitstellungs Tool oder dem Microsoft Endpoint Configuration Manager zur Verfügung stehen.
  
Der Dienst unterstützt die Möglichkeit für Verwaltungstools, den Download der Inhalte zu erkennen und zu automatisieren, wenn Updates zur Verfügung gestellt werden.
  
**Die folgende Abbildung ist eine Übersicht über das Herunterladen eines benutzerdefinierten Bilds.**

![A diagram of using the COM interface on  the Office Click-To-Run installer.](media/e7ac2523-e67b-4a44-ae67-c048709f872a.png "Ein Diagramm zur Verwendung der COM-Schnittstelle im Office-Klick-und-Los-Installationsprogramm")
  
### <a name="overview-of-downloading-a-custom-image"></a>Übersicht über das Herunterladen eines benutzerdefinierten Bilds
  
Im vorherigen Diagramm sehen Sie, dass ein neues Microsoft 365-apps-Bild im CDN zur Verfügung steht. Zusammen mit dem Microsoft 365-apps-Image steht eine API zur Verfügung, die die erforderlichen Informationen zum Aktivieren der Verwaltungssoftware zum direkten erstellen angepasster Bilder enthält, die die Verwendung des Office-Bereitstellungstools ersetzen.

Ein Unternehmen konfiguriert seine WSUS so, dass die Microsoft 365-apps-Updates synchronisiert werden. Diese Updates enthalten nicht die tatsächliche Bild Nutzlast, aber die Verwaltungssoftware kann erkennen, wenn neue Inhalte verfügbar sind. Die Verwaltbarkeit-Software kann dann die Microsoft 365 apps Update-Metadaten lesen, um zu verstehen, für welche Version von Office das Update gilt.

Wenn das Update anwendbar ist, kann die Verwaltbarkeit-Software den CDN-Inhalt und die Dateiliste verwenden, um das benutzerdefinierte Abbild zu erstellen und es auf dem Dateifreigabespeicherort zu speichern, der für die Verwendung konfiguriert ist.
  
### <a name="using-the-microsoft-365-apps-file-list-api"></a>Verwenden der API für Dateilisten von Microsoft 365-apps

Die Dateilisten-API von Microsoft 365 apps dient zum Abrufen der Namen der Dateien, die für ein bestimmtes Microsoft 365-apps-Update benötigt werden.

HTTP-Anforderung

GET https://config.office.com/api/filelist

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

Optionale Abfrageparameter

|**Name**|**Beschreibung**|
|:-----|:-----|
| channel <br/>| Gibt den Kanalnamen an.  <br/> Optional – standardmäßig auf ' Halbjahresbericht ' <br/> Unterstützte Werte https://docs.microsoft.com/DeployOffice/office-deployment-tool-configuration-options#channel-attribute-part-of-add-element |
| Version <br/>| Gibt die Update Version an. <br/> Optional – Standardwert ist die neueste Version, die für den angegebenen Kanal verfügbar ist. |
| Bogen <br/>| Gibt die Clientarchitektur an. <br/> Optional – standardmäßig "x64" <br/> Unterstützte Werte: x64, x86 |
| lid <br/>| Gibt die Sprachdateien an, die eingeschlossen werden sollen. <br/> Optional – Standardwert: None <br/> Um mehrere Sprachen anzugeben, schließen Sie einen Lid-Abfrageparameter für jede Sprache ein. <br/> Verwenden Sie das Format für die Sprachen-ID, ex. "en-US", "fr-FR" |
| AllLanguages <br/>| Gibt an, dass alle Sprachdateien eingeschlossen werden sollen. <br/> Optional – Standardwert ist false |

HTTP-Antwort

Wenn die Methode erfolgreich verläuft, werden der Antwortcode 200 OK und eine Sammlung von File-Objekten im Antworttext zurückgegeben.

Führen Sie die folgenden Schritte aus, um ein Bild zu erstellen:
1.  Rufen Sie die API auf, und stellen Sie die entsprechenden Abfrageparameter für den Kanal, die Version und die Architektur des Updates bereit, das Sie interessieren.
Hinweis: Dateiobjekte mit dem Attribut "LCID": "0" sind sprachneutrale Dateien und müssen in das Bild aufgenommen werden.
2.  Erstellen Sie ein lokales Image des CDN, indem Sie die File-Objekte durchlaufen und die CDN-Dateien kopieren, während Sie die Ordnerstruktur entsprechend dem Attribut "relativePath" erstellen, das für die einzelnen Dateiobjekte definiert wurde.

Im folgenden Beispiel wird die Dateiliste für den aktuellen Kanal und die Version 16.0.4229.1004 für 64bit abgerufen und die Sprachdateien Französisch und Englisch eingeschlossen:

```http
Get https://config.office.com/api/filelist?Channel=Current&Version=16.0.4229.1004&Arch=x64&Lid=fr-fr&Lid=en-US
```

### <a name="hash-verification-of-dat-files"></a>Hash Überprüfung von DAT-Dateien

Bilder Erstellungstools können die Integrität der heruntergeladenen DAT-Dateien überprüfen, indem Sie einen berechneten Hashwert mit dem bereitgestellten Hashwert vergleichen, der den einzelnen DAT-Dateien zugeordnet ist. Es folgt ein Beispiel für ein File-Objekt, das hashLocation-und hashAlgorithm-Werte angibt:
  
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

- Das **hashLocation** -Attribut gibt den relativen Pfadspeicherort der CAB-Datei an, die den Hashwert enthält. Erstellen Sie den Speicherort der Hash Datei, indem Sie URL + relativePath + hashLocation verketten. Im folgenden Beispiel wäre der Speicherort Stream.x64.bg-bg. Hash wie folgt: 
    
  ```http
  https://officecdn.microsoft.com/pr/492350f6-3a01-4f97-b9c0-c7c6ddf67d60/office/data/16.0.4229.1004/s641026.cab/stream.x64.bg-bg.hash 
  ```

- Das Attribut **hashAlgorithm** gibt an, welcher Hashalgorithmus verwendet wurde. 
    
  Um die Integrität der Datei Stream.x64.bg-bg. dat zu überprüfen, öffnen Sie den Stream.x64.bg-bg. Hash und lesen Sie den Hashwert, der die erste Textzeile in der Hash Datei ist. Vergleichen Sie diesen Wert mit dem berechneten Hashwert (mithilfe des angegebenen Hashalgorithmus), um die Integrität der heruntergeladenen DAT-Datei zu überprüfen.
    
  Im folgenden Beispiel wird der C#-Code zum Lesen des Hashs gezeigt.
    
  ```cs
    string[] readHashes = System.IO.File.ReadAllLines(tmpFile, Encoding.Unicode);
    string readHash = readHashes.First();
  ```

### <a name="microsoft-365-apps-updates"></a>Updates für Microsoft 365-apps

Alle Microsoft 365-apps-Updates werden im [Microsoft Update-Katalog](https://www.catalog.update.microsoft.com/Search.aspx?q=office+365+client)veröffentlicht.
  
Microsoft 365 apps-Updates ermöglichen eine verwaltbare Software zur Behandlung von Microsoft 365-apps Updates auf eine Art und Weise, die einem anderen Wu-Update mit einer Ausnahme ähnelt. die Clientupdates enthalten keine tatsächliche Nutzlast. Die Updates für Microsoft 365-apps sollten nicht auf allen Clients installiert werden, sondern verwendet werden, um die Workflows mit der Verwaltungssoftware auszulösen, wobei der Installationsbefehl durch den oben gezeigten com-basierten Installationsmechanismus ersetzt wird.

**In der folgenden Abbildung ist ein Diagramm des Office 365-Client Update Workflows dargestellt.**

![Workflow diagram for O365PP client updates.](media/bc8092b0-62b8-402c-a5c0-04d55cca01d4.png "Workflow Diagramm für O365PP-Clientupdates")
  
Jedes veröffentlichte Microsoft 365-apps-Update enthält Metadaten zum Update. Diese Metadaten enthalten einen Parameter namens MoreInfoUrl, der zum Ableiten des API-Aufrufs an die Dateilisten-API für das jeweilige Update verwendet werden kann.

Im folgenden Beispiel wird die Dateilisten-API in das MoreInfoUrl-Verzeichnis eingebettet und beginnt mit "ServicePath =".

http://go.microsoft.com/fwlink/?LinkId=626090&Ver=16.0.12527.21104&Branch=Insiders&Arch=64&XMLVer=1.6&xmlPath=http://officecdn.microsoft.com/pr/wsus/ofl.cab&xmlFile=O365Client_64bit.xml& ServicePath =https://config.office.com/api/filelist?Channel=Insiders&Version=16.0.12527.21104&Arch=64&AllLanguages=True
  
### <a name="additional-metadata-for-automating-content-staging"></a>Zusätzliche Metadaten zum Automatisieren der Inhaltsbereitstellung

**Versionsverlaufs-API**
  
Die Microsoft 365 apps-Versionsverlaufs-API dient zum Abrufen von Details für jedes der im CDN veröffentlichten Updates zusammen mit den Kanalnamen und anderen Kanal Attributen.

HTTP-Anforderung

```http
GET https://config.office.com/api/filelist/channels 
```

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

HTTP-Antwort

Wenn die Methode erfolgreich verläuft, werden der Antwortcode 200 OK und eine Sammlung von File-Objekten im Antworttext zurückgegeben.

**SKUs-API**
  
Die SKUs-API gibt Informationen zurück, die für die Ermittlung geeignet sind, welche Produkte für die Bereitstellung und Wartung aus dem Office CDN zur Verfügung stehen, zusammen mit verschiedenen Optionen.

HTTP-Anforderung

```http
GET https://config.office.com/api/filelist/skus 
```

Geben Sie für diese Methode keinen Anforderungstext an.

Zum Aufrufen dieser API sind keine Berechtigungen erforderlich.

HTTP-Antwort

Wenn die Methode erfolgreich verläuft, werden der Antwortcode 200 OK und eine Sammlung von File-Objekten im Antworttext zurückgegeben.
