---
title: Verwenden von CSISyncClient zum Steuern des Office-Dokument Caches (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Erfahren Sie, wie Sie CSISyncClient verwenden, um den Office-Dokument Cache (ODC) zu steuern.
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346256"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a>Verwenden von CSISyncClient zum Steuern des Office-Dokument Caches (ODC)

Erfahren Sie, wie Sie CSISyncClient verwenden, um den Office-Dokument Cache (ODC) zu steuern.
  
CSISyncClient ist ein prozessinterner COM-Server (CsiSyncClient. exe), der es Microsoft OneDrive ermöglicht, das Verhalten des Office-Dokument Caches (ODC) zu steuern. Beispielsweise kann OneDrive die ODC über CSISyncClient zum Hochladen und Herunterladen von Dateien zu und von MS-FSSHTTP-aktivierten Endpunkten aufrufen. Dies ermöglicht erweiterte Dienst gesicherte Funktionen in Office, wie die gemeinsame Dokumenterstellung und nahtlose Übergänge zwischen Offline und online.
  
CsiSyncClient ist in Office Desktop (sowohl x86 als auch x64) verfügbar. Hinweis: während neuere Versionen von Office möglicherweise mit CsiSyncClient ausgeliefert werden, wird der Prozess nur aus Gründen der Abwärtskompatibilität verwendet. Die CsiSyncClient-Schnittstelle und die Methodik der Überwachung von ODC werden in zukünftigen Versionen von Office geändert.
  
Die Klassen-ID ist derzeit so festgelegt, dass Sie nur auf OneDrive antwortet.
  
Das COM-Objekt kann als out-of-proc-COM-Server verwendet werden und wird in CsiSyncClient. exe ausgeführt. Aufgrund von Einschränkungen beim Zugriff (der von ODC verwendet wird), wird er mit dem Bit-Typ ausgeliefert, in dem Office eingeht, sodass x64 Office ein x64-COM-Objekt oder x86 Office ein x86-COM-Objekt bezeichnet. Um diese Einschränkung zu umgehen, muss das COM-Objekt als ein Out-of-proc-COM-Server gehostet werden, um die Bitanzahl-Kompatibilität zu ermöglichen, indem Sie CLSCTX_LOCAL_SERVER als Teil des CoCreateInstance angeben.
  
## <a name="interfaces"></a>Schnittstellen

CSISyncClient verwendet die folgenden Schnittstellen.
  
### <a name="interface-ilsclocalsyncclient"></a>Schnittstelle ILSCLocalSyncClient

Dies ist die primäre Schnittstelle, die zum Synchronisieren von Dateien in Office verwendet wird.
  
- ProgID: Office. LocalSyncClient
- CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}
- TypBibliothek: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}
   
Das verfügbar gemachte COM-Objekt wird als out-of-proc-Server verwendet. Die Angabe von CLSCTX_LOCAL_SERVER als Teil von CoCreateInstance ermöglicht die Kompatibilität zwischen 64bit-und 32bit-Prozessen.
  
