---
title: Verwendung von CSISyncClient zum Steuern der Office-Dokument-Cache (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Erfahren Sie, wie CSISyncClient verwenden, um die Office-Dokument-Cache (ODC) zu steuern.
ms.openlocfilehash: 908442bdc4e02f8268b9af877921da45a64ab197
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565284"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Verwendung von CSISyncClient zum Steuern der Office-Dokument-Cache (ODC)

Erfahren Sie, wie CSISyncClient verwenden, um die Office-Dokument-Cache (ODC) zu steuern.
  
CSISyncClient ist ein Out-of-Proc-COM-Server (CsiSyncClient.exe), der Microsoft-OneDrive zum Steuern des Verhaltens der Office Dokument Cache (ODC) ermöglicht. Zum Beispiel OneDrive rufen möglicherweise die ODC über CSISyncClient hoch-und Herunterladen von Dateien zu und von Endpunkten MS-FSSHTTP aktiviert. Auf diese Weise können die erweiterte Service-Backup-Funktionen in Office, wie gemeinsame dokumenterstellung und nahtlose Übergänge von offline zu online.
  
CsiSyncClient ist im Office-Desktop (X86 und X64) verfügbar. Hinweis: Während neuere Versionen von Office mit CsiSyncClient liefern können, wird der Prozess nur für Abwärtskompatibilität verwendet werden. Die CsiSyncClient-Schnittstelle und die Methodik zum Steuern der ODC werden in zukünftigen Versionen von Office ändern.
  
Die Klassen-ID ist derzeit nur auf OneDrive reagieren festgelegt.
  
Das COM-Objekt kann als Out-of-Proc-com-Server verwendet werden und führt im CsiSyncClient.exe. Aufgrund von Einschränkungen mit Access (mit dem die ODC) mit der Bit-Typ, der in diesem Fall X64 Office kommt Office bedeutet, ein X64 dass wunderbare COM-Objekt oder X86 Office bedeutet, dass ein X86 COM-Objekt. Mit dieser Einschränkung CLSCTX_LOCAL_SERVER angeben, wie Teil der CoCreateInstance das COM-Objekt als ein Out-of-Proc-com-Server verschoben, sodass Cross-Bitness Kompatibilität gehostet werden.
  
## <a name="interfaces"></a>Schnittstellen

CSISyncClient verwendet die folgenden Schnittstellen.
  
### <a name="interface-ilsclocalsyncclient"></a>Schnittstelle ILSCLocalSyncClient

Dies ist die primäre Schnittstelle verwendet, um Dateien in Office zu synchronisieren.
  
- ProgID: Office.LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- Der Typbibliothek: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
Das COM-Objekt, das verfügbar gemacht wird, wird als Out-of-Proc-Server verwendet. Angeben von CLSCTX_LOCAL_SERVER als Teil des CoCreateInstance ermöglicht Kompatibilität zwischen 64-Bit- und 32-Bit-Prozessen.
  
Nachdem Sie das COM-Objekt gemeinsam erstellt haben, müssen Sie zuerst [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) aufrufen. Sobald [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgreich abgeschlossen wurde, können Sie eine beliebige API so oft wie gewünscht und in beliebiger Reihenfolge aufrufen. Sie können auch [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) für ein bereits initialisiertes Objekt aufrufen, aber dies hat keine Auswirkung. 
  
Ausnahmen zu den vorherigen Absatz sind [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) und [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Nach dem Aufruf von [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) auf das COM-Objekt müssen Sie dieses Objekt löschen und erstellen Sie einen neuen Anwendungspool. [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) wird Ihre Subcache löschen, löschen alle zugehörigen Dateiinformationen im Cache, doch lassen Sie die Dokumente auf dem Datenträger. Es intakt auch den Status für die Kommunikation mit dem Cache. Dadurch können Sie zum Aufrufen der [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erneut aus, um einen neuen Cache ohne zerstören und das COM-Objekt neu erstellen. 
  
**Öffentliche Member-Funktionen**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::DeleteFile

DeleteFile wird verwendet, um die Dateiinformationen aus dem Cache zu entfernen. Diese Methode wird jedoch die zugehörige Datei auf der Festplatte und auf dem Server lassen.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Die Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert muss eine nicht leere mit bis zu 128 Zeichen. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Der angegebene ResourceID ist nicht im Cache.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Die Initialisierung wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die Datei wird derzeit synchronisiert oder geöffnet und kann nicht gelöscht werden.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges gibt einen Enumerator von ILSCEvent-Objekten und auch gibt ein Token, das auf den nächsten Aufruf von GetChanges, vorausgesetzt, dass der Consumer verarbeitet wurden, die vorherige Gruppe von Ereignissen erfolgt ist. Ereignisse vor dem _nPreviousChangesToken_ angegeben werden gelöscht und nicht verfügbar. Wenn es keine Ereignisse sind verarbeitet werden, _PnCurrentChangesToken_ sollte den gleichen Wert wie _nPreviousChangesToken_sein, sondern _PpiEvents_ wird weiterhin festgelegt werden. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parameter

 _nPreviousChangesToken_
  
Gibt an, welches Ereignis zuletzt vom Consumer verarbeitet wurde. 
  
 _pnCurrentChangesToken_
  
Gibt das letzte Ereignis an Consumer übergeben wird. Darf nicht null sein.
  
 _ppiEvents_
  
Ein Enumerator für die Ereignisse, die an die Consumer übergeben. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission wird verwendet, um abzufragen, ob die Synchronisierung des Office-Heuristik für Netzwerk-Kosten und Stromverbrauchs außer Kraft gesetzt werden. Auf einer 3G oder ein anderes Netzwerk hohe Kosten oder bei der Ausführung auf Batterie im Vergleich zu eingesteckt wird, können Office bis zu einem Zeitpunkt mehr angebracht Netzwerkverkehr zu blockieren.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parameter

 _nspType_
  
Ein Flag, das welche Kosten heuristische zur Abfrage definiert. Finden Sie unter [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Gibt an, ob die angeforderte Kosten Heuristik derzeit überschrieben wird. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus wird verwendet, um das Sammeln von Informationen für eine bestimmte Datei:, ob im Cache vorhanden ist, hat ausstehende Kommunikation mit der Kopie auf dem Server und Office 2013 den aktuellsten Datumsdaten aus der lokalen Kopie hat. Es erfordert eine bitweise Kennzeichnung von [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) Werten, welche Informationen bestimmen die CsiSyncClient COM-Objekt für Abfragen. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Die Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss nicht leer ist, mit bis zu 128 Zeichen sein. 
  
 _sfRequestedStatus_
  
Ein Flag das definiert, welche Informationen zurückgeben. Finden Sie unter [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
Die Zeichenfolge, die den Speicherort der Datei _BstrResourceID_ auf dem Client identifizierten angibt. Darf nicht null sein. 
  
 _pbstrETag_
  
Eine Zeichenfolge, die das eTag für die Datei _BstrResourceID_identifizierten enthalten wird. Darf nicht null sein. 
  
 _psfFileStatus_
  
Ein Flag, das den Status über _SfRequestedStatus_ für die Datei _BstrResourceID_identifizierten angefordert enthalten wird. Darf nicht null sein. Finden Sie unter [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Dateiinformationen durch _BstrResourceID_ angegeben ist im Cache nicht vorhanden.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged angefordert wurde oder durch _BstrResourceID_ angegebene Datei ist gesperrt oder fehlt.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions gibt eine Liste der senkrechte Striche getrennte Dateierweiterungen, die derzeit von der CsiSyncClient COM-Objekt unterstützt werden. Beachten Sie, dass dieser Liste kann sich ändern, und der Consumer über eine Änderung über das IPartnerActivityCallback-Objekt, das auf [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (finden Sie unter EventOccured) bereitgestellt benachrichtigt. 
  
Ein Beispiel für die Zeichenfolge zurückgegeben wird wie folgt: "| Docx | Docm | Pptx |"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parameter

 _pbstrSupportedFileExtensions_
  
Eine Zeichenfolge mit einer senkrechte Striche getrennte Dateierweiterungen unterstützt das CsiSyncClient COM-Objekt festgelegt werden soll. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize muss die erste Methode aufgerufen. Andernfalls wird allen anderen APIs E_LSC_NOTINITIALIZED zurückgegeben. Initialize für ein bereits initialisiertes Objekt aufrufen, gibt S_OK zurück und hat keine Auswirkung. Wenn E_LSC_CACHEMISMATCH zurückgegeben wird, kann der Aufrufer [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) zum Löschen des Caches mit der angegebenen SuppliedID verknüpften aufrufen. Allerdings werden in diesem Fall andere APIs weiterhin E_LSC_NOTINITIALIZED zurück. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parameter

 _bstrSuppliedID_
  
Identifiziert die Consumer und der cache verwendet. Muss nicht leeren mit bis zu 32 Zeichen. 
  
 _bstrProgID_
  
Identifiziert die Consumer COM-Objekt für die bidirektionale Kommunikation. Muss nicht leeren mit maximal 39 Zeichen. Finden Sie unter [ \<ProgID\> Schlüssel](https://docs.microsoft.com/en-us/windows/desktop/com/-progid--key) Weitere Informationen zu ProgIDs. 
  
 _bstrFileSystemDirectoryHint_
  
Gibt das Stammverzeichnis an, in dem lokale Dateien gespeichert werden sollen. Muss nicht leeren mit maximal 256 Zeichen. Das Verzeichnis muss bereits vorhanden sein. 
  
 _pEventCallback_
  
Das Callback-Schnittstelle die CsiSyncClient auf Änderungen informiert wird. Finden Sie unter IPartnerActivityCallback::EventOccurred. Dieser Wert darf nicht null sein. 
  
 _pfCreatedNewCache_
  
Gibt zurück, ob ein neuer Cache erstellt wurde. Wenn kein Cache mit der SuppliedID verknüpft ist, wird eine erstellt. Dieser Wert darf nicht null sein.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Eine SuppliedID bereits einen mit ihm verbundenen Cache hat, jedoch eine unterschiedliche ProgId oder FileSystemDirectoryHint als bereitgestellten.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |Die FileSystemDirectoryHint (oder einen Unterordner) auf einem anderen Cache bereits vorhanden ist.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |Die ProgID auf einem anderen Cache ist bereits vorhanden.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange wird verwendet, um das CsiSyncClient COM-Objekt zu versuchen, die angegebene Datei hochladen zu informieren. Die Methode wird die Datei für den Upload, lesen die aktuellen Inhalt der Datei einschließlich vorbereiten. Wenn ein Upload noch aussteht, vorherigen Uploads werden verworfen, und den neuen Inhalt für die vorbereitet hochladen. Wenn die Datei zur Bearbeitung in einer Anwendung geöffnet ist, gibt diese Methode S_OK zurück, ohne zuvor die Datei für den Upload (die Anwendung sollte bereits diesen Schritt tun, wenn Änderungen vorhanden sind).
  
Diese Methode ermöglicht Uploads Wenn sie als markiert wurde hochgeladen blockierte zuvor (siehe [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

 _bstrFileSystemPath_
  
Eine Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss eine nicht leere lokaler Pfad mit maximal 256 Zeichen sein. In diesem Pfad muss in der Verzeichnisstruktur durch die FileSystemDirectoryHint angegeben wird, wenn der Aufruf von [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) vorgenommen wurde. 
  
 _bstrResourceID_
  
Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert muss eine nicht leere mit bis zu 128 Zeichen. 
  
 _bstrWebPath_
  
Eine Zeichenfolge, die die Datei auf dem Server identifiziert. Dieser Wert muss nicht leeren, gültige URL, aber nicht mehr als INTERNET_MAX_URL_LENGTH, durch die definierten http://support.microsoft.com/kb/208427. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Durch _BstrFileSystemPath_ angegebene Datei hat einen anderen ResourceID als angegeben. Wenn dieser Fehler zurückgegeben wird, wird ein Ereignis vom Typ LSCEventType_OnFilePathConflict gesendet. Finden Sie unter [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Datei wurde gelöschten Mid-Vorgang.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Die angegebene Dateierweiterung wird durch das CsiSyncClient COM-Objekt nicht unterstützt. Finden Sie unter [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |Das COM-Objekt keinen Upload planen, weil der Datei im Cache der letzten Änderung vom Datenträger waren.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Durch _BstrFileSystemPath_ angegebene Datei ist nicht vorhanden oder gesperrt.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath ist nicht unter dem Stammverzeichnis, durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Durch _BstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei bereits hat ausstehende Änderungen in einem anderen Cache und kann nicht noch die Consumer Cache zugeordnet werden.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Die bereitgestellten WebPath fällt unter einem anderen Cache.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile wird eine neue URL und den lokalen Pfad für einen bestimmten ResourceID zuordnen. Wenn die Datei mit der ResourceID angegebenen im Cache nicht bereits vorhanden ist, wird ein Versuch unternommen werden, erstellen und für den Download markieren.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert muss eine nicht leere mit bis zu 128 Zeichen. 
  
 _bstrNewFileSystemPath_
  
Eine Zeichenfolge, die den neuen lokalen Pfad für die Datei angibt. Dieser Wert muss eine nicht leere lokaler Pfad mit maximal 256 Zeichen sein. In diesem Pfad muss in der Verzeichnisstruktur durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde. 
  
 _bstrNewWebPath_
  
Eine Zeichenfolge, die die neue URL für die Datei angibt. Dieser Wert muss nicht leeren gültige URL, aber nicht mehr als INTERNET_MAX_URL_LENGTH, durch die definierten http://support.microsoft.com/kb/208427. 
  
 _fBlockUploads_
  
Gibt an, ob Uploads am neuen Speicherort derzeit zulässig sind. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Die _BstrNewFileSystemPath_ oder _BstrNewWebPath_ bereits vorhanden sind auf eine andere Datei in einem Cache. Wenn dieser Fehler zurückgegeben wird, wird ein Ereignis vom Typ LSCEventType_OnFilePathConflict gesendet. Finden Sie unter [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Dateiinformationen wurde aus dem Cache gelöscht, während diese Methode ausgeführt wurde.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath ist nicht unter dem Stammverzeichnis, durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei wird in einer Office-Anwendung derzeit synchronisiert.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache löscht den Cache der SuppliedID, die auf Initialize bereitgestellt wurde zugeordnet. Dies umfasst alle Dateiinformationen, aber verlassen die Dateien auf dem Client und dem Server. Diese Methode bewirkt, dass auch das Objekt eine teilweise nicht initialisiert. Der einzige gültige Anrufe nach Dies sind [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) oder [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Diese Methode kann aufgerufen werden, wenn Initialize schlägt fehl und E_LSC_CACHEMISMATCH gibt, und löscht den Cache der SuppliedID, die mit der fehlerhaften Anruf bereitgestellt wurde zugeordnet.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parameter

Keine
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht erfolgreich in der Vergangenheit aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange weist das CsiSyncClient COM-Objekt die angegebene Datei für den Download markieren. Wenn die Datei in einer Office-Anwendung für die Bearbeitung geöffnet ist, gibt diese Methode S_OK zurück, ohne markieren die Datei zum Herunterladen (die Anwendung sollte bereits diesen Schritt tun, wenn Änderungen vorhanden sind).
  
Diese Methode ermöglicht, Downloads, wenn er als markiert wurde downloads blockierte zuvor (Siehe RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Eine Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss eine nicht leere lokaler Pfad mit maximal 256 Zeichen sein. In diesem Pfad muss in der Verzeichnisstruktur durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.  <br/> |
|bstrResourceID  <br/> |Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert muss eine nicht leere mit bis zu 128 Zeichen.  <br/> |
|bstrWebPath  <br/> |Eine Zeichenfolge, die die Datei auf dem Server identifiziert. Dieser Wert muss eine gültige URL nicht leer, wird jedoch nicht mehr als INTERNET_MAX_URL_LENGTH, durch die definierten http://support.microsoft.com/kb/208427.  <br/> |
   
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler bei der Cache Connectivity Zustand festgelegt.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Durch _BstrFileSystemPath_ angegebene Datei hat einen anderen ResourceID als angegeben.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Die angegebene Dateierweiterung wird durch das CsiSyncClient COM-Objekt nicht unterstützt. Finden Sie unter GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Datei wurde in Mid Vorgang gelöscht.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath ist nicht unter dem Stammverzeichnis, durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Durch _BstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei bereits ausstehende Änderungen in einem anderen Cache wurde und nicht noch die Consumer Cache zugeordnet sein.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Die bereitgestellten WebPath fällt unter einem anderen Cache.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Wird der Cache in einem Zustand online oder offline. Wenn offline, versucht Office nicht mit dem Server für alle Dateien in diesem Cache, unabhängig von der Einstellung für jede einzelne Datei _fBlockUploads_ kommunizieren. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parameter

 _fIsOnline_
  
Ermitteln des Status der Konnektivität des Caches ein boolescher Wert. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler bei der Cache Connectivity Zustand festgelegt.  <br/> |
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission wird verwendet, um entweder Override oder des RestoreOffice synchronisieren Heuristik für Netzwerk Verwendung Kosten und Leistung. Auf einer 3G oder ein anderes Netzwerk hohe Kosten oder bei der Ausführung auf Batterie im Vergleich zu eingesteckt wird, können Office bis zu einem Zeitpunkt mehr angebracht Netzwerkverkehr zu blockieren. Consumer dieser API können sie außer Kraft setzen des Office-Heuristik und erzwingen die Synchronisierung erfolgen.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parameter

 _nspType_
  
Ein Kennzeichen, die definiert, welche Kosten heuristische außer Kraft gesetzt. Finden Sie unter [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Gibt an, ob So erzwingen Sie synchronisieren auf, daher Überschreiben dieser Kosten heuristische, oder es nicht mehr zu überschreiben. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Synchronisieren von Heuristik außer Kraft gesetzt.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Entlädt den Cache aus dem COM-Objekt und schließende Tag vom Typ Vorgänge ausführen. [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUSS vor dem Löschen des COM-Objekts aufgerufen werden. Nach dem Aufrufen keine anderen APIs aufgerufen werden kann, muss das COM-Objekt gelöscht werden, und eine neue erstellt wird, wenn Vorgänge fortgesetzt werden soll. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parameter

Keine.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Initialisieren.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Schnittstelle IEnumLSCEvent

Diese Schnittstelle stellt eine Liste der ILSCEvent Ereignisse.
  
**Öffentliche Member-Funktionen**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Ruft das nächste Ereignis aus der Liste der Ereignisse.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Parameter

 _ppiLSCEvent_
  
Ein Zeiger auf eine ILSCEvent-Schnittstelle.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Es sind keine weiteren Ereignisse.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Setzt den Enumerator auf das erste Ereignis zurück.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parameter

Keine.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
### <a name="interface-ilscevent"></a>Schnittstelle ILSCEvent

Diese Schnittstelle stellt ein Ereignis synchronisieren. Alle Informationen über das Ereignis kann über die Benutzeroberfläche abgerufen werden.
  
**Öffentliche Member-Funktionen**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Beachten Sie, dass dieser Wert [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) aufgerufen wird nicht, wenn das Ereignis erstellt wurde, damit Sie nur verfügen, werden den aktuellen Status der Datei, die nicht den Status der Datei ein, wenn der Status Konflikt geändert, aufgefüllt wird. 
  
Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnLocalConflictStateChanged ist. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parameter

 _pfIsInConflict_
  
Der aktuelle Konflikt Status der Datei mit dem Ereignis verknüpft ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parameter

 _pnError_
  
Der Fehler, die mit diesem Ereignis verknüpft ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parameter

 _pbstrETag_
  
Das ETag mit diesem Ereignis verknüpft ist
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Ruft den Typ für dieses Ereignis ab.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parameter

 _pnEventType_
  
Den Ereignistyp dieses Ereignisses. Gültige Werte finden Sie unter [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) . Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Ruft den lokalen Arbeitspfad für dieses Ereignis ab.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parameter

 _pbstrLocalWorkingPath_
  
Der lokale Pfad der Datei auf der dieses Ereignis bezieht. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Ruft die Ressourcen-ID für das Ereignis ab.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parameter

 _pbstrResourceID_
  
Die ResourceID der Datei mit diesem Ereignis verknüpft ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist. Wenn Sie ein Anruf an [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) einen Konflikt Web oder lokalen Pfad durch eine andere Datei in den Cache für den Office-Dateien, würde dies Ereignis wird generiert. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parameter

 _pbstrResourceIDAttempted_
  
Die ResourceID, das dieses Ereignis generiert werden. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parameter

 _pnSyncErrorType_
  
Den Fehlertyp mit diesem Ereignis verknüpft ist. Mögliche Werte finden Sie unter [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) . Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_INVALIDARG  <br/> |Ein oder mehrere Parameter sind ungültig.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parameter

 _pbstrWebPath_
  
Gibt den Web-Pfad dieses Ereignis zugeordnet. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
### <a name="interface-ilscevent2"></a>Schnittstelle ILSCEvent2

Diese Schnittstelle enthält zusätzliche Informationen zu einem Ereignis synchronisieren.
  
**Öffentliche Member-Funktionen**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Ruft die Kette Fehlerinformationen zu einem Synchronisieren von Ereignis ab.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parameter

 _pbstrErrorChain_
  
Eine Zeichenfolge, die die Fehlerinformationen Kette enthalten soll. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_NOTIMPL  <br/> |Die installierte Version von Office wird diese Schnittstelle nicht unterstützt.  <br/> |
|E_INVALIDARG  <br/> |Eine oder mehrere der Werte für Parameter sind ungültig.  <br/> |
|E_FAIL  <br/> |Die Fehlerinformationen Kette ist nicht verfügbar.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Schnittstelle IPartnerActivityCallback

Diese Schnittstelle stellt eine Rückruffunktion, die das CSISyncClient COM-Objekt.
  
**Öffentliche Member-Funktionen**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Dies ist eine Rückruffunktion für das Objekt, das CsiSyncClient COM-Objekt zugewiesen. Es wird erwartet, dass beim Eintreten Ereignisses dieses (Gültige Ereignistypen finden Sie unter [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) ) CsiSyncClient COM-Objekt dieser Methode, den Consumer Signalisierung aufgerufen wird. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parameter

 _eEventTypeOccurred_
  
Den Ereignistyp dieses Ereignisses. Gültige Werte finden Sie unter [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) . 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück.
  
## <a name="enumerations"></a>Enumerationen

CSISyncClient verwendet die folgenden Aufzählungen.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Diese Enumeration gibt die Kategorien von Fehlern, die beim Synchronisieren einer Datei auftreten können.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |Synchronisieren von Fehlers dieses Ereignisses wurde unerwartet und besondere Aufmerksamkeit erfordern. Der Benutzer möglicherweise eingreifen.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |Der Synchronisierung von Fehler dieses Ereignisses braucht nicht besonders beachtet. Office wird es automatisch behandelt werden.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |Der Synchronisierung von Fehler dieses Ereignisses bewirkt, dass einen Benutzer Behebung. Fehler beim Zusammenführen der Konflikt muss beispielsweise ein Benutzer öffnen Sie das Dokument und zusammenführen.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |Der Synchronisierung von Fehler dieses Ereignisses erfordert den Consumer eingreifen, aber nicht besonders beachtet durch den Benutzer erforderlich sein soll.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |Der Synchronisierung Fehler dieses Ereignisses erfordert den Consumer als Sonderfall eingreifen.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enum LSCEventType
<a name="Enum_LSCEventType"> </a>

Diese Enumeration gibt die Art der Ereignisse, die für eine bestimmte Datei auftreten können.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Änderungen wurden in einer lokalen Datei vorgenommen.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Ein Benutzer eine Datei geöffnet wurde.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Herunterladen der Datei Änderungen vom Server ist beendet.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Beendet die Datei Änderungen an den Server hochladen.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |Der Zusammenführung Konflikt Status einer Datei wurde geändert.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Eine Datei wurde hinzugefügt.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Eine Datei wurde gelöscht.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Synchronisieren von wurde für Dateien des Benutzers aktiviert.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Download von Änderungen vom Server gestartet.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Schritte Hochladen der Datei Änderungen an den Server.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Dieses Ereignis wird generiert, wenn ein Aufruf von [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) führt zu einem Konflikt Web oder lokalen Pfad durch eine andere Datei in der Zwischenspeicher für Office-Datei.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Diese Enumeration gibt die Art der Ereignisse, die auftreten können. Consumer muss bestimmte basierte auf den Ereignistyp ILSCLocalSyncClient-Funktionen aufrufen.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Ein ILSCEvent ist aufgetreten. Consumer sollte [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) zum Abrufen der Daten aufrufen.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Die unterstützten Dateierweiterungen wurden geändert. Consumer sollte [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) zum Abrufen der neuen Liste mit unterstützten Erweiterungen aufrufen.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Diese Enumeration gibt die Kennzeichen für ein Netzwerk Kosten heuristische verwendet. 

|Enumerator|Beschreibung|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True, wenn die Heuristik Kosten für teuren Netzwerke (z. B. 3 G) überschrieben wird.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True, wenn die Heuristik Kosten für die Verwendung von Power (beispielsweise eine Batterie) überschrieben wird.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Diese Enumeration wird den Status Synchronisieren einer Datei darstellen. 
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True, wenn es an die Server-Datei zu sendenden Daten steht.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True, wenn es ausstehende Daten aus der Serverdatei herunterladen.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True, wenn die Daten für die Datei im Cache befindet ist die aktuellste Kopie der Daten auf dem Datenträger.  <br/> |
   

