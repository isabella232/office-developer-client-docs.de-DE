---
title: Verwenden von CSISyncClient zum Steuern Office Dokumentcache (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Erfahren Sie, wie Sie CSISyncClient zum Steuern des Office Document Cache (ODC) verwenden.
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346256"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Verwenden von CSISyncClient zum Steuern Office Dokumentcache (ODC)

Erfahren Sie, wie Sie CSISyncClient zum Steuern des Office Document Cache (ODC) verwenden.
  
CSISyncClient ist ein out-of-proc-COM-Server (CsiSyncClient.exe), der Microsoft OneDrive das Verhalten des Office Document Cache (ODC) steuern kann. Beispielsweise kann OneDrive odC über CSISyncClient aufrufen, um Dateien auf und von MS-FSSHTTP-aktivierten Endpunkten hochzuladen und herunterzuladen. Dies ermöglicht erweiterte servicegesicherte Features in Office, z. B. die gemeinsamen Erstellung und nahtlose Übergänge von offline zu online.
  
CsiSyncClient ist in Office Desktop verfügbar (sowohl x86 als auch x64). Hinweis: Neuere Versionen von Office möglicherweise mit CsiSyncClient, der Prozess wird jedoch nur zur Abwärtskompatibilität verwendet. Die CsiSyncClient-Schnittstelle und die Methode zum Steuern des ODC werden sich in zukünftigen Versionen von Office.
  
Die Klassen-ID ist derzeit so festgelegt, dass sie nur auf OneDrive.
  
Das COM-Objekt kann als out-of-proc-COM-Server verwendet werden und wird in CsiSyncClient.exe. Aufgrund von Einschränkungen bei Access (die vom ODC verwendet werden) wird der Bittyp Office verwendet, sodass x64 Office ein x64 COM-Objekt oder x86 Office ein x86 COM-Objekt bedeutet. Um diese Einschränkung zu umgehen, wird das COM-Objekt CLSCTX_LOCAL_SERVER durch Angabe von CLSCTX_LOCAL_SERVER als Teil der CoCreateInstance als out-of-proc-COM-Server gehostet, was bitübergreifende Kompatibilität ermöglicht.
  
## <a name="interfaces"></a>Schnittstellen

CSISyncClient verwendet die folgenden Schnittstellen.
  
### <a name="interface-ilsclocalsyncclient"></a>Schnittstelle ILSCLocalSyncClient

Dies ist die primäre Schnittstelle zum Synchronisieren von Dateien in Office.
  
- ProgID: Office. LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
Das verfügbar gemachte COM-Objekt wird als Out-of-Proc-Server verwendet. Das Angeben CLSCTX_LOCAL_SERVER als Teil von CoCreateInstance ermöglicht die Kompatibilität zwischen 64-Bit- und 32-Bit-Prozessen.
  
Nachdem Sie das COM-Objekt gemeinsam erstellt haben, müssen Sie [zuerst ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) aufrufen. Sobald [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgreich abgeschlossen wurde, können Sie jede API so oft wie gewünscht und in beliebiger Reihenfolge aufrufen. Sie können auch [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) für ein bereits initialisiertes Objekt aufrufen, dies führt jedoch nicht dazu. 
  
Die Ausnahmen zum vorherigen Absatz sind [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) und [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Nachdem Sie [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) für das COM-Objekt aufgerufen haben, müssen Sie dieses Objekt zerstören und ein neues erstellen. [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) löscht Ihren Untercache, löscht alle zugeordneten Dateiinformationen im Cache, belasse die Dokumente jedoch auf dem Datenträger. Außerdem bleibt der Zustand für die Kommunikation mit dem Cache erhalten. Auf diese Weise können Sie [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erneut aufrufen, um einen neuen Cache zu erstellen, ohne das COM-Objekt zerstören und neu erstellen zu müssen. 
  
**Öffentliche Memberfunktionen**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

DeleteFile wird verwendet, um die Dateiinformationen aus dem Cache zu entfernen. Bei dieser Methode bleibt die zugeordnete Datei jedoch auf dem Datenträger und auf dem Server.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Die Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert darf maximal 128 Zeichen lang sein. 
  
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

GetChanges gibt einen Enumerator von ILSCEvent-Objekten zurück und gibt auch ein Token zurück, das für den nächsten Aufruf von GetChanges angegeben wird, vorausgesetzt, der Consumer hat den vorherigen Satz von Ereignissen verarbeitet. Ereignisse vor  _dem angegebenen nPreviousChangesToken_ werden gelöscht und sind nicht verfügbar. Wenn keine Ereignisse verarbeitet werden sollen, sollte  _pnCurrentChangesToken_ denselben Wert wie  _nPreviousChangesToken_ haben,  _aber ppiEvents_ wird weiterhin festgelegt. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parameter

 _nPreviousChangesToken_
  
Gibt an, welches Ereignis zuletzt vom Consumer verarbeitet wurde. 
  
 _pnCurrentChangesToken_
  
Gibt das neueste Ereignis an, das an den Verbraucher übergeben wird. Darf nicht null sein.
  
 _ppiEvents_
  
Ein Aufzählerator für die Ereignisse, die dem Verbraucher übergeben werden. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient::GetClientNetworkSyncPermission

GetClientNetworkSyncPermission wird verwendet, um zu abfragen, ob Office Synchronisierungs heuristics für Netzwerkkosten und Energieverbrauch außer Kraft gesetzt werden. Wenn sie sich 3G oder einem anderen netzwerk mit hohen Kosten befinden oder wenn sie mit Akku betrieben werden oder angeschlossen werden, Office möglicherweise den Netzwerkdatenverkehr bis zu einem bestimmten Zeitpunkt blockieren.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parameter

 _nspType_
  
Ein Flag, das definiert, welche Kosten heuristisch abgefragt werden. Weitere [Informationen finden Sie unter Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Gibt an, ob die angeforderte Kostenhuristik derzeit außer Kraft gesetzt wird. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient::GetFileStatus

GetFileStatus wird verwendet, um Informationen für eine bestimmte Datei zu sammeln: ob sie im Cache vorhanden ist, ob die Kommunikation mit der Serverkopie aussteht und Office 2013 die neuesten Daten aus der lokalen Kopie enthält. Es erfordert ein bitweises Flag von [Enum LSCStatusFlag-Werten,](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) um zu bestimmen, welche Informationen das CsiSyncClient COM-Objekt abfragen soll. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Die Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert darf nicht leer sein und darf maximal 128 Zeichen lang sein. 
  
 _sfRequestedStatus_
  
Ein Flag, das definiert, welche Informationen zurückgeben werden. Siehe [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
Die Zeichenfolge, die den Speicherort der Datei identifiziert, die von  _bstrResourceID auf_ dem Client identifiziert wird. Darf nicht null sein. 
  
 _pbstrETag_
  
Eine Zeichenfolge, die das eTag für die durch _bstrResourceID identifizierte Datei enthält._ Darf nicht null sein. 
  
 _psfFileStatus_
  
Ein Flag, das den über _sfRequestedStatus_ angeforderten Status für die durch _bstrResourceID identifizierte Datei enthält._ Darf nicht null sein. Siehe [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die von  _bstrResourceID_ angegebenen Dateiinformationen sind im Cache nicht vorhanden.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged angefordert wurde oder die durch  _bstrResourceID_ angegebene Datei gesperrt oder fehlt.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient::GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions gibt eine Liste der durch Pipe getrennten Dateierweiterungen zurück, die derzeit vom CsiSyncClient COM-Objekt unterstützt werden. Beachten Sie, dass sich diese Liste ändern kann, und der Verbraucher wird über das IPartnerActivityCallback-Objekt benachrichtigt, das auf [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) bereitgestellt wird (siehe EventOccured). 
  
Ein Beispiel für die zurückgegebene Zeichenfolge lautet: "|docx|docm|pptx|"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parameter

 _pbstrSupportedFileExtensions_
  
Eine Zeichenfolge, die mit einem durch Pipe getrennten Satz von Dateierweiterungen festgelegt werden soll, die vom CsiSyncClient COM-Objekt unterstützt werden. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient::Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize muss die erste aufgerufene Methode sein. Andernfalls werden alle anderen APIs E_LSC_NOTINITIALIZED. Das Aufrufen von Initialize für ein bereits initialisiertes Objekt gibt S_OK zurück und führt nichts aus. Wenn E_LSC_CACHEMISMATCH zurückgegeben wird, kann der Aufrufer [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) aufrufen, um den Cache zu löschen, der der angegebenen SuppliedID zugeordnet ist. In diesem Fall werden jedoch weiterhin andere APIs E_LSC_NOTINITIALIZED. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parameter

 _bstrSuppliedID_
  
Identifiziert den Consumer und den zu verwendende Cache. Darf maximal 32 Zeichen lang sein. 
  
 _bstrProgID_
  
Identifiziert das COM-Objekt des Verbrauchers für die zweiwege Kommunikation. Darf maximal 39 Zeichen lang sein. Weitere Informationen zu ProgIDs finden Sie unter [ \< ProgID \> Key.](https://docs.microsoft.com/windows/desktop/com/-progid--key) 
  
 _bstrFileSystemDirectoryHint_
  
Gibt den Verzeichnisstamm an, in dem lokale Dateien gespeichert werden. Darf maximal 256 Zeichen lang sein. Das Verzeichnis muss bereits vorhanden sein. 
  
 _pEventCallback_
  
Die Rückrufschnittstelle, die CsiSyncClient bei Änderungen benachrichtigt. Weitere Informationen finden Sie unter IPartnerActivityCallback::EventOccurred. Dieser Wert darf nicht null sein. 
  
 _pfCreatedNewCache_
  
Gibt zurück, ob ein neuer Cache erstellt wurde. Wenn der SuppliedID kein Cache zugeordnet ist, wird ein Cache erstellt. Dieser Wert darf nicht null sein.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Einer SuppliedID ist bereits ein Cache zugeordnet, aber eine andere ProgId oder FileSystemDirectoryHint als die bereitgestellten.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |Das FileSystemDirectoryHint (oder ein Unterordner) ist bereits in einem anderen Cache vorhanden.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |Die ProgID ist bereits in einem anderen Cache vorhanden.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient::LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange wird verwendet, um das CsiSyncClient COM-Objekt anzuraten, die angegebene Datei hochzuladen. Die Methode bereitet die Datei für den Upload vor, einschließlich des Lesens des aktuellen Inhalts der Datei. Wenn ein Upload bereits aussteht, wird der vorherige Upload verworfen und die neuen Inhalte für den Upload vorbereitet. Wenn die Datei für die Bearbeitung in einer Anwendung geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei für den Upload vorbereiten zu müssen (die Anwendung sollte diesen Schritt bereits tun, wenn Änderungen vorhanden sind).
  
Diese Methode ermöglicht Uploads, wenn sie zuvor als blockierte Uploads markiert wurde (siehe [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

 _bstrFileSystemPath_
  
Eine Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein. Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die vom FileSystemDirectoryHint angegeben wird, wenn der Aufruf von [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgt ist. 
  
 _bstrResourceID_
  
Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert darf maximal 128 Zeichen lang sein. 
  
 _bstrWebPath_
  
Eine Zeichenfolge, die die Datei auf dem Server identifiziert. Dieser Wert muss nicht leer sein, gültige URL, aber nicht länger als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427 definiert. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Die von  _bstrFileSystemPath_ angegebene Datei hat eine andere ResourceID als angegeben. Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird. Siehe [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Datei wurde in der Mitte des Vorgangs gelöscht.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Die angegebene Dateierweiterung wird vom CsiSyncClient COM-Objekt nicht unterstützt. Weitere Informationen finden Sie unter [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |Das COM-Objekt hat keinen Upload geplant, da die Datei im Cache die neuesten Änderungen auf dem Datenträger hatte.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Die von  _bstrFileSystemPath_ angegebene Datei fehlt oder ist gesperrt.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Die durch  _bstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei hat bereits ausstehende Änderungen in einem anderen Cache und kann dem Cache des Verbrauchers noch nicht zugeordnet werden.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Der bereitgestellte WebPath fällt unter einen anderen Cache.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient::RenameFile
<a name="ILSCLocalSyncClient_RenameFile"> </a>

RenameFile zuordnen eine neue URL und einen lokalen Pfad für eine bestimmte ResourceID. Wenn die durch die ResourceID angegebene Datei noch nicht im Cache vorhanden ist, wird versucht, sie zu erstellen und zum Download zu markieren.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert darf maximal 128 Zeichen lang sein. 
  
 _bstrNewFileSystemPath_
  
Eine Zeichenfolge, die den neuen lokalen Pfad für die Datei angibt. Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein. Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde. 
  
 _bstrNewWebPath_
  
Eine Zeichenfolge, die die neue URL für die Datei angibt. Bei diesem Wert muss es sich um eine nicht leere gültige URL, jedoch nicht mehr als INTERNET_MAX_URL_LENGTH, wie von https://support.microsoft.com/kb/208427 definiert. 
  
 _fBlockUploads_
  
Gibt an, ob Uploads an den neuen Speicherort derzeit zulässig sind. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Der  _bstrNewFileSystemPath_ oder  _bstrNewWebPath_ ist bereits in einer anderen Datei in einem beliebigen Cache vorhanden. Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird. Siehe [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Dateiinformationen wurden während der Ausführung dieser Methode aus dem Cache gelöscht.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei wird derzeit in einer Office synchronisiert.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient::ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache löscht den Cache, der der suppliedID zugeordnet ist, die bei Initialize bereitgestellt wurde. Dies umfasst alle Dateiinformationen, die Dateien werden jedoch sowohl auf dem Client als auch auf dem Server gespeichert. Diese Methode belässt das Objekt auch in einem teilweise nicht initialisierten Zustand. Die einzigen gültigen Aufrufe danach sind [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) oder [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Diese Methode kann aufgerufen werden, wenn Initialize fehlschlägt und E_LSC_CACHEMISMATCH zurückgibt und den Cache löscht, der der SuppliedID zugeordnet ist, die mit dem fehlerhaften Aufruf bereitgestellt wurde.
  
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

ServerFileChange weist das CsiSyncClient COM-Objekt an, die angegebene Datei zum Herunterladen zu markieren. Wenn die Datei in einer Office zum Bearbeiten geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei zum Herunterladen zu markieren (die Anwendung sollte diesen Schritt bereits tun, wenn Änderungen vorhanden sind).
  
Diese Methode lässt Downloads zu, wenn sie zuvor als blockiert markiert wurde (siehe RenameFile).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Eine Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein. Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.  <br/> |
|bstrResourceID  <br/> |Eine Zeichenfolge, die die ResourceID der Datei identifiziert. Dieser Wert darf maximal 128 Zeichen lang sein.  <br/> |
|bstrWebPath  <br/> |Eine Zeichenfolge, die die Datei auf dem Server identifiziert. Bei diesem Wert muss es sich um eine nicht leere gültige URL, jedoch nicht mehr als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427 definiert.  <br/> |
   
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Festlegen des Cacheverbindungsstatus.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Die von  _bstrFileSystemPath_ angegebene Datei hat eine andere ResourceID als angegeben.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Die angegebene Dateierweiterung wird vom CsiSyncClient COM-Objekt nicht unterstützt. Weitere Informationen finden Sie unter GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Datei wurde in der Mitte des Vorgangs gelöscht.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Die durch  _bstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei hat bereits ausstehende Änderungen in einem anderen Cache und kann dem Cache des Verbrauchers noch nicht zugeordnet werden.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Der bereitgestellte WebPath fällt unter einen anderen Cache.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient::SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Legt den Cache in einen Online- oder Offlinestatus fest. Wenn sie offline Office, wird nicht versucht, mit dem Server für Dateien in diesem Cache zu kommunizieren, unabhängig von der _fBlockUploads-Einstellung_ jeder einzelnen Datei. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parameter

 _fIsOnline_
  
Ein boolescher Wert, der den Verbindungsstatus des Caches bestimmt. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Festlegen des Cacheverbindungsstatus.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient::SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission wird verwendet, um die Synchronisierungshuristiken vonOffice für Netzwerkkosten und Energieverbrauch zu überschreiben oder wiederherzustellen. Wenn sie sich 3G oder einem anderen netzwerk mit hohen Kosten befinden oder wenn sie mit Akku betrieben werden oder angeschlossen werden, Office möglicherweise den Netzwerkdatenverkehr bis zu einem bestimmten Zeitpunkt blockieren. Der Verbraucher dieser API kann sie verwenden, um die heuristischen Office zu überschreiben und die Synchronisierung zu erzwingen.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parameter

 _nspType_
  
Ein Flag, das definiert, welche Kosten heuristisch überschrieben werden müssen. Weitere [Informationen finden Sie unter Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Gibt an, ob die Synchronisierung erzwingen und damit heuristisch überschrieben oder nicht mehr außer Kraft gesetzt werden soll. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Überschreiben der Synchronisierung von Heuristiken.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient::Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Entlädt den Cache aus dem COM-Objekt und führt schließende Vorgänge aus. [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUSS aufgerufen werden, bevor das COM-Objekt zerstört wird. Nach dem Aufgerufenen können keine anderen APIs aufgerufen werden, das COM-Objekt MUSS zerstört und ein neues erstellt werden, wenn Sie vorgänge fortsetzen möchten. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parameter

Keine.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Fehler beim Uninitialisieren.  <br/> |
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
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent::Reset

Setzt den Enumerationszähler auf das erste Ereignis zurück.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parameter

Keine.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK. 
  
### <a name="interface-ilscevent"></a>Schnittstelle ILSCEvent

Diese Schnittstelle stellt ein Synchronisierungsereignis dar. Alle Informationen zum Ereignis können von der Schnittstelle abgerufen werden.
  
**Öffentliche Memberfunktionen**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent::GetConflictStatus

Beachten Sie, dass dieser Wert aufgefüllt wird, wenn [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) aufgerufen wird, nicht beim Erstellen des Ereignisses. Daher haben Sie nur den aktuellen Status der Datei und nicht den Status der Datei, wenn sich der Konfliktstatus geändert hat. 
  
Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnLocalConflictStateChanged. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parameter

 _pfIsInConflict_
  
Der aktuelle Konfliktstatus der Datei, die dem Ereignis zugeordnet ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent::GetError

Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parameter

 _pnError_
  
Der diesem Ereignis zugeordnete Fehler.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent::GetETag

Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parameter

 _pbstrETag_
  
Das diesem Ereignis zugeordnete ETag
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent::GetEventType

Ruft den Typ für dieses Ereignis ab.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parameter

 _pnEventType_
  
Der Ereignistyp dieses Ereignisses. Gültige [Werte finden Sie unter Enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent::GetLocalWorkingPath

Ruft den lokalen Arbeitspfad für dieses Ereignis ab.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parameter

 _pbstrLocalWorkingPath_
  
Der lokale Pfad der Datei, zu der dieses Ereignis führt. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent::GetResourceID

Ruft die Ressourcen-ID für das Ereignis ab.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parameter

 _pbstrResourceID_
  
Die ResourceID der Datei, die diesem Ereignis zugeordnet ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent::GetResourceIDAttempted

Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict. Wenn ein Aufruf von [ILSCLocalSyncClient::LocalFileChange, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange) [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) einen Webpfad- oder Lokalen Pfad-Kollision mit einer anderen Datei im Office-Dateicache verursachen würde, wird dieses Ereignis generiert. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parameter

 _pbstrResourceIDAttempted_
  
Die ResourceID, die dazu führte, dass dieses Ereignis generiert wurde. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent::GetSyncErrorType

Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parameter

 _pnSyncErrorType_
  
Der diesem Ereignis zugeordnete Fehlertyp. Mögliche Werte finden Sie [unter Enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent::GetWebPath

Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parameter

 _pbstrWebPath_
  
Gibt den diesem Ereignis zugeordneten Webpfad an. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK. 
  
### <a name="interface-ilscevent2"></a>Schnittstelle ILSCEvent2

Diese Schnittstelle enthält zusätzliche Informationen zu einem Synchronisierungsereignis.
  
**Öffentliche Memberfunktionen**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2::GetErrorChain

Ruft die Fehlerketteninformationen zu einem Synchronisierungsereignis ab.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parameter

 _pbstrErrorChain_
  
Eine Zeichenfolge zum Halten der Fehlerketteninformationen. Darf nicht null sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_NOTIMPL  <br/> |Die installierte Version von Office unterstützt diese Schnittstelle nicht  <br/> |
|E_INVALIDARG  <br/> |Mindestens einer der Parameterwerte ist ungültig.  <br/> |
|E_FAIL  <br/> |Die Informationen zur Fehlerkette sind nicht verfügbar.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Schnittstelle IPartnerActivityCallback

Diese Schnittstelle stellt eine Rückruffunktion für das CSISyncClient COM-Objekt bereit.
  
**Öffentliche Memberfunktionen**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback::EventOccurred

Dies ist eine Rückruffunktion für das Objekt, das dem CsiSyncClient COM-Objekt übergeben wird. Es wird erwartet, dass beim Auftreten eines Ereignisses (siehe [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) für gültige Ereignistypen) das CsiSyncClient COM-Objekt diese Methode aufruft und den Consumer signalisiert. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parameter

 _eEventTypeOccurred_
  
Der Ereignistyp dieses Ereignisses. Gültige Werte finden Sie unter [Enum LSCEventTypeOccurred.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK.
  
## <a name="enumerations"></a>Enumerationen

CSISyncClient verwendet die folgenden Enumerationen.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Diese Aufzählung gibt die Kategorien von Fehlern an, die beim Synchronisieren einer Datei auftreten können.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |Der Synchronisierungsfehler dieses Ereignisses war unerwartet und kann besondere Beachtung erfordern. Standardmäßig muss der Benutzer möglicherweise eingreifen.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses muss nicht besonders berücksichtigt werden. Office wird automatisch ausgeführt.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass ein Benutzer ihn löst. Beispielsweise erfordert der Zusammenführungskonfliktfehler, dass ein Benutzer das Dokument öffnet und zusammenführen muss.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Verbraucher interveniert, sollte jedoch vom Benutzer nicht besonders berücksichtigt werden.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Verbraucher als Sonderfall interveniert.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enum LSCEventType
<a name="Enum_LSCEventType"> </a>

Diese Enumeration gibt den Typ der Ereignisse an, die für eine bestimmte Datei auftreten können.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |An einer lokalen Datei wurden Änderungen vorgenommen.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Ein Benutzer hat eine Datei geöffnet.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Das Herunterladen von Dateiänderungen vom Server wurde abgeschlossen.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Das Hochladen von Dateiänderungen auf den Server wurde abgeschlossen.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |Der Seriendruckkonfliktstatus einer Datei hat sich geändert.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Es wurde eine Datei hinzugefügt.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Eine Datei wurde gelöscht.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Die Synchronisierung wurde für die Dateien eines Benutzers aktiviert.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Das Herunterladen von Dateiänderungen vom Server wurde gestartet.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Es wurde begonnen, Dateiänderungen auf den Server hochzuladen.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Dieses Ereignis wird generiert, wenn ein Aufruf von [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) einen Webpfad- oder lokalen Pfadzusammenstoß mit einer anderen Datei im Office-Dateicache verursacht.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Diese Aufzählung gibt den Typ der Ereignisse an, die auftreten können. Der Consumer muss bestimmte ILSCLocalSyncClient-Funktionen basierend auf dem Ereignistyp aufrufen.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Ein ILSCEvent ist aufgetreten. Der Consumer sollte [ILSCLocalSyncClient::GetChanges aufrufen, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) um die Daten abzurufen.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Die unterstützten Dateierweiterungen haben sich geändert. Der Consumer sollte [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) aufrufen, um die neue Liste der unterstützten Erweiterungen abzurufen.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Diese Enumeration gibt die Flags an, die für eine Heuristik der Netzwerkkosten verwendet werden. 

|Enumerator|Beschreibung|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True, wenn die Kostenhuristik für teure Netzwerke (z. B. 3G) außer Kraft gesetzt wird.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True, wenn die Kostenhuristik für den Energieverbrauch (z. B. ein Akku) außer Kraft gesetzt wird.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Diese Enumeration wird verwendet, um den Synchronisierungsstatus einer Datei zu repräsentieren. 
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True, wenn ausstehende Daten an die Serverdatei gesendet werden müssen.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True, wenn ausstehende Daten aus der Serverdatei heruntergeladen werden müssen.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True, wenn die Daten, Office die Datei im Cache enthält, die neueste Kopie der Daten auf dem Datenträger sind.  <br/> |
   