Nachdem Sie das COM-Objekt erstellt haben, müssen Sie zuerst [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) aufrufen. Nachdem [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgreich abgeschlossen wurde, können Sie eine beliebige API beliebig oft und in beliebiger Reihenfolge aufrufen. Sie können auch [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) für ein bereits initialisiertes Objekt aufrufen, aber dies hat keine Funktion. 
  
Die Ausnahmen vom vorherigen Absatz sind [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) und [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Nachdem Sie [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) für das COM-Objekt aufgerufen haben, müssen Sie dieses Objekt zerstören und eine neue erstellen. [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) löscht den unter Cache, löscht alle zugehörigen Dateiinformationen im Cache, belässt die Dokumente jedoch auf dem Datenträger. Außerdem bleibt der Status für die Kommunikation mit dem Cache intakt. Auf diese Weise können Sie [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erneut aufrufen, um einen neuen Cache zu erstellen, ohne das COM-Objekt zu zerstören und neu zu erstellen. 
  
**Öffentliche Memberfunktionen**

#### <a name="ilsclocalsyncclientdeletefile"></a>ILSCLocalSyncClient::D eleteFile

Delete File wird verwendet, um die Dateiinformationen aus dem Cache zu entfernen. Diese Methode belässt jedoch die zugehörige Datei auf dem Datenträger und auf dem Server.
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Die Zeichenfolge, die die Resourcen-Kennung der Datei identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die angegebene resourcecollection befindet sich nicht im Cache.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |Initialize wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die Datei wird derzeit synchronisiert oder geöffnet und kann nicht gelöscht werden.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a>ILSCLocalSyncClient:: getChanges
<a name="ILSCLocalSyncClient_GetChanges"> </a>

GetChanges gibt einen Enumerator von ILSCEvent-Objekten zurück und gibt auch ein Token zurück, das für den nächsten Aufruf von getChanges angegeben wird, vorausgesetzt, der Consumer hat den vorherigen Satz von Ereignissen verarbeitet. Ereignisse vor dem angegebenen _nPreviousChangesToken_ werden gelöscht und sind nicht verfügbar. Wenn keine zu verarbeitenden Ereignisse vorhanden sind, sollte _pnCurrentChangesToken_ den gleichen Wert wie _nPreviousChangesToken_aufweisen, aber _ppiEvents_ wird weiterhin festgelegt. 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a>Parameter

 _nPreviousChangesToken_
  
Gibt an, welches Ereignis zuletzt vom Consumer verarbeitet wurde. 
  
 _pnCurrentChangesToken_
  
Gibt das letzte Ereignis an, das dem Consumer übergeben wird. Darf nicht NULL sein.
  
 _ppiEvents_
  
Ein Enumerator für die Ereignisse, die dem Consumer übergeben wurden. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a>ILSCLocalSyncClient:: GetClientNetworkSyncPermission

GetClientNetworkSyncPermission wird verwendet, um abzufragen, ob die Synchronisierungs Heuristik von Office für Netzwerkkosten und Energieverbrauch außer Kraft gesetzt wird. Wenn Sie sich in einem 3G-oder einem anderen hochkosten Netzwerk oder bei Batteriebetrieb im Vergleich mit dem Stromnetz anmelden, kann Office den Netzwerkdatenverkehr bis zu einem günstigeren Zeitpunkt blockieren.
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a>Parameter

 _nspType_
  
Ein Flag, das definiert, welche Kosten heuristisch abgefragt werden sollen. Weitere Informationen finden Sie unter [enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType). 
  
 _pfSyncEnabled_
  
Gibt an, ob die angeforderte Kosten Heuristik derzeit außer Kraft gesetzt wird. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a>ILSCLocalSyncClient:: GetFileStatus

GetFileStatus wird verwendet, um Informationen zu einer bestimmten Datei zu sammeln: ob Sie im Cache vorhanden ist, wenn Sie ausstehende Kommunikation mit der Serverkopie hat, und wenn Office 2013 über die neuesten Daten aus der lokalen Kopie verfügt. Es erfordert ein bitweises Flag von [enum-LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) -Werten, um zu bestimmen, welche Informationen das CSISYNCCLIENT-com-Objekt Abfragen soll. 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Die Zeichenfolge, die die Datei auf dem Client identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein. 
  
 _sfRequestedStatus_
  
Ein Flag, das angibt, welche Informationen zurückgegeben werden sollen. Weitere Informationen finden Sie unter [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
 _pbstrFileSystemPath_
  
Die Zeichenfolge, die den Speicherort der von _bstrResourceID_ auf dem Client angegebenen Datei identifiziert. Darf nicht NULL sein. 
  
 _pbstrETag_
  
Eine Zeichenfolge, die das eTag für die durch _bstrResourceID_angegebene Datei enthält. Darf nicht NULL sein. 
  
 _psfFileStatus_
  
Eine Kennzeichnung, die den über _sfRequestedStatus_ angeforderten Status für die durch _bstrResourceID_angegebene Datei enthält. Darf nicht NULL sein. Weitere Informationen finden Sie unter [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag). 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die von _bstrResourceID_ angegebenen Dateiinformationen sind nicht im Cache vorhanden.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |LSCStatusFlag_LocalFileUnchanged wurde angefordert, oder die von _bstrResourceID_ angegebene Datei ist gesperrt oder fehlt.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a>ILSCLocalSyncClient:: GetSupportedFileExtensions
<a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a>

GetSupportedFileExtensions gibt eine Liste mit Pipe-getrennten Dateierweiterungen zurück, die derzeit vom CsiSyncClient-COM-Objekt unterstützt werden. Beachten Sie, dass sich diese Liste ändern kann und der Consumer über das IPartnerActivityCallback-Objekt, das in [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) bereitgestellt wird, über eine Änderung benachrichtigt wird (siehe EventOccured). 
  
Ein Beispiel für die zurückgegebene Zeichenfolge lautet wie folgt: "| docx | DOCM | PPTX |"
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a>Parameter

 _pbstrSupportedFileExtensions_
  
Eine Zeichenfolge, die mit einem durch Pipe getrennten Satz von Dateierweiterungen festgelegt werden soll, der vom CsiSyncClient-COM-Objekt unterstützt wird. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a>ILSCLocalSyncClient:: Initialize
<a name="ILSCLocalSyncClient_Initialize"> </a>

Initialize muss die erste aufgerufene Methode sein. Andernfalls gibt alle anderen APIs E_LSC_NOTINITIALIZED zurück. Durch Aufrufen von Initialize für ein bereits initialisiertes Objekt wird S_OK zurückgegeben, und es wird nichts ausgeführt. Wenn E_LSC_CACHEMISMATCH zurückgegeben wird, ruft der Aufrufer möglicherweise [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) auf, um den Cache zu löschen, der mit der angegebenen angegebenen-verknüpft ist. In diesem Fall werden jedoch auch andere APIs E_LSC_NOTINITIALIZED zurückgeben. 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a>Parameter

 _bstrSuppliedID_
  
Identifiziert den Consumer und den zu verwendenden Cache. Muss mit maximal 32 Zeichen nicht leer sein. 
  
 _bstrProgID_
  
Identifiziert das COM-Objekt des Consumers für die bidirektionale Kommunikation. Muss mit maximal 39 Zeichen nicht leer sein. Weitere Informationen zu ProgIDs finden Sie unter [ \<ProgID\> -Schlüssel](https://docs.microsoft.com/windows/desktop/com/-progid--key) . 
  
 _bstrFileSystemDirectoryHint_
  
Identifiziert den Verzeichnisstamm, in dem lokale Dateien gespeichert werden. Muss mit maximal 256 Zeichen nicht leer sein. Das Verzeichnis muss bereits vorhanden sein. 
  
 _pEventCallback_
  
Die Rückrufschnittstelle, die CsiSyncClient bei Änderungen benachrichtigt. Weitere Informationen finden Sie unter IPartnerActivityCallback:: EventOccurred. Dieser Wert darf nicht NULL sein. 
  
 _pfCreatedNewCache_
  
Gibt zurück, ob ein neuer Cache erstellt wurde. Wenn kein Cache mit der BereitgeStellten-Nr verknüpft ist, wird eine erstellt. Dieser Wert darf nicht NULL sein.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CACHEMISMATCH  <br/> |Ein BereitgeStellter-ID hat bereits einen Cache zugeordnet, hat jedoch eine andere ProgId oder FileSystemDirectoryHint als die bereitgestellten.  <br/> |
|E_LSC_DIRECTORYHINTCONFLICT  <br/> |Der FileSystemDirectoryHint (oder ein Unterordner) ist bereits in einem anderen Cache vorhanden.  <br/> |
|E_LAC_PROGIDCONFLICT  <br/> |Die ProgID ist bereits in einem anderen Cache vorhanden.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a>ILSCLocalSyncClient:: LocalFileChange
<a name="ILSCLocalSyncClient_LocalFileChange"> </a>

LocalFileChange wird verwendet, um das CsiSyncClient-COM-Objekt anzuweisen, die angegebene Datei hochzuladen. Die-Methode bereitet die Datei für den Upload vor, einschließlich des Lesens der aktuellen Inhalte der Datei. Wenn ein Upload bereits aussteht, wird der vorherige Upload verworfen und der neue Inhalt für den Upload vorbereitet. Wenn die Datei zur Bearbeitung in einer Anwendung geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei für den Upload vorzubereiten (die Anwendung sollte diesen Schritt bereits ausführen, falls Änderungen vorgenommen werden).
  
Diese Methode lässt Uploads zu, wenn Sie als zuvor blockierte Uploads markiert wurde (siehe [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)renamedatei).
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

 _bstrFileSystemPath_
  
Eine Zeichenfolge, die die Datei auf dem Client identifiziert. Bei diesem Wert muss es sich um einen nicht leeren lokalen Pfad mit maximal 256 Zeichen handeln. Dieser Pfad muss sich in der vom FileSystemDirectoryHint angegebenen Verzeichnisstruktur befinden, wenn der Aufruf von [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) vorgenommen wurde. 
  
 _bstrResourceID_
  
Ein String-Wert, der die Resource-Kennung der Datei identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein. 
  
 _bstrWebPath_
  
Eine Zeichenfolge, die die Datei auf dem Server identifiziert. Dieser Wert muss nicht leer, gültige URL, aber nicht mehr als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427definiert. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Die von _bstrFileSystemPath_ angegebene Datei hat eine andere Resourcen-als die angegebene. Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird. Weitere Informationen finden Sie unter [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)GetChanges.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Datei wurde in der Mitte des Vorgangs gelöscht.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Die angegebene Dateierweiterung wird vom CsiSyncClient-COM-Objekt nicht unterstützt. Weitere Informationen finden Sie unter [ILSCLocalSyncClient:: GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).  <br/> |
|E_LSC_FILEUPTODATE  <br/> |Das COM-Objekt hat keinen Upload geplant, weil die Datei im Cache die neuesten Änderungen vom Datenträger hatte.  <br/> |
|E_LSC_LOCALFILEUNAVAILABLE  <br/> |Die von _bstrFileSystemPath_ angegebene Datei fehlt oder ist gesperrt.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der von der FileSystemDirectoryHint angegeben wurde, wenn der Aufruf von Initialize ausgeführt wurde.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Die von _bstrResourceID_ angegebene Datei hat eine andere FileSystemPath als angegeben.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei weist bereits ausstehende Änderungen in einem anderen Cache auf und kann dem Consumer-Cache noch nicht zugeordnet werden.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Der bereitgestellte webPath fällt unter einen anderen Cache.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a>ILSCLocalSyncClient:: renamedatei
<a name="ILSCLocalSyncClient_RenameFile"> </a>

Mit der renamedatei wird eine neue URL und ein lokaler Pfad für eine bestimmte resourcecollection zugeordnet. Wenn die durch die resourcecollection angegebene Datei nicht bereits im Cache vorhanden ist, wird versucht, Sie zu erstellen und zum herunterladen zu markieren.
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a>Parameter

 _bstrResourceID_
  
Ein String-Wert, der die Resource-Kennung der Datei identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein. 
  
 _bstrNewFileSystemPath_
  
Eine Zeichenfolge, die den neuen lokalen Pfad für die Datei angibt. Bei diesem Wert muss es sich um einen nicht leeren lokalen Pfad mit maximal 256 Zeichen handeln. Dieser Pfad muss sich in der vom FileSystemDirectoryHint angegebenen Verzeichnisstruktur befinden, wenn der Aufruf von Initialize ausgeführt wurde. 
  
 _bstrNewWebPath_
  
Eine Zeichenfolge, die die neue URL für die Datei angibt. Bei diesem Wert muss es sich um eine nicht leere gültige URL handeln, aber nicht länger als INTERNET_MAX_URL_LENGTH https://support.microsoft.com/kb/208427, wie von definiert. 
  
 _fBlockUploads_
  
Gibt an, ob Uploads an den neuen Speicherort derzeit zulässig sind. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Die _bstrNewFileSystemPath_ oder _bstrNewWebPath_ sind bereits in einer anderen Datei in einem beliebigen Cache vorhanden. Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird. Weitere Informationen finden Sie unter [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)GetChanges.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Dateiinformationen wurden während dieser Methode aus dem Cache gelöscht.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der von der FileSystemDirectoryHint angegeben wurde, wenn der Aufruf von Initialize ausgeführt wurde.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei wird derzeit in einer Office-Anwendung synchronisiert.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a>ILSCLocalSyncClient:: ResetCache
<a name="ILSCLocalSyncClient_ResetCache"> </a>

ResetCache löscht den Cache, der der bei Initialize bereitgestellten Bereitstellung zugeordnet ist. Hierzu gehören alle Dateiinformationen, die Dateien werden jedoch sowohl auf dem Client als auch auf dem Server belassen. Diese Methode verlässt auch das Objekt in einem teilweise nicht initialisierten Zustand. Die einzigen gültigen Aufrufe sind [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) oder [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize). Diese Methode kann aufgerufen werden, wenn Initialize fehlschlägt und E_LSC_CACHEMISMATCH zurückgegeben wird, und löscht den Cache, der mit der angegebenen mit dem fehlerhaften Aufruf bereitgestellten-Wert verknüpft ist.
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a>Parameter

Keine
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Aufruf ist fehlerhaft.  <br/> |
|E_LSC_NOTINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a>ILSCLocalSyncClient:: ServerFileChange
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

ServerFileChange weist das CsiSyncClient-COM-Objekt an, die angegebene Datei zum herunterladen zu markieren. Wenn die Datei in einer Office-Anwendung zur Bearbeitung geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei zum herunterladen zu markieren (die Anwendung sollte diesen Schritt bereits ausführen, falls Änderungen vorgenommen werden).
  
Diese Methode ermöglicht Downloads, wenn Sie als Downloads gekennzeichnet wurde, die zuvor blockiert wurden (siehe renamedatei).
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a>Parameter

|Parameter|Beschreibung|
|:-----|:-----|
|bstrFileSystemPath  <br/> |Eine Zeichenfolge, die die Datei auf dem Client identifiziert. Bei diesem Wert muss es sich um einen nicht leeren lokalen Pfad mit maximal 256 Zeichen handeln. Dieser Pfad muss sich in der vom FileSystemDirectoryHint angegebenen Verzeichnisstruktur befinden, wenn der Aufruf von Initialize ausgeführt wurde.  <br/> |
|bstrResourceID  <br/> |Ein String-Wert, der die Resource-Kennung der Datei identifiziert. Dieser Wert muss mit maximal 128 Zeichen nicht leer sein.  <br/> |
|bstrWebPath  <br/> |Eine Zeichenfolge, die die Datei auf dem Server identifiziert. Bei diesem Wert muss es sich um eine nicht leere gültige URL handeln, aber nicht länger als INTERNET_MAX_URL_LENGTH, https://support.microsoft.com/kb/208427wie von definiert.  <br/> |
   
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Cache Verbindungsstatus wird nicht festgelegt.  <br/> |
|E_LSC_CONFLICTINGFILE  <br/> |Die von _bstrFileSystemPath_ angegebene Datei hat eine andere Resourcen-als die angegebene.  <br/> |
|E_LSC_FILENOTSUPPORTED  <br/> |Die angegebene Dateierweiterung wird vom CsiSyncClient-COM-Objekt nicht unterstützt. Siehe GetSupportedFileExtensions.  <br/> |
|E_LSC_FILENOTFOUND  <br/> |Die Datei wurde in der Mitte des Vorgangs gelöscht.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_LOCALPATHNOTMAPPED  <br/> |Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der von der FileSystemDirectoryHint angegeben wurde, wenn der Aufruf von Initialize ausgeführt wurde.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|E_LSC_PATHMISMATCH  <br/> |Die von _bstrResourceID_ angegebene Datei hat eine andere FileSystemPath als angegeben.  <br/> |
|E_LSC_PENDINGCHANGESINCACHE  <br/> |Die angegebene Datei weist bereits ausstehende Änderungen in einem anderen Cache auf und kann dem Consumer-Cache noch nicht zugeordnet werden.  <br/> |
|E_LSC_SERVERPATHINDIFFERENTCACHE  <br/> |Der bereitgestellte webPath fällt unter einen anderen Cache.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a>ILSCLocalSyncClient:: SetClientConnectivityState
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

Legt den Cache in einen Online-oder Offlinestatus fest. Im Offlinemodus versucht Office nicht, mit dem Server für Dateien in diesem Cache zu kommunizieren, unabhängig von der _fBlockUploads_ -Einstellung jeder einzelnen Datei. 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a>Parameter

 _fIsOnline_
  
Ein boolescher Wert, der den Verbindungsstatus des Caches bestimmt. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Der Cache Verbindungsstatus wird nicht festgelegt.  <br/> |
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a>ILSCLocalSyncClient:: SetClientNetworkSyncPermission
<a name="ILSCLocalSyncClient_ServerFileChange"> </a>

SetClientNetworkSyncPermission wird verwendet, um die heuristischen Heuristiken von restoreOffice für Netzwerkkosten und Stromverbrauch zu überschreiben. Wenn Sie sich in einem 3G-oder einem anderen hochkosten Netzwerk oder bei Batteriebetrieb im Vergleich mit dem Stromnetz anmelden, kann Office den Netzwerkdatenverkehr bis zu einem günstigeren Zeitpunkt blockieren. Der Consumer dieser API kann damit die Heuristiken von Office außer Kraft setzen und die Synchronisierung erzwingen.
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a>Parameter

 _nspType_
  
Ein Flag, das definiert, welche Kosten heuristisch überschrieben werden. Weitere Informationen finden Sie unter [enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).
  
 _fEnableSync_
  
Gibt an, ob die Synchronisierung mit erzwungen wird, wodurch diese Kosten Heuristik überschrieben wird oder nicht mehr überschrieben wird. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Die Synchronisierungs Heuristik wird nicht außer Kraft gesetzt.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a>ILSCLocalSyncClient:: Uninitialize
<a name="ILSCLocalSyncClient_Uninitialize"> </a>

Entlädt den Cache aus dem COM-Objekt und führt Schließvorgänge aus. [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUSS vor dem Zerstören des COM-Objekts aufgerufen werden. Nachdem Sie aufgerufen wurden, können keine anderen APIs aufgerufen werden, das COM-Objekt muss zerstört und eine neue erstellt werden, wenn Sie den Vorgang fortsetzen möchten. 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a>Parameter

Keine.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Nicht deinitialisieren.  <br/> |
|E_LSC_NOINITIALIZED  <br/> |[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.  <br/> |
|S_OK  <br/> |Der Aufruf war erfolgreich.  <br/> |
   
### <a name="interface-ienumlscevent"></a>Schnittstelle IEnumLSCEvent

Diese Schnittstelle stellt eine Liste von ILSCEvent-Ereignissen dar.
  
**Öffentliche Memberfunktionen**

#### <a name="ienumlsceventfnext"></a>IEnumLSCEvent:: FNext

Ruft das nächste Ereignis aus der Liste der Ereignisse ab.
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a>Parameter

 _ppiLSCEvent_
  
Ein Zeiger auf eine ILSCEvent-Schnittstelle.
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_FAIL  <br/> |Es sind keine weiteren Ereignisse mehr vorhanden.  <br/> |
|S_OK  <br/> |Der Anruf wurde erfolgreich ausgeführt.  <br/> |
   
#### <a name="ienumlsceventreset"></a>IEnumLSCEvent:: Reset

Setzt den Enumerator auf das erste Ereignis zurück.
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a>Parameter

Keine.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
### <a name="interface-ilscevent"></a>Schnittstelle ILSCEvent

Diese Schnittstelle stellt ein Synchronisierungsereignis dar. Alle Informationen über das Ereignis können von der Benutzeroberfläche abgerufen werden.
  
**Öffentliche Memberfunktionen**

#### <a name="ilsceventgetconflictstatus"></a>ILSCEvent:: GetConflictStatus

Beachten Sie, dass dieser Wert aufgefüllt wird, wenn [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) GetChanges aufgerufen wird, nicht beim Erstellen des Ereignisses, sodass Sie nur den aktuellen Status der Datei und nicht den Status der Datei haben, wenn der Konfliktstatus geändert wurde. 
  
Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnLocalConflictStateChanged ist. 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a>Parameter

 _pfIsInConflict_
  
Der aktuelle Konfliktstatus der Datei, die dem Ereignis zugeordnet ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgeterror"></a>ILSCEvent:: getError

Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a>Parameter

 _pnError_
  
Der mit diesem Ereignis verknüpfte Fehler.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetetag"></a>ILSCEvent:: getETag

Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a>Parameter

 _pbstrETag_
  
Das mit diesem Ereignis verknüpfte ETag
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgeteventtype"></a>ILSCEvent:: getEventtype

Ruft den Typ für dieses Ereignis ab.
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a>Parameter

 _pnEventType_
  
Der Ereignistyp dieses Ereignisses. Weitere Informationen finden Sie unter [enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for Valid values. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|S_OK  <br/> |Der Anruf wurde erfolgreich ausgeführt.  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a>ILSCEvent:: GetLocalWorkingPath

Ruft den lokalen Arbeitspfad für dieses Ereignis ab.
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a>Parameter

 _pbstrLocalWorkingPath_
  
Der lokale Pfad der Datei, auf die sich dieses Ereignis bezieht. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetresourceid"></a>ILSCEvent:: GetResource-Nr.

Ruft die Ressourcen-ID für das Ereignis ab.
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a>Parameter

 _pbstrResourceID_
  
Die resourcecollection der Datei, die diesem Ereignis zugeordnet ist.
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetresourceidattempted"></a>ILSCEvent:: GetResourceIDAttempted

Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist. Wenn ein Aufruf von [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) renamedatei einen Webpfad oder einen lokalen Pfad Konflikt mit einer anderen Datei im Office-Dateicache verursacht, Ereignis generiert. 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a>Parameter

 _pbstrResourceIDAttempted_
  
Die resourcecollection, die das Generieren dieses Ereignisses verursacht hat. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
#### <a name="ilsceventgetsyncerrortype"></a>ILSCEvent:: GetSyncErrorType

Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist. 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a>Parameter

 _pnSyncErrorType_
  
Der diesem Ereignis zugeordnete Fehlertyp. Weitere Informationen finden Sie unter [enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for Potential values. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_INVALIDARG  <br/> |Mindestens ein Parameter ist ungültig.  <br/> |
|S_OK  <br/> |Der Anruf wurde erfolgreich ausgeführt.  <br/> |
   
#### <a name="ilsceventgetwebpath"></a>ILSCEvent:: GetWebPath

Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist. 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a>Parameter

 _pbstrWebPath_
  
Gibt den webPfad an, der diesem Ereignis zugeordnet ist. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück. 
  
### <a name="interface-ilscevent2"></a>Schnittstelle ILSCEvent2

Diese Schnittstelle enthält zusätzliche Informationen zu einem Synchronisierungsereignis.
  
**Öffentliche Memberfunktionen**

#### <a name="ilscevent2geterrorchain"></a>ILSCEvent2:: GetErrorChain

Ruft die Fehler Kette Informationen zu einem Synchronisierungsereignis ab.
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a>Parameter

 _pbstrErrorChain_
  
Eine Zeichenfolge, die die Fehler Ketten Informationen enthalten soll. Darf nicht NULL sein. 
  
##### <a name="return-values"></a>Rückgabewerte

|Wert|Beschreibung|
|:-----|:-----|
|E_NOTIMPL  <br/> |Diese Schnittstelle wird von der installierten Office-Version nicht unterstützt.  <br/> |
|E_INVALIDARG  <br/> |Mindestens einer der Parameterwerte ist ungültig.  <br/> |
|E_FAIL  <br/> |Die Fehler Ketten Informationen sind nicht verfügbar.  <br/> |
|S_OK  <br/> |Der Anruf wurde erfolgreich ausgeführt.  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a>Schnittstelle IPartnerActivityCallback

Diese Schnittstelle stellt eine Rückruffunktion für das CSISyncClient-COM-Objekt bereit.
  
**Öffentliche Memberfunktionen**

#### <a name="ipartneractivitycallbackeventoccurred"></a>IPartnerActivityCallback:: EventOccurred

Hierbei handelt es sich um eine Rückruffunktion für das Objekt, das für das CsiSyncClient-COM-Objekt angegeben wurde. Es wird erwartet, dass beim Eintreten eines Ereignisses (siehe [enum-LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) für gültige Ereignistypen) das CSISYNCCLIENT-com-Objekt diese Methode aufruft, um den Consumer zu signalisieren. 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a>Parameter

 _eEventTypeOccurred_
  
Der Ereignistyp dieses Ereignisses. Weitere Informationen finden Sie unter [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for Valid values. 
  
##### <a name="return-values"></a>Rückgabewerte

Gibt immer S_OK zurück.
  
## <a name="enumerations"></a>Enumerationen

CSISyncClient verwendet die folgenden Enumerationen.
  
### <a name="enum-lsceventsyncerrortype"></a>Enum-LSCEventSyncErrorType
<a name="Enum_LSCEventSyncErrorType"> </a>

Diese Enumeration gibt die Fehlerkategorien an, die beim Synchronisieren einer Datei auftreten können.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventSyncErrorType_UserInterventionRequiredUnexpected  <br/> |Der Synchronisierungsfehler dieses Ereignisses war unerwartet und erfordert möglicherweise besondere Überlegungen. In der Standardeinstellung muss der Benutzer möglicherweise eingreifen.  <br/> |
|LSCEventSyncErrorType_NoInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert keine besondere Überlegung. Office behandelt es automatisch.  <br/> |
|LSCEventSyncErrorType_UserInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass ein Benutzer diesen auflöst. Beispielsweise muss ein Benutzer beim Zusammenführen von Konflikten das Dokument öffnen und zusammenführen.  <br/> |
|LSCEventSyncErrorType_WaitingOnClient  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Consumer eingreift, aber keine besondere Überlegung durch den Benutzer erfordert.  <br/> |
|LSCEventSyncErrorType_ClientInterventionRequired  <br/> |Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Consumer als Sonderfall interveniert.  <br/> |
|LSCEventSyncErrorType_Max  <br/> ||
   
### <a name="enum-lsceventtype"></a>Enum-LSCEventType
<a name="Enum_LSCEventType"> </a>

Diese Enumeration gibt den Typ der Ereignisse an, die für eine bestimmte Datei auftreten können.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventType_None  <br/> ||
|LSCEventType_OnLocalChanges  <br/> |Änderungen wurden an einer lokalen Datei vorgenommen.  <br/> |
|LSCEventType_OnOpenedByUser  <br/> |Ein Benutzer hat eine Datei geöffnet.  <br/> |
|LSCEventType_OnServerChangesDownloaded  <br/> |Dateiänderungen wurden vom Server heruntergeladen.  <br/> |
|LSCEventType_OnLocalChangesUploaded  <br/> |Hochladen von Dateiänderungen auf den Server abgeschlossen.  <br/> |
|LSCEventType_OnLocalConflictStateChanged  <br/> |Der Merge-Konfliktstatus einer Datei wurde geändert.  <br/> |
|LSCEventType_OnFileAdded  <br/> |Eine Datei wurde hinzugefügt.  <br/> |
|LSCEventType_OnFileDeleted  <br/> |Eine Datei wurde gelöscht.  <br/> |
|LSCEventType_OnSyncEnabled  <br/> |Die Synchronisierung wurde für die Dateien eines Benutzers aktiviert.  <br/> |
|LSCEventType_OnServerChangesDownloadStarted  <br/> |Dateiänderungen wurden vom Server heruntergeladen.  <br/> |
|LSCEventType_OnLocalChangesUploadStarted  <br/> |Mit dem Hochladen von Dateiänderungen auf den Server begonnen.  <br/> |
|LSCEventType_OnFilePathConflict  <br/> |Dieses Ereignis wird generiert, wenn ein Aufruf von [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) renameDatei bewirkt, dass ein Webpfad oder ein lokaler Pfad Konflikt mit einer anderen Datei in der Office-Dateicache.  <br/> |
|LSCEventType_OnFileForked  <br/> ||
|LSCEventType_Max  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a>Enum-LSCEventTypeOccurred
<a name="Enum_LSCEventTypeOccurred"> </a>

Diese Enumeration gibt den Typ der Ereignisse an, die auftreten können. Der Consumer muss bestimmte ILSCLocalSyncClient-Funktionen basierend auf dem Ereignistyp aufrufen.
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LSCEventTypeOccurred_GetChanges  <br/> |Ein ILSCEvent ist aufgetreten. Der Consumer sollte [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) GetChanges aufrufen, um die Daten abzurufen.  <br/> |
|LSCEventTypeOccurred_GetSupportedFileExtensions  <br/> |Die unterstützten Dateierweiterungen wurden geändert. Der Consumer sollte [ILSCLocalSyncClient:: GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) aufrufen, um die neue Liste unterstützter Erweiterungen abzurufen.  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a>Enum-LSCNetworkSyncPermissionType
<a name="Enum_LSCNetworkSyncPermissionType"> </a>

Diese Enumeration gibt die Flags an, die für eine heuristische Netzwerkkosten verwendet werden. 

|Enumerator|Beschreibung|
|:-----|:-----|
|LSCNetworkSyncPermissionType_HighCost  <br/> |True, wenn die Kosten Heuristik für teure Netzwerke (wie 3G) überschrieben wird.  <br/> |
|LSCNetworkSyncPermissionType_HighPowerUsage  <br/> |True, wenn die Kosten Heuristik für Energieverbrauch (wie eine Batterie) überschrieben wird.  <br/> |
   
### <a name="enum-lscstatusflag"></a>Enum-LSCStatusFlag
<a name="Enum_LSCStatusFlag"> </a>

Diese Enumeration wird verwendet, um den Synchronisierungsstatus einer Datei darzustellen. 
  
|Enumerator|Beschreibung|
|:-----|:-----|
|LCSStatusFlag_None  <br/> ||
|LSCStatusFlag_UploadPending  <br/> |True, wenn ausstehende Daten an die Server Datei gesendet werden.  <br/> |
|LSCStatusFlag_DownloadPending  <br/> |True, wenn die Daten aus der Server Datei heruntergeladen werden müssen.  <br/> |
|LSCStatusFlag_LocalFileUnchanged  <br/> |True, wenn sich das Daten Büro in der Datei in seinem Cache befindet, ist die neueste Kopie der Daten auf dem Datenträger.  <br/> |
   

