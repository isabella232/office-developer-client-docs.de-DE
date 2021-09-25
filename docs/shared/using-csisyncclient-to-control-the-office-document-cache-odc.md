---
title: Verwenden von CSISyncClient zum Steuern des Office Dokumentcaches (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Erfahren Sie, wie Sie CSISyncClient verwenden, um den Office Dokumentcache (ODC) zu steuern.
ms.openlocfilehash: 1ad8c752e573eab894be675a2b0e790d560f4002
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59560200"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Verwenden von CSISyncClient zum Steuern des Office Dokumentcaches (ODC)

Erfahren Sie, wie Sie CSISyncClient verwenden, um den Office Dokumentcache (ODC) zu steuern.
  
CSISyncClient ist ein out-of-proc COM-Server (CsiSyncClient.exe), mit dem Microsoft OneDrive das Verhalten des Office Dokumentcache (ODC) steuern können. Beispielsweise können OneDrive die ODC über CSISyncClient aufrufen, um Dateien in und von MS-FSSHTTP-fähigen Endpunkten hoch- und herunterzuladen. Dies ermöglicht erweiterte dienstbasierte Features in Office, z. B. gemeinsame Dokumenterstellung und nahtlose Übergänge von Offline zu Online.
  
CsiSyncClient ist in Office Desktop verfügbar (x86 und x64). Hinweis: Neuere Versionen von Office können zwar mit CsiSyncClient ausgeliefert werden, der Prozess wird jedoch nur für die Abwärtskompatibilität verwendet. Die CsiSyncClient-Schnittstelle und die Methodik der Steuerung des ODC werden sich in zukünftigen Versionen von Office ändern.
  
Die Klassen-ID ist derzeit so festgelegt, dass sie nur auf OneDrive reagiert.
  
Das COM-Objekt kann als out-of-proc COM-Server verwendet werden und wird in CsiSyncClient.exe ausgeführt. Aufgrund von Einschränkungen in Access (die vom ODC verwendet werden) wird der Bittyp angegeben, in dem Office enthalten ist. x64-Office bedeutet also ein x64-COM-Objekt oder x86-Office ein x86-COM-Objekt. Um diese Einschränkung zu umgehen, wird bei Angabe CLSCTX_LOCAL_SERVER als Teil der CoCreateInstance das COM-Objekt als out-of-proc-COM-Server gehostet, sodass bitübergreifende Kompatibilität möglich ist.
  
## <a name="interfaces"></a>Schnittstellen

CSISyncClient verwendet die folgenden Schnittstellen.
  
### <a name="interface-ilsclocalsyncclient"></a>Schnittstelle ILSCLocalSyncClient

Dies ist die primäre Schnittstelle, die zum Synchronisieren von Dateien in Office verwendet wird.
  
- ProgID: Office. LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
Das verfügbar gemachte COM-Objekt wird als Out-of-Proc-Server verwendet. Die Angabe CLSCTX_LOCAL_SERVER als Teil von CoCreateInstance ermöglicht die Kompatibilität zwischen 64-Bit- und 32-Bit-Prozessen.
  
Nachdem Sie das COM-Objekt gemeinsam erstellt haben, MÜSSEN Sie [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) zuerst aufrufen. Nachdem [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgreich abgeschlossen wurde, können Sie eine beliebige API beliebig oft und in beliebiger Reihenfolge aufrufen. Sie können auch [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) für ein bereits initialisiertes Objekt aufrufen, aber dies hat keine Auswirkungen. 
  
Die Ausnahmen vom vorherigen Absatz sind [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) und [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Nachdem Sie [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) für das COM-Objekt aufgerufen haben, MÜSSEN Sie dieses Objekt zerstören und ein neues erstellen. [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) löscht Ihren Untercache, löscht alle zugehörigen Dateiinformationen im Cache, aber belässt die Dokumente auf dem Datenträger. Außerdem bleibt der Status für die Kommunikation mit dem Cache erhalten. Auf diese Weise können Sie [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erneut aufrufen, um einen neuen Cache zu erstellen, ohne das COM-Objekt zu zerstören und neu zu erstellen. 
  
**Öffentliche Memberfunktionen**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile wird verwendet, um die Dateiinformationen aus dem Cache zu entfernen. Diese Methode belässt die zugeordnete Datei jedoch auf dem Datenträger und auf dem Server.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Die Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die angegebene ResourceID befindet sich nicht im Cache.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die Datei wird derzeit synchronisiert oder geöffnet und kann nicht gelöscht werden.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient::GetChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges gibt einen Enumerator von ILSCEvent-Objekten zurück und gibt auch ein Token zurück, das dem nächsten Aufruf von GetChanges übergeben wird, vorausgesetzt, der Consumer hat den vorherigen Satz von Ereignissen verarbeitet. Ereignisse vor dem  _angegebenen nPreviousChangesToken_ werden gelöscht und sind nicht verfügbar. Wenn keine Ereignisse verarbeitet werden sollen, sollte  _pnCurrentChangesToken_ den gleichen Wert wie  _nPreviousChangesToken_ aufweisen,  _ppiEvents_ wird jedoch weiterhin festgelegt. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parameter

 _nPreviousChangesToken_
  
Gibt an, welches Ereignis zuletzt vom Verbraucher verarbeitet wurde. 
  
 _pnCurrentChangesToken_
  
Identifiziert das letzte Ereignis, das dem Verbraucher übergeben wird. Darf nicht NULL sein.
  
 _ppiEvents_
  
Ein Enumerator für die Ereignisse, die dem Verbraucher übergeben werden. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission wird verwendet, um abzufragen, ob die Synchronisierungshuristiken Office für Netzwerkkosten und Energieverbrauch überschrieben werden. Wenn sie sich in einem 3G oder einem anderen kostengünstigen Netzwerk befinden oder wenn sie mit Akku betrieben werden, oder wenn sie nicht angeschlossen sind, können Office den Netzwerkdatenverkehr bis zu einem besseren Zeitpunkt blockieren.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parameter

 _nspType_
  
Ein Kennzeichen, das definiert, welche Kosten heuristisch abgefragt werden sollen. Siehe [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Gibt an, ob die angeforderte Kostenhuristik derzeit überschrieben wird oder nicht. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus wird verwendet, um Informationen für eine bestimmte Datei zu sammeln: ob sie im Cache vorhanden ist, ob die Kommunikation mit der Serverkopie aussteht und ob Office 2013 die aktuellsten Daten aus der lokalen Kopie enthält. Es erfordert ein bitweises Flag von [Enum LSCStatusFlag-Werten,](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) um zu bestimmen, nach welchen Informationen das CsiSyncClient COM-Objekt abfragen soll. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Die Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss nicht leer sein und maximal 128 Zeichen umfassen. 
  
 _sfRequestedStatus_
  
Ein Kennzeichen, das definiert, welche Informationen zurückgegeben werden sollen. Siehe [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _PbstrFileSystemPath_
  
Die Zeichenfolge, die den Speicherort der von  _bstrResourceID_ auf dem Client identifizierten Datei identifiziert. Darf nicht NULL sein. 
  
 _PbstrETag_
  
Eine Zeichenfolge, die das eTag für die von  _bstrResourceID_ identifizierte Datei enthält. Darf nicht NULL sein. 
  
 _psfFileStatus_
  
Ein Kennzeichen, das den über  _sfRequestedStatus angeforderten_ Status für die durch  _bstrResourceID_ identifizierte Datei enthält. Darf nicht NULL sein. Siehe [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die durch  _bstrResourceID_ angegebenen Dateiinformationen sind nicht im Cache vorhanden.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged angefordert wurde oder die durch  _bstrResourceID_ angegebene Datei gesperrt oder fehlt.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions gibt eine Liste von durch Pipe getrennten Dateierweiterungen zurück, die derzeit vom CsiSyncClient COM-Objekt unterstützt werden. Beachten Sie, dass sich diese Liste ändern kann, und der Verbraucher über eine Änderung über das IPartnerActivityCallback-Objekt benachrichtigt wird, das auf [ILSCLocalSyncClient bereitgestellt wird::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (Siehe EventOccured). 
  
Ein Beispiel für die zurückgegebene Zeichenfolge lautet wie folgt: "|docx|docm|pptx|"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parameter

 _pbstrSupportedFileExtensions_
  
Eine Zeichenfolge, die mit einem durch Pipe getrennten Satz von Dateierweiterungen festgelegt werden soll, der vom CsiSyncClient COM-Objekt unterstützt wird. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize muss die erste aufgerufene Methode sein. Andernfalls geben alle anderen APIs E_LSC_NOTINITIALIZED zurück. Das Aufrufen der Initialisierung für ein bereits initialisiertes Objekt gibt S_OK zurück und führt keine Aktion aus. Wenn E_LSC_CACHEMISMATCH zurückgegeben wird, kann der Aufrufer [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) aufrufen, um den Cache zu löschen, der der angegebenen SuppliedID zugeordnet ist. In diesem Fall geben andere APIs jedoch weiterhin E_LSC_NOTINITIALIZED zurück. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parameter

 _bstrSuppliedID_
  
Gibt den Consumer und den zu verwendenden Cache an. Muss mit maximal 32 Zeichen nicht leer sein. 
  
 _bstrProgID_
  
Identifiziert das COM-Objekt des Verbrauchers für die bidirektionale Kommunikation. Muss mit maximal 39 Zeichen nicht leer sein. Weitere Informationen zu ProgIDs finden Sie unter [ \<ProgID\> Schlüssel.](https://docs.microsoft.com/windows/desktop/com/-progid--key) 
  
 _bstrFileSystemDirectoryHint_
  
Gibt den Verzeichnisstamm an, in dem lokale Dateien gespeichert werden. Muss mit maximal 256 Zeichen nicht leer sein. Das Verzeichnis muss bereits vorhanden sein. 
  
 _pEventCallback_
  
Die Rückrufschnittstelle, die CsiSyncClient bei Änderungen benachrichtigt. Siehe "IPartnerActivityCallback::EventOccurred". Dieser Wert darf nicht null sein. 
  
 _pfCreatedNewCache_
  
Gibt zurück, ob ein neuer Cache erstellt wurde. Wenn der angegebenen ID kein Cache zugeordnet ist, wird einer erstellt. Dieser Wert darf nicht null sein.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Einer SuppliedID ist bereits ein Cache zugeordnet, aber eine andere ProgId oder FileSystemDirectoryHint als die bereitgestellten.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |FileSystemDirectoryHint (oder ein Unterordner) ist bereits in einem anderen Cache vorhanden.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |Die ProgID ist bereits in einem anderen Cache vorhanden.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange wird verwendet, um das CsiSyncClient COM-Objekt anweisen, die angegebene Datei hochzuladen. Die Methode bereitet die Datei für den Upload vor, einschließlich des Lesens des aktuellen Inhalts der Datei. Wenn ein Upload bereits aussteht, wird der vorherige Upload verworfen, und die neuen Inhalte werden für den Upload vorbereitet. Wenn die Datei zur Bearbeitung in einer Anwendung geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei für den Upload vorzubereiten (die Anwendung sollte diesen Schritt bereits ausführen, wenn Änderungen vorhanden sind).
  
Diese Methode ermöglicht Uploads, wenn sie als zuvor blockierte Uploads markiert wurde (siehe [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

 _bstrFileSystemPath_
  
Eine Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein. Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die von FileSystemDirectoryHint angegeben wurde, als der Aufruf von [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) ausgeführt wurde. 
  
 _bstrResourceID_
  
Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein. 
  
 _bstrWebPath_
  
Eine Zeichenfolge, die die Datei auf dem Server identifiziert. Dieser Wert muss nicht leer, gültige URL sein, jedoch nicht länger als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427 . 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Die von  _bstrFileSystemPath_ angegebene Datei hat eine andere ResourceID als angegeben. Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird. Siehe [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Datei wurde während des mittleren Vorgangs gelöscht.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Die angegebene Dateierweiterung wird vom CsiSyncClient COM-Objekt nicht unterstützt. Siehe [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |Das COM-Objekt hat keinen Upload geplant, da die Datei im Cache die neuesten Änderungen vom Datenträger aufwies.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Die durch  _bstrFileSystemPath_ angegebene Datei fehlt oder ist gesperrt.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Die durch  _bstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei hat bereits ausstehende Änderungen in einem anderen Cache und kann dem Cache des Consumers noch nicht zugeordnet werden.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Der bereitgestellte WebPath unterliegt einem anderen Cache.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile ordnet eine neue URL und einen lokalen Pfad für eine bestimmte ResourceID zu. Wenn die durch die ResourceID angegebene Datei nicht bereits im Cache vorhanden ist, wird versucht, sie zu erstellen und zum Download zu markieren.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein. 
  
 _bstrNewFileSystemPath_
  
Eine Zeichenfolge, die den neuen lokalen Pfad für die Datei angibt. Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein. Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die von FileSystemDirectoryHint angegeben wurde, als der Aufruf der Initialisierung ausgeführt wurde. 
  
 _bstrNewWebPath_
  
Eine Zeichenfolge, die die neue URL für die Datei angibt. Dieser Wert muss nicht leerer gültiger URL sein, jedoch nicht länger als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427 definiert. 
  
 _fBlockUploads_
  
Gibt an, ob Uploads an den neuen Speicherort derzeit zulässig sind. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Der  _bstrNewFileSystemPath_ oder  _bstrNewWebPath_ ist bereits in einer anderen Datei in einem Cache vorhanden. Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird. Siehe [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Dateiinformationen wurden während der Ausführung dieser Methode aus dem Cache gelöscht.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei wird derzeit in einer Office Anwendung synchronisiert.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache löscht den Cache, der der bei Initialize bereitgestellten SuppliedID zugeordnet ist. Dies umfasst alle Dateiinformationen, belässt die Dateien jedoch sowohl auf dem Client als auch auf dem Server. Diese Methode belässt das Objekt auch in einem teilweise nicht initialisierten Zustand. Die einzigen gültigen Aufrufe danach sind [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) oder [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Diese Methode kann aufgerufen werden, wenn initialize fehlschlägt und E_LSC_CACHEMISMATCH zurückgibt, und löscht den Cache, der der suppliedID zugeordnet ist, die mit dem fehlerhaften Aufruf bereitgestellt wurde.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parameter

Keine
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient::ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange weist das CsiSyncClient COM-Objekt an, die angegebene Datei zum Download zu markieren. Wenn die Datei in einer Office Anwendung zur Bearbeitung geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei zum Download zu markieren (die Anwendung sollte diesen Schritt bereits ausführen, wenn Änderungen vorhanden sind).
  
Diese Methode ermöglicht Downloads, wenn sie als zuvor blockierte Downloads markiert wurde (siehe RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Eine Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein. Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die von FileSystemDirectoryHint angegeben wurde, als der Aufruf der Initialisierung ausgeführt wurde.  <br/> |
|bstrResourceID  <br/> |Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein.  <br/> |
|bstrWebPath  <br/> |Eine Zeichenfolge, die die Datei auf dem Server identifiziert. Dieser Wert muss eine nicht leere gültige URL sein, jedoch nicht länger als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427 .  <br/> |
   
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Festlegen des Cachekonnektivitätsstatus.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Die von  _bstrFileSystemPath_ angegebene Datei hat eine andere ResourceID als angegeben.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Die angegebene Dateierweiterung wird vom CsiSyncClient COM-Objekt nicht unterstützt. Siehe "GetSupportedFileExtensions".  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Datei wurde in der Mitte des Vorgangs gelöscht.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Die durch  _bstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei hat bereits ausstehende Änderungen in einem anderen Cache und kann dem Cache des Consumers noch nicht zugeordnet werden.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Der bereitgestellte WebPath unterliegt einem anderen Cache.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Legt den Cache in einen Online- oder Offlinestatus fest. Im Offlinemodus versucht Office nicht, mit dem Server für Dateien in diesem Cache zu kommunizieren, unabhängig von der _fBlockUploads-Einstellung_ jeder einzelnen Datei. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parameter

 _fIsOnline_
  
Ein boolescher Wert, der den Verbindungsstatus des Caches bestimmt. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Festlegen des Cachekonnektivitätsstatus.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission wird verwendet, um die Synchronisierungshuristiken von Office für Netzwerkkosten und Energieverbrauch zu überschreiben oder wiederherzustellen. Wenn sie sich in einem 3G oder einem anderen kostengünstigen Netzwerk befinden oder wenn sie mit Akku betrieben werden, oder wenn sie nicht angeschlossen sind, können Office den Netzwerkdatenverkehr bis zu einem besseren Zeitpunkt blockieren. Der Consumer dieser API kann sie verwenden, um die Heuristiken Office außer Kraft zu setzen und die Synchronisierung zu erzwingen.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parameter

 _nspType_
  
Ein Kennzeichen, das definiert, welche Kosten heuristisch überschrieben werden sollen. Siehe [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Gibt an, ob die Synchronisierung erzwungen werden soll, um diese Kostenheuristik zu überschreiben oder nicht mehr außer Kraft zu setzen. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Außerkraftsetzen der Synchronisierung von Heuristiken.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Lädt den Cache aus dem COM-Objekt und führt Schließen-Vorgänge aus. [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUSS aufgerufen werden, bevor das COM-Objekt zerstört wird. Nach dem Aufruf können keine anderen APIs aufgerufen werden, das COM-Objekt MUSS zerstört und ein neues erstellt werden, wenn Sie den Vorgang fortsetzen möchten. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parameter

Keine.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Aufheben der Initialisierung.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Schnittstelle IEnumLSCEvent

Diese Schnittstelle stellt eine Liste der ILSCEvent-Ereignisse dar.
  
**Öffentliche Memberfunktionen**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent::FNext

Ruft das nächste Ereignis aus der Liste der Ereignisse ab.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Parameter

 _ppiLSCEvent_
  
Ein Zeiger auf eine ILSCEvent-Schnittstelle.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Es gibt keine weiteren Ereignisse.  <br/> |
|S_OK  <br/> |Der Anruf war erfolgreich.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Setzt den Enumerator auf das erste Ereignis zurück.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parameter

Keine.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
### <a name="interface-ilscevent"></a>Schnittstelle ILSCEvent

Diese Schnittstelle stellt ein Synchronisierungsereignis dar. Alle Informationen über das Ereignis können von der Schnittstelle abgerufen werden.
  
**Öffentliche Memberfunktionen**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Beachten Sie, dass dieser Wert aufgefüllt wird, wenn [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) aufgerufen wird, nicht beim Erstellen des Ereignisses. Daher haben Sie nur den aktuellen Status der Datei, nicht den Status der Datei, wenn sich der Konfliktstatus geändert hat. 
  
Dieser Wert wird nur ausgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnLocalConflictStateChanged ist. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parameter

 _pfIsInConflict_
  
Der aktuelle Konfliktstatus der Datei, die dem Ereignis zugeordnet ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Dieser Wert wird nur ausgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parameter

 _pnError_
  
Der diesem Ereignis zugeordnete Fehler.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Dieser Wert wird nur ausgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parameter

 _PbstrETag_
  
Das diesem Ereignis zugeordnete ETag
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Ruft den Typ für dieses Ereignis ab.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parameter

 _pnEventType_
  
Der Ereignistyp dieses Ereignisses. Gültige Werte finden Sie unter ["Enum LSCEventType".](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|S_OK  <br/> |Der Anruf war erfolgreich.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Ruft den lokalen Arbeitspfad für dieses Ereignis ab.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parameter

 _pbstrLocalWorkingPath_
  
Der lokale Pfad der Datei, zu der dieses Ereignis gehört. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Ruft die Ressourcen-ID für das Ereignis ab.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parameter

 _PbstrResourceID_
  
Die ResourceID der Datei, die diesem Ereignis zugeordnet ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Dieser Wert wird nur ausgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist. Wenn ein Aufruf von [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) einen Webpfad- oder lokalen Pfadkonflikt mit einer anderen Datei im Office Dateicache verursachen würde, wird dieses Ereignis generiert. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parameter

 _pbstrResourceIDAttempted_
  
Die ResourceID, durch die dieses Ereignis generiert wurde. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Dieser Wert wird nur ausgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parameter

 _pnSyncErrorType_
  
Der Fehlertyp, der diesem Ereignis zugeordnet ist. Mögliche Werte finden Sie unter ["Enum LSCEventType".](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|S_OK  <br/> |Der Anruf war erfolgreich.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Dieser Wert wird nur ausgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parameter

 _PbstrWebPath_
  
Gibt den Webpfad an, der diesem Ereignis zugeordnet ist. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
### <a name="interface-ilscevent2"></a>Schnittstelle ILSCEvent2

Diese Schnittstelle enthält zusätzliche Informationen zu einem Synchronisierungsereignis.
  
**Öffentliche Memberfunktionen**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Ruft die Fehlerketteninformationen zu einem Synchronisierungsereignis ab.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parameter

 _PbstrErrorChain_
  
Eine Zeichenfolge zum Speichern der Fehlerketteninformationen. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_NOTIMPL  <br/> |Die installierte Version von Office unterstützt diese Schnittstelle nicht.  <br/> |
|E_INVALIDARG  <br/> |Mindestens einer der Parameterwerte ist ungültig.  <br/> |
|E_FAIL  <br/> |Die Informationen zur Fehlerkette sind nicht verfügbar.  <br/> |
|S_OK  <br/> |Der Anruf war erfolgreich.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Schnittstelle IPartnerActivityCallback

Diese Schnittstelle stellt eine Rückruffunktion für das CSISyncClient COM-Objekt bereit.
  
**Öffentliche Memberfunktionen**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Dies ist eine Rückruffunktion für das Objekt, das dem CsiSyncClient COM-Objekt übergeben wird. Es wird erwartet, dass beim Auftreten eines Ereignisses (siehe [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) für gültige Ereignistypen) das CsiSyncClient COM-Objekt diese Methode aufruft und den Consumer signalisiert. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parameter

 _eEventTypeOccurred_
  
Der Ereignistyp dieses Ereignisses. Gültige Werte finden Sie unter ["Enum LSCEventTypeOccurred".](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück.
  
## <a name="enumerations"></a>Aufzählungen

CSISyncClient verwendet die folgenden Enumerationen.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Diese Enumeration gibt die Kategorien von Fehlern an, die beim Synchronisieren einer Datei auftreten können.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |Der Synchronisierungsfehler dieses Ereignisses war unerwartet und kann besondere Überlegungen erfordern. Standardmäßig muss der Benutzer möglicherweise eingreifen.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses muss nicht besonders berücksichtigt werden. Office wird automatisch behandelt.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass ein Benutzer ihn beheben kann. Beispielsweise erfordert ein Zusammenführungskonfliktfehler, dass ein Benutzer das Dokument öffnen und zusammenführen muss.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Verbraucher eingreifen muss, der Benutzer sollte jedoch keine besondere Berücksichtigung erfordern.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Verbraucher als Sonderfall eingreifen muss.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enumeration LSCEventType
<a name="Enum_LSCEventType"> </a>

Diese Enumeration gibt den Typ der Ereignisse an, die für eine bestimmte Datei auftreten können.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |An einer lokalen Datei wurden Änderungen vorgenommen.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Ein Benutzer hat eine Datei geöffnet.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Dateiänderungen wurden vom Server heruntergeladen.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Dateiänderungen wurden auf den Server hochgeladen.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |Der Zusammenführungskonfliktstatus einer Datei wurde geändert.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Eine Datei wurde hinzugefügt.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Eine Datei wurde gelöscht.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Die Synchronisierung wurde für die Dateien eines Benutzers aktiviert.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Dateiänderungen wurden vom Server heruntergeladen.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Dateiänderungen wurden auf den Server hochgeladen.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Dieses Ereignis wird generiert, wenn ein Aufruf von [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) einen Webpfad- oder lokalen Pfadkonflikt mit einer anderen Datei im Office Dateicache verursacht.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Diese Enumeration gibt den Typ der Ereignisse an, die auftreten können. Der Consumer muss bestimmte ILSCLocalSyncClient-Funktionen basierend auf dem Ereignistyp aufrufen.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Ein ILSCEvent ist aufgetreten. Der Consumer sollte [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) aufrufen, um die Daten abzurufen.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Die unterstützten Dateierweiterungen wurden geändert. Der Consumer sollte [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) aufrufen, um die neue Liste der unterstützten Erweiterungen abzurufen.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Diese Enumeration gibt die Flags an, die für eine Heuristik für Netzwerkkosten verwendet werden. 

|Enumerator|Beschreibung|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True, wenn die Kostenhuristik für teure Netzwerke (z. B. 3G) überschrieben wird.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True, wenn die Kostenhuristik für die Energienutzung (z. B. einen Akku) überschrieben wird.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Diese Enumeration wird verwendet, um den Synchronisierungsstatus einer Datei darzustellen. 
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True, wenn an die Serverdatei zu sendende Daten ausstehen.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True, wenn daten aus der Serverdatei heruntergeladen werden müssen.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True, wenn die Daten, die Office in der Datei im Cache gespeichert hat, die letzte Kopie der Daten auf dem Datenträger sind.  <br/> |
   

