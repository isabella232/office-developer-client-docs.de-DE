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
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="8cb01-103">Verwenden von CSISyncClient zum Steuern des Office-Dokument Caches (ODC)</span><span class="sxs-lookup"><span data-stu-id="8cb01-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="8cb01-104">Erfahren Sie, wie Sie CSISyncClient verwenden, um den Office-Dokument Cache (ODC) zu steuern.</span><span class="sxs-lookup"><span data-stu-id="8cb01-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="8cb01-105">CSISyncClient ist ein prozessinterner COM-Server (CsiSyncClient. exe), der es Microsoft OneDrive ermöglicht, das Verhalten des Office-Dokument Caches (ODC) zu steuern.</span><span class="sxs-lookup"><span data-stu-id="8cb01-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="8cb01-106">Beispielsweise kann OneDrive die ODC über CSISyncClient zum Hochladen und Herunterladen von Dateien zu und von MS-FSSHTTP-aktivierten Endpunkten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="8cb01-107">Dies ermöglicht erweiterte Dienst gesicherte Funktionen in Office, wie die gemeinsame Dokumenterstellung und nahtlose Übergänge zwischen Offline und online.</span><span class="sxs-lookup"><span data-stu-id="8cb01-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="8cb01-108">CsiSyncClient ist in Office Desktop (sowohl x86 als auch x64) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8cb01-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="8cb01-109">Hinweis: während neuere Versionen von Office möglicherweise mit CsiSyncClient ausgeliefert werden, wird der Prozess nur aus Gründen der Abwärtskompatibilität verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cb01-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="8cb01-110">Die CsiSyncClient-Schnittstelle und die Methodik der Überwachung von ODC werden in zukünftigen Versionen von Office geändert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="8cb01-111">Die Klassen-ID ist derzeit so festgelegt, dass Sie nur auf OneDrive antwortet.</span><span class="sxs-lookup"><span data-stu-id="8cb01-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="8cb01-112">Das COM-Objekt kann als out-of-proc-COM-Server verwendet werden und wird in CsiSyncClient. exe ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="8cb01-113">Aufgrund von Einschränkungen beim Zugriff (der von ODC verwendet wird), wird er mit dem Bit-Typ ausgeliefert, in dem Office eingeht, sodass x64 Office ein x64-COM-Objekt oder x86 Office ein x86-COM-Objekt bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="8cb01-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="8cb01-114">Um diese Einschränkung zu umgehen, muss das COM-Objekt als ein Out-of-proc-COM-Server gehostet werden, um die Bitanzahl-Kompatibilität zu ermöglichen, indem Sie CLSCTX_LOCAL_SERVER als Teil des CoCreateInstance angeben.</span><span class="sxs-lookup"><span data-stu-id="8cb01-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="8cb01-115">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="8cb01-115">Interfaces</span></span>

<span data-ttu-id="8cb01-116">CSISyncClient verwendet die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="8cb01-117">Schnittstelle ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="8cb01-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="8cb01-118">Dies ist die primäre Schnittstelle, die zum Synchronisieren von Dateien in Office verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="8cb01-119">ProgID: Office. LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="8cb01-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="8cb01-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="8cb01-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="8cb01-121">TypBibliothek: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="8cb01-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="8cb01-122">Das verfügbar gemachte COM-Objekt wird als out-of-proc-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="8cb01-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="8cb01-123">Die Angabe von CLSCTX_LOCAL_SERVER als Teil von CoCreateInstance ermöglicht die Kompatibilität zwischen 64bit-und 32bit-Prozessen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="8cb01-124">Nachdem Sie das COM-Objekt erstellt haben, müssen Sie zuerst [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="8cb01-125">Nachdem [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgreich abgeschlossen wurde, können Sie eine beliebige API beliebig oft und in beliebiger Reihenfolge aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="8cb01-126">Sie können auch [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) für ein bereits initialisiertes Objekt aufrufen, aber dies hat keine Funktion.</span><span class="sxs-lookup"><span data-stu-id="8cb01-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="8cb01-127">Die Ausnahmen vom vorherigen Absatz sind [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) und [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="8cb01-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="8cb01-128">Nachdem Sie [ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) für das COM-Objekt aufgerufen haben, müssen Sie dieses Objekt zerstören und eine neue erstellen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="8cb01-129">[ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) löscht den unter Cache, löscht alle zugehörigen Dateiinformationen im Cache, belässt die Dokumente jedoch auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="8cb01-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="8cb01-130">Außerdem bleibt der Status für die Kommunikation mit dem Cache intakt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="8cb01-131">Auf diese Weise können Sie [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erneut aufrufen, um einen neuen Cache zu erstellen, ohne das COM-Objekt zu zerstören und neu zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="8cb01-132">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="8cb01-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="8cb01-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="8cb01-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="8cb01-134">Delete File wird verwendet, um die Dateiinformationen aus dem Cache zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="8cb01-135">Diese Methode belässt jedoch die zugehörige Datei auf dem Datenträger und auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="8cb01-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-136">Parameters</span></span>

 <span data-ttu-id="8cb01-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="8cb01-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="8cb01-138">Die Zeichenfolge, die die Resourcen-Kennung der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="8cb01-139">Dieser Wert muss mit maximal 128 Zeichen nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-140">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-140">Return values</span></span>

|<span data-ttu-id="8cb01-141">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-141">Value</span></span>|<span data-ttu-id="8cb01-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-144">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-146">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-148">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="8cb01-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="8cb01-150">Die angegebene resourcecollection befindet sich nicht im Cache.</span><span class="sxs-lookup"><span data-stu-id="8cb01-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-152">Initialize wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="8cb01-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="8cb01-154">Die Datei wird derzeit synchronisiert oder geöffnet und kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="8cb01-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-155">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-156">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="8cb01-157">ILSCLocalSyncClient:: getChanges</span><span class="sxs-lookup"><span data-stu-id="8cb01-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="8cb01-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-158"></span></span>

<span data-ttu-id="8cb01-159">GetChanges gibt einen Enumerator von ILSCEvent-Objekten zurück und gibt auch ein Token zurück, das für den nächsten Aufruf von getChanges angegeben wird, vorausgesetzt, der Consumer hat den vorherigen Satz von Ereignissen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="8cb01-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="8cb01-160">Ereignisse vor dem angegebenen _nPreviousChangesToken_ werden gelöscht und sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8cb01-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="8cb01-161">Wenn keine zu verarbeitenden Ereignisse vorhanden sind, sollte _pnCurrentChangesToken_ den gleichen Wert wie _nPreviousChangesToken_aufweisen, aber _ppiEvents_ wird weiterhin festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-162">Parameters</span></span>

 <span data-ttu-id="8cb01-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="8cb01-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="8cb01-164">Gibt an, welches Ereignis zuletzt vom Consumer verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="8cb01-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="8cb01-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="8cb01-166">Gibt das letzte Ereignis an, das dem Consumer übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="8cb01-167">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-167">Must not be null.</span></span>
  
 <span data-ttu-id="8cb01-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="8cb01-168">_ppiEvents_</span></span>
  
<span data-ttu-id="8cb01-169">Ein Enumerator für die Ereignisse, die dem Consumer übergeben wurden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="8cb01-170">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-171">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-171">Return values</span></span>

|<span data-ttu-id="8cb01-172">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-172">Value</span></span>|<span data-ttu-id="8cb01-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-175">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-177">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-179">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-180">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-181">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="8cb01-182">ILSCLocalSyncClient:: GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="8cb01-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="8cb01-183">GetClientNetworkSyncPermission wird verwendet, um abzufragen, ob die Synchronisierungs Heuristik von Office für Netzwerkkosten und Energieverbrauch außer Kraft gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="8cb01-184">Wenn Sie sich in einem 3G-oder einem anderen hochkosten Netzwerk oder bei Batteriebetrieb im Vergleich mit dem Stromnetz anmelden, kann Office den Netzwerkdatenverkehr bis zu einem günstigeren Zeitpunkt blockieren.</span><span class="sxs-lookup"><span data-stu-id="8cb01-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-185">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-185">Parameters</span></span>

 <span data-ttu-id="8cb01-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="8cb01-186">_nspType_</span></span>
  
<span data-ttu-id="8cb01-187">Ein Flag, das definiert, welche Kosten heuristisch abgefragt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="8cb01-188">Weitere Informationen finden Sie unter [enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="8cb01-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="8cb01-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="8cb01-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="8cb01-190">Gibt an, ob die angeforderte Kosten Heuristik derzeit außer Kraft gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="8cb01-191">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-192">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-192">Return values</span></span>

|<span data-ttu-id="8cb01-193">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-193">Value</span></span>|<span data-ttu-id="8cb01-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-196">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-198">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-200">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-201">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-202">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="8cb01-203">ILSCLocalSyncClient:: GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="8cb01-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="8cb01-204">GetFileStatus wird verwendet, um Informationen zu einer bestimmten Datei zu sammeln: ob Sie im Cache vorhanden ist, wenn Sie ausstehende Kommunikation mit der Serverkopie hat, und wenn Office 2013 über die neuesten Daten aus der lokalen Kopie verfügt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="8cb01-205">Es erfordert ein bitweises Flag von [enum-LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) -Werten, um zu bestimmen, welche Informationen das CSISYNCCLIENT-com-Objekt Abfragen soll.</span><span class="sxs-lookup"><span data-stu-id="8cb01-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-206">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-206">Parameters</span></span>

 <span data-ttu-id="8cb01-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="8cb01-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="8cb01-208">Die Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="8cb01-209">Dieser Wert muss mit maximal 128 Zeichen nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="8cb01-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="8cb01-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="8cb01-211">Ein Flag, das angibt, welche Informationen zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-211">A flag which defines what information to return.</span></span> <span data-ttu-id="8cb01-212">Weitere Informationen finden Sie unter [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="8cb01-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="8cb01-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="8cb01-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="8cb01-214">Die Zeichenfolge, die den Speicherort der von _bstrResourceID_ auf dem Client angegebenen Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="8cb01-215">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-215">Must not be null.</span></span> 
  
 <span data-ttu-id="8cb01-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="8cb01-216">_pbstrETag_</span></span>
  
<span data-ttu-id="8cb01-217">Eine Zeichenfolge, die das eTag für die durch _bstrResourceID_angegebene Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="8cb01-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="8cb01-218">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-218">Must not be null.</span></span> 
  
 <span data-ttu-id="8cb01-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="8cb01-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="8cb01-220">Eine Kennzeichnung, die den über _sfRequestedStatus_ angeforderten Status für die durch _bstrResourceID_angegebene Datei enthält.</span><span class="sxs-lookup"><span data-stu-id="8cb01-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="8cb01-221">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-221">Must not be null.</span></span> <span data-ttu-id="8cb01-222">Weitere Informationen finden Sie unter [enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="8cb01-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-223">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-223">Return values</span></span>

|<span data-ttu-id="8cb01-224">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-224">Value</span></span>|<span data-ttu-id="8cb01-225">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-227">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-229">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="8cb01-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="8cb01-231">Die von _bstrResourceID_ angegebenen Dateiinformationen sind nicht im Cache vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8cb01-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="8cb01-233">LSCStatusFlag_LocalFileUnchanged wurde angefordert, oder die von _bstrResourceID_ angegebene Datei ist gesperrt oder fehlt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="8cb01-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-235">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-236">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-237">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="8cb01-238">ILSCLocalSyncClient:: GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="8cb01-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="8cb01-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-239"></span></span>

<span data-ttu-id="8cb01-240">GetSupportedFileExtensions gibt eine Liste mit Pipe-getrennten Dateierweiterungen zurück, die derzeit vom CsiSyncClient-COM-Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="8cb01-241">Beachten Sie, dass sich diese Liste ändern kann und der Consumer über das IPartnerActivityCallback-Objekt, das in [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) bereitgestellt wird, über eine Änderung benachrichtigt wird (siehe EventOccured).</span><span class="sxs-lookup"><span data-stu-id="8cb01-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="8cb01-242">Ein Beispiel für die zurückgegebene Zeichenfolge lautet wie folgt: "| docx | DOCM | PPTX |"</span><span class="sxs-lookup"><span data-stu-id="8cb01-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-243">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-243">Parameters</span></span>

 <span data-ttu-id="8cb01-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="8cb01-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="8cb01-245">Eine Zeichenfolge, die mit einem durch Pipe getrennten Satz von Dateierweiterungen festgelegt werden soll, der vom CsiSyncClient-COM-Objekt unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="8cb01-246">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-247">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-247">Return values</span></span>

|<span data-ttu-id="8cb01-248">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-248">Value</span></span>|<span data-ttu-id="8cb01-249">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-251">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-253">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-255">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-256">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-257">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="8cb01-258">ILSCLocalSyncClient:: Initialize</span><span class="sxs-lookup"><span data-stu-id="8cb01-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="8cb01-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-259"></span></span>

<span data-ttu-id="8cb01-260">Initialize muss die erste aufgerufene Methode sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-260">Initialize must be the first method called.</span></span> <span data-ttu-id="8cb01-261">Andernfalls gibt alle anderen APIs E_LSC_NOTINITIALIZED zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="8cb01-262">Durch Aufrufen von Initialize für ein bereits initialisiertes Objekt wird S_OK zurückgegeben, und es wird nichts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="8cb01-263">Wenn E_LSC_CACHEMISMATCH zurückgegeben wird, ruft der Aufrufer möglicherweise [ILSCLocalSyncClient:: ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) auf, um den Cache zu löschen, der mit der angegebenen angegebenen-verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="8cb01-264">In diesem Fall werden jedoch auch andere APIs E_LSC_NOTINITIALIZED zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="8cb01-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-265">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-265">Parameters</span></span>

 <span data-ttu-id="8cb01-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="8cb01-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="8cb01-267">Identifiziert den Consumer und den zu verwendenden Cache.</span><span class="sxs-lookup"><span data-stu-id="8cb01-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="8cb01-268">Muss mit maximal 32 Zeichen nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="8cb01-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="8cb01-269">_bstrProgID_</span></span>
  
<span data-ttu-id="8cb01-270">Identifiziert das COM-Objekt des Consumers für die bidirektionale Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="8cb01-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="8cb01-271">Muss mit maximal 39 Zeichen nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="8cb01-272">Weitere Informationen zu ProgIDs finden Sie unter [ \<ProgID\> -Schlüssel](https://docs.microsoft.com/windows/desktop/com/-progid--key) .</span><span class="sxs-lookup"><span data-stu-id="8cb01-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="8cb01-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="8cb01-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="8cb01-274">Identifiziert den Verzeichnisstamm, in dem lokale Dateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="8cb01-275">Muss mit maximal 256 Zeichen nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="8cb01-276">Das Verzeichnis muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="8cb01-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="8cb01-277">_pEventCallback_</span></span>
  
<span data-ttu-id="8cb01-278">Die Rückrufschnittstelle, die CsiSyncClient bei Änderungen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="8cb01-279">Weitere Informationen finden Sie unter IPartnerActivityCallback:: EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="8cb01-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="8cb01-280">Dieser Wert darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="8cb01-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="8cb01-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="8cb01-282">Gibt zurück, ob ein neuer Cache erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="8cb01-283">Wenn kein Cache mit der BereitgeStellten-Nr verknüpft ist, wird eine erstellt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="8cb01-284">Dieser Wert darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-285">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-285">Return values</span></span>

|<span data-ttu-id="8cb01-286">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-286">Value</span></span>|<span data-ttu-id="8cb01-287">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-289">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-291">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="8cb01-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="8cb01-293">Ein BereitgeStellter-ID hat bereits einen Cache zugeordnet, hat jedoch eine andere ProgId oder FileSystemDirectoryHint als die bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="8cb01-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="8cb01-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="8cb01-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="8cb01-295">Der FileSystemDirectoryHint (oder ein Unterordner) ist bereits in einem anderen Cache vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="8cb01-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="8cb01-297">Die ProgID ist bereits in einem anderen Cache vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-298">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-299">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="8cb01-300">ILSCLocalSyncClient:: LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="8cb01-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="8cb01-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-301"></span></span>

<span data-ttu-id="8cb01-302">LocalFileChange wird verwendet, um das CsiSyncClient-COM-Objekt anzuweisen, die angegebene Datei hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="8cb01-303">Die-Methode bereitet die Datei für den Upload vor, einschließlich des Lesens der aktuellen Inhalte der Datei.</span><span class="sxs-lookup"><span data-stu-id="8cb01-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="8cb01-304">Wenn ein Upload bereits aussteht, wird der vorherige Upload verworfen und der neue Inhalt für den Upload vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="8cb01-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="8cb01-305">Wenn die Datei zur Bearbeitung in einer Anwendung geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei für den Upload vorzubereiten (die Anwendung sollte diesen Schritt bereits ausführen, falls Änderungen vorgenommen werden).</span><span class="sxs-lookup"><span data-stu-id="8cb01-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="8cb01-306">Diese Methode lässt Uploads zu, wenn Sie als zuvor blockierte Uploads markiert wurde (siehe [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)renamedatei).</span><span class="sxs-lookup"><span data-stu-id="8cb01-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-307">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-307">Parameters</span></span>

 <span data-ttu-id="8cb01-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="8cb01-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="8cb01-309">Eine Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="8cb01-310">Bei diesem Wert muss es sich um einen nicht leeren lokalen Pfad mit maximal 256 Zeichen handeln.</span><span class="sxs-lookup"><span data-stu-id="8cb01-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="8cb01-311">Dieser Pfad muss sich in der vom FileSystemDirectoryHint angegebenen Verzeichnisstruktur befinden, wenn der Aufruf von [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="8cb01-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="8cb01-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="8cb01-313">Ein String-Wert, der die Resource-Kennung der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="8cb01-314">Dieser Wert muss mit maximal 128 Zeichen nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="8cb01-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="8cb01-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="8cb01-316">Eine Zeichenfolge, die die Datei auf dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="8cb01-317">Dieser Wert muss nicht leer, gültige URL, aber nicht mehr als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427definiert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-318">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-318">Return values</span></span>

|<span data-ttu-id="8cb01-319">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-319">Value</span></span>|<span data-ttu-id="8cb01-320">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-322">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-324">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="8cb01-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="8cb01-326">Die von _bstrFileSystemPath_ angegebene Datei hat eine andere Resourcen-als die angegebene.</span><span class="sxs-lookup"><span data-stu-id="8cb01-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="8cb01-327">Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="8cb01-328">Weitere Informationen finden Sie unter [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)GetChanges.</span><span class="sxs-lookup"><span data-stu-id="8cb01-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="8cb01-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="8cb01-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="8cb01-330">Die Datei wurde in der Mitte des Vorgangs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8cb01-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="8cb01-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="8cb01-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="8cb01-332">Die angegebene Dateierweiterung wird vom CsiSyncClient-COM-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="8cb01-333">Weitere Informationen finden Sie unter [ILSCLocalSyncClient:: GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="8cb01-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="8cb01-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="8cb01-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="8cb01-335">Das COM-Objekt hat keinen Upload geplant, weil die Datei im Cache die neuesten Änderungen vom Datenträger hatte.</span><span class="sxs-lookup"><span data-stu-id="8cb01-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="8cb01-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="8cb01-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="8cb01-337">Die von _bstrFileSystemPath_ angegebene Datei fehlt oder ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="8cb01-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="8cb01-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="8cb01-339">Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der von der FileSystemDirectoryHint angegeben wurde, wenn der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="8cb01-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-341">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="8cb01-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="8cb01-343">Die von _bstrResourceID_ angegebene Datei hat eine andere FileSystemPath als angegeben.</span><span class="sxs-lookup"><span data-stu-id="8cb01-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="8cb01-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="8cb01-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="8cb01-345">Die angegebene Datei weist bereits ausstehende Änderungen in einem anderen Cache auf und kann dem Consumer-Cache noch nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="8cb01-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="8cb01-347">Der bereitgestellte webPath fällt unter einen anderen Cache.</span><span class="sxs-lookup"><span data-stu-id="8cb01-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-348">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-349">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="8cb01-350">ILSCLocalSyncClient:: renamedatei</span><span class="sxs-lookup"><span data-stu-id="8cb01-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="8cb01-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-351"></span></span>

<span data-ttu-id="8cb01-352">Mit der renamedatei wird eine neue URL und ein lokaler Pfad für eine bestimmte resourcecollection zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="8cb01-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="8cb01-353">Wenn die durch die resourcecollection angegebene Datei nicht bereits im Cache vorhanden ist, wird versucht, Sie zu erstellen und zum herunterladen zu markieren.</span><span class="sxs-lookup"><span data-stu-id="8cb01-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-354">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-354">Parameters</span></span>

 <span data-ttu-id="8cb01-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="8cb01-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="8cb01-356">Ein String-Wert, der die Resource-Kennung der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="8cb01-357">Dieser Wert muss mit maximal 128 Zeichen nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="8cb01-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="8cb01-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="8cb01-359">Eine Zeichenfolge, die den neuen lokalen Pfad für die Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="8cb01-360">Bei diesem Wert muss es sich um einen nicht leeren lokalen Pfad mit maximal 256 Zeichen handeln.</span><span class="sxs-lookup"><span data-stu-id="8cb01-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="8cb01-361">Dieser Pfad muss sich in der vom FileSystemDirectoryHint angegebenen Verzeichnisstruktur befinden, wenn der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="8cb01-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="8cb01-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="8cb01-363">Eine Zeichenfolge, die die neue URL für die Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="8cb01-364">Bei diesem Wert muss es sich um eine nicht leere gültige URL handeln, aber nicht länger als INTERNET_MAX_URL_LENGTH https://support.microsoft.com/kb/208427, wie von definiert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="8cb01-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="8cb01-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="8cb01-366">Gibt an, ob Uploads an den neuen Speicherort derzeit zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="8cb01-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-367">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-367">Return values</span></span>

|<span data-ttu-id="8cb01-368">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-368">Value</span></span>|<span data-ttu-id="8cb01-369">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-371">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-373">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="8cb01-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="8cb01-375">Die _bstrNewFileSystemPath_ oder _bstrNewWebPath_ sind bereits in einer anderen Datei in einem beliebigen Cache vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="8cb01-376">Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="8cb01-377">Weitere Informationen finden Sie unter [ILSCLocalSyncClient:: ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges)GetChanges.</span><span class="sxs-lookup"><span data-stu-id="8cb01-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="8cb01-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="8cb01-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="8cb01-379">Die Dateiinformationen wurden während dieser Methode aus dem Cache gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8cb01-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="8cb01-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="8cb01-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="8cb01-381">Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der von der FileSystemDirectoryHint angegeben wurde, wenn der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="8cb01-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-383">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="8cb01-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="8cb01-385">Die angegebene Datei wird derzeit in einer Office-Anwendung synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="8cb01-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-386">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-387">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="8cb01-388">ILSCLocalSyncClient:: ResetCache</span><span class="sxs-lookup"><span data-stu-id="8cb01-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="8cb01-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-389"></span></span>

<span data-ttu-id="8cb01-390">ResetCache löscht den Cache, der der bei Initialize bereitgestellten Bereitstellung zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="8cb01-391">Hierzu gehören alle Dateiinformationen, die Dateien werden jedoch sowohl auf dem Client als auch auf dem Server belassen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="8cb01-392">Diese Methode verlässt auch das Objekt in einem teilweise nicht initialisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="8cb01-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="8cb01-393">Die einzigen gültigen Aufrufe sind [ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) oder [ILSCLocalSyncClient:: Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="8cb01-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="8cb01-394">Diese Methode kann aufgerufen werden, wenn Initialize fehlschlägt und E_LSC_CACHEMISMATCH zurückgegeben wird, und löscht den Cache, der mit der angegebenen mit dem fehlerhaften Aufruf bereitgestellten-Wert verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="8cb01-395">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-395">Parameters</span></span>

<span data-ttu-id="8cb01-396">Keine</span><span class="sxs-lookup"><span data-stu-id="8cb01-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-397">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-397">Return values</span></span>

|<span data-ttu-id="8cb01-398">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-398">Value</span></span>|<span data-ttu-id="8cb01-399">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-401">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="8cb01-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-403">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-404">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-405">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="8cb01-406">ILSCLocalSyncClient:: ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="8cb01-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="8cb01-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-407"></span></span>

<span data-ttu-id="8cb01-408">ServerFileChange weist das CsiSyncClient-COM-Objekt an, die angegebene Datei zum herunterladen zu markieren.</span><span class="sxs-lookup"><span data-stu-id="8cb01-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="8cb01-409">Wenn die Datei in einer Office-Anwendung zur Bearbeitung geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei zum herunterladen zu markieren (die Anwendung sollte diesen Schritt bereits ausführen, falls Änderungen vorgenommen werden).</span><span class="sxs-lookup"><span data-stu-id="8cb01-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="8cb01-410">Diese Methode ermöglicht Downloads, wenn Sie als Downloads gekennzeichnet wurde, die zuvor blockiert wurden (siehe renamedatei).</span><span class="sxs-lookup"><span data-stu-id="8cb01-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-411">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-411">Parameters</span></span>

|<span data-ttu-id="8cb01-412">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-412">Parameter</span></span>|<span data-ttu-id="8cb01-413">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="8cb01-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="8cb01-415">Eine Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="8cb01-416">Bei diesem Wert muss es sich um einen nicht leeren lokalen Pfad mit maximal 256 Zeichen handeln.</span><span class="sxs-lookup"><span data-stu-id="8cb01-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="8cb01-417">Dieser Pfad muss sich in der vom FileSystemDirectoryHint angegebenen Verzeichnisstruktur befinden, wenn der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="8cb01-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="8cb01-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="8cb01-419">Ein String-Wert, der die Resource-Kennung der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="8cb01-420">Dieser Wert muss mit maximal 128 Zeichen nicht leer sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="8cb01-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="8cb01-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="8cb01-422">Eine Zeichenfolge, die die Datei auf dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="8cb01-423">Bei diesem Wert muss es sich um eine nicht leere gültige URL handeln, aber nicht länger als INTERNET_MAX_URL_LENGTH, https://support.microsoft.com/kb/208427wie von definiert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="8cb01-424">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-424">Return values</span></span>

|<span data-ttu-id="8cb01-425">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-425">Value</span></span>|<span data-ttu-id="8cb01-426">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-428">Der Cache Verbindungsstatus wird nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="8cb01-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="8cb01-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="8cb01-430">Die von _bstrFileSystemPath_ angegebene Datei hat eine andere Resourcen-als die angegebene.</span><span class="sxs-lookup"><span data-stu-id="8cb01-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="8cb01-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="8cb01-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="8cb01-432">Die angegebene Dateierweiterung wird vom CsiSyncClient-COM-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="8cb01-433">Siehe GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="8cb01-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="8cb01-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="8cb01-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="8cb01-435">Die Datei wurde in der Mitte des Vorgangs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8cb01-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="8cb01-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-437">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="8cb01-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="8cb01-439">Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der von der FileSystemDirectoryHint angegeben wurde, wenn der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="8cb01-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-441">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="8cb01-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="8cb01-443">Die von _bstrResourceID_ angegebene Datei hat eine andere FileSystemPath als angegeben.</span><span class="sxs-lookup"><span data-stu-id="8cb01-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="8cb01-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="8cb01-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="8cb01-445">Die angegebene Datei weist bereits ausstehende Änderungen in einem anderen Cache auf und kann dem Consumer-Cache noch nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="8cb01-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="8cb01-447">Der bereitgestellte webPath fällt unter einen anderen Cache.</span><span class="sxs-lookup"><span data-stu-id="8cb01-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-448">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-449">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="8cb01-450">ILSCLocalSyncClient:: SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="8cb01-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="8cb01-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-451"></span></span>

<span data-ttu-id="8cb01-452">Legt den Cache in einen Online-oder Offlinestatus fest.</span><span class="sxs-lookup"><span data-stu-id="8cb01-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="8cb01-453">Im Offlinemodus versucht Office nicht, mit dem Server für Dateien in diesem Cache zu kommunizieren, unabhängig von der _fBlockUploads_ -Einstellung jeder einzelnen Datei.</span><span class="sxs-lookup"><span data-stu-id="8cb01-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-454">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-454">Parameters</span></span>

 <span data-ttu-id="8cb01-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="8cb01-455">_fIsOnline_</span></span>
  
<span data-ttu-id="8cb01-456">Ein boolescher Wert, der den Verbindungsstatus des Caches bestimmt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-457">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-457">Return values</span></span>

|<span data-ttu-id="8cb01-458">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-458">Value</span></span>|<span data-ttu-id="8cb01-459">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-461">Der Cache Verbindungsstatus wird nicht festgelegt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="8cb01-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-463">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-465">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-466">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-467">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="8cb01-468">ILSCLocalSyncClient:: SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="8cb01-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="8cb01-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-469"></span></span>

<span data-ttu-id="8cb01-470">SetClientNetworkSyncPermission wird verwendet, um die heuristischen Heuristiken von restoreOffice für Netzwerkkosten und Stromverbrauch zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="8cb01-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="8cb01-471">Wenn Sie sich in einem 3G-oder einem anderen hochkosten Netzwerk oder bei Batteriebetrieb im Vergleich mit dem Stromnetz anmelden, kann Office den Netzwerkdatenverkehr bis zu einem günstigeren Zeitpunkt blockieren.</span><span class="sxs-lookup"><span data-stu-id="8cb01-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="8cb01-472">Der Consumer dieser API kann damit die Heuristiken von Office außer Kraft setzen und die Synchronisierung erzwingen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-473">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-473">Parameters</span></span>

 <span data-ttu-id="8cb01-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="8cb01-474">_nspType_</span></span>
  
<span data-ttu-id="8cb01-475">Ein Flag, das definiert, welche Kosten heuristisch überschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="8cb01-476">Weitere Informationen finden Sie unter [enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="8cb01-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="8cb01-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="8cb01-477">_fEnableSync_</span></span>
  
<span data-ttu-id="8cb01-478">Gibt an, ob die Synchronisierung mit erzwungen wird, wodurch diese Kosten Heuristik überschrieben wird oder nicht mehr überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-479">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-479">Return values</span></span>

|<span data-ttu-id="8cb01-480">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-480">Value</span></span>|<span data-ttu-id="8cb01-481">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-483">Die Synchronisierungs Heuristik wird nicht außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="8cb01-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-485">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-486">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-487">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="8cb01-488">ILSCLocalSyncClient:: Uninitialize</span><span class="sxs-lookup"><span data-stu-id="8cb01-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="8cb01-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-489"></span></span>

<span data-ttu-id="8cb01-490">Entlädt den Cache aus dem COM-Objekt und führt Schließvorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="8cb01-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="8cb01-491">[ILSCLocalSyncClient:: Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUSS vor dem Zerstören des COM-Objekts aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="8cb01-492">Nachdem Sie aufgerufen wurden, können keine anderen APIs aufgerufen werden, das COM-Objekt muss zerstört und eine neue erstellt werden, wenn Sie den Vorgang fortsetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="8cb01-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="8cb01-493">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-493">Parameters</span></span>

<span data-ttu-id="8cb01-494">Keine.</span><span class="sxs-lookup"><span data-stu-id="8cb01-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-495">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-495">Return values</span></span>

|<span data-ttu-id="8cb01-496">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-496">Value</span></span>|<span data-ttu-id="8cb01-497">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-499">Nicht deinitialisieren.</span><span class="sxs-lookup"><span data-stu-id="8cb01-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="8cb01-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="8cb01-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="8cb01-501">[ILSCLocalSyncClient:: Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="8cb01-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-502">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-503">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="8cb01-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="8cb01-504">Schnittstelle IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="8cb01-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="8cb01-505">Diese Schnittstelle stellt eine Liste von ILSCEvent-Ereignissen dar.</span><span class="sxs-lookup"><span data-stu-id="8cb01-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="8cb01-506">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="8cb01-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="8cb01-507">IEnumLSCEvent:: FNext</span><span class="sxs-lookup"><span data-stu-id="8cb01-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="8cb01-508">Ruft das nächste Ereignis aus der Liste der Ereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="8cb01-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-509">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-509">Parameters</span></span>

 <span data-ttu-id="8cb01-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="8cb01-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="8cb01-511">Ein Zeiger auf eine ILSCEvent-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="8cb01-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-512">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-512">Return values</span></span>

|<span data-ttu-id="8cb01-513">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-513">Value</span></span>|<span data-ttu-id="8cb01-514">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-516">Es sind keine weiteren Ereignisse mehr vorhanden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="8cb01-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-517">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-518">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="8cb01-519">IEnumLSCEvent:: Reset</span><span class="sxs-lookup"><span data-stu-id="8cb01-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="8cb01-520">Setzt den Enumerator auf das erste Ereignis zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="8cb01-521">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-521">Parameters</span></span>

<span data-ttu-id="8cb01-522">Keine.</span><span class="sxs-lookup"><span data-stu-id="8cb01-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-523">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-523">Return values</span></span>

<span data-ttu-id="8cb01-524">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="8cb01-525">Schnittstelle ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="8cb01-525">Interface ILSCEvent</span></span>

<span data-ttu-id="8cb01-526">Diese Schnittstelle stellt ein Synchronisierungsereignis dar.</span><span class="sxs-lookup"><span data-stu-id="8cb01-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="8cb01-527">Alle Informationen über das Ereignis können von der Benutzeroberfläche abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="8cb01-528">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="8cb01-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="8cb01-529">ILSCEvent:: GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="8cb01-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="8cb01-530">Beachten Sie, dass dieser Wert aufgefüllt wird, wenn [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) GetChanges aufgerufen wird, nicht beim Erstellen des Ereignisses, sodass Sie nur den aktuellen Status der Datei und nicht den Status der Datei haben, wenn der Konfliktstatus geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="8cb01-531">Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnLocalConflictStateChanged ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-532">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-532">Parameters</span></span>

 <span data-ttu-id="8cb01-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="8cb01-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="8cb01-534">Der aktuelle Konfliktstatus der Datei, die dem Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-535">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-535">Return values</span></span>

<span data-ttu-id="8cb01-536">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="8cb01-537">ILSCEvent:: getError</span><span class="sxs-lookup"><span data-stu-id="8cb01-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="8cb01-538">Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-539">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-539">Parameters</span></span>

 <span data-ttu-id="8cb01-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="8cb01-540">_pnError_</span></span>
  
<span data-ttu-id="8cb01-541">Der mit diesem Ereignis verknüpfte Fehler.</span><span class="sxs-lookup"><span data-stu-id="8cb01-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-542">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-542">Return values</span></span>

<span data-ttu-id="8cb01-543">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="8cb01-544">ILSCEvent:: getETag</span><span class="sxs-lookup"><span data-stu-id="8cb01-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="8cb01-545">Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-546">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-546">Parameters</span></span>

 <span data-ttu-id="8cb01-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="8cb01-547">_pbstrETag_</span></span>
  
<span data-ttu-id="8cb01-548">Das mit diesem Ereignis verknüpfte ETag</span><span class="sxs-lookup"><span data-stu-id="8cb01-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-549">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-549">Return values</span></span>

<span data-ttu-id="8cb01-550">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="8cb01-551">ILSCEvent:: getEventtype</span><span class="sxs-lookup"><span data-stu-id="8cb01-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="8cb01-552">Ruft den Typ für dieses Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="8cb01-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-553">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-553">Parameters</span></span>

 <span data-ttu-id="8cb01-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="8cb01-554">_pnEventType_</span></span>
  
<span data-ttu-id="8cb01-555">Der Ereignistyp dieses Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="8cb01-555">The event type of this event.</span></span> <span data-ttu-id="8cb01-556">Weitere Informationen finden Sie unter [enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for Valid values.</span><span class="sxs-lookup"><span data-stu-id="8cb01-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="8cb01-557">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-558">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-558">Return values</span></span>

|<span data-ttu-id="8cb01-559">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-559">Value</span></span>|<span data-ttu-id="8cb01-560">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-562">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-563">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-564">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="8cb01-565">ILSCEvent:: GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="8cb01-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="8cb01-566">Ruft den lokalen Arbeitspfad für dieses Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="8cb01-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-567">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-567">Parameters</span></span>

 <span data-ttu-id="8cb01-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="8cb01-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="8cb01-569">Der lokale Pfad der Datei, auf die sich dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="8cb01-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-570">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-570">Return values</span></span>

<span data-ttu-id="8cb01-571">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="8cb01-572">ILSCEvent:: GetResource-Nr.</span><span class="sxs-lookup"><span data-stu-id="8cb01-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="8cb01-573">Ruft die Ressourcen-ID für das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="8cb01-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-574">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-574">Parameters</span></span>

 <span data-ttu-id="8cb01-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="8cb01-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="8cb01-576">Die resourcecollection der Datei, die diesem Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-577">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-577">Return values</span></span>

<span data-ttu-id="8cb01-578">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="8cb01-579">ILSCEvent:: GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="8cb01-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="8cb01-580">Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="8cb01-581">Wenn ein Aufruf von [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) renamedatei einen Webpfad oder einen lokalen Pfad Konflikt mit einer anderen Datei im Office-Dateicache verursacht, Ereignis generiert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-582">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-582">Parameters</span></span>

 <span data-ttu-id="8cb01-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="8cb01-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="8cb01-584">Die resourcecollection, die das Generieren dieses Ereignisses verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="8cb01-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="8cb01-585">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-586">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-586">Return values</span></span>

<span data-ttu-id="8cb01-587">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="8cb01-588">ILSCEvent:: GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="8cb01-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="8cb01-589">Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-590">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-590">Parameters</span></span>

 <span data-ttu-id="8cb01-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="8cb01-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="8cb01-592">Der diesem Ereignis zugeordnete Fehlertyp.</span><span class="sxs-lookup"><span data-stu-id="8cb01-592">The error type associated with this event.</span></span> <span data-ttu-id="8cb01-593">Weitere Informationen finden Sie unter [enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for Potential values.</span><span class="sxs-lookup"><span data-stu-id="8cb01-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="8cb01-594">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-595">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-595">Return values</span></span>

|<span data-ttu-id="8cb01-596">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-596">Value</span></span>|<span data-ttu-id="8cb01-597">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-599">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-600">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-601">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="8cb01-602">ILSCEvent:: GetWebPath</span><span class="sxs-lookup"><span data-stu-id="8cb01-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="8cb01-603">Dieser Wert wird nur aufgefüllt, wenn die [Enumeration LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-604">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-604">Parameters</span></span>

 <span data-ttu-id="8cb01-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="8cb01-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="8cb01-606">Gibt den webPfad an, der diesem Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="8cb01-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="8cb01-607">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-608">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-608">Return values</span></span>

<span data-ttu-id="8cb01-609">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="8cb01-610">Schnittstelle ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="8cb01-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="8cb01-611">Diese Schnittstelle enthält zusätzliche Informationen zu einem Synchronisierungsereignis.</span><span class="sxs-lookup"><span data-stu-id="8cb01-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="8cb01-612">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="8cb01-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="8cb01-613">ILSCEvent2:: GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="8cb01-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="8cb01-614">Ruft die Fehler Kette Informationen zu einem Synchronisierungsereignis ab.</span><span class="sxs-lookup"><span data-stu-id="8cb01-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-615">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-615">Parameters</span></span>

 <span data-ttu-id="8cb01-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="8cb01-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="8cb01-617">Eine Zeichenfolge, die die Fehler Ketten Informationen enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="8cb01-617">A string to hold the error chain information.</span></span> <span data-ttu-id="8cb01-618">Darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="8cb01-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-619">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-619">Return values</span></span>

|<span data-ttu-id="8cb01-620">Wert</span><span class="sxs-lookup"><span data-stu-id="8cb01-620">Value</span></span>|<span data-ttu-id="8cb01-621">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="8cb01-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="8cb01-623">Diese Schnittstelle wird von der installierten Office-Version nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="8cb01-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="8cb01-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="8cb01-625">Mindestens einer der Parameterwerte ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="8cb01-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="8cb01-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="8cb01-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="8cb01-627">Die Fehler Ketten Informationen sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8cb01-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="8cb01-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="8cb01-628">S_OK</span></span>  <br/> |<span data-ttu-id="8cb01-629">Der Anruf wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="8cb01-630">Schnittstelle IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="8cb01-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="8cb01-631">Diese Schnittstelle stellt eine Rückruffunktion für das CSISyncClient-COM-Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="8cb01-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="8cb01-632">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="8cb01-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="8cb01-633">IPartnerActivityCallback:: EventOccurred</span><span class="sxs-lookup"><span data-stu-id="8cb01-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="8cb01-634">Hierbei handelt es sich um eine Rückruffunktion für das Objekt, das für das CsiSyncClient-COM-Objekt angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="8cb01-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="8cb01-635">Es wird erwartet, dass beim Eintreten eines Ereignisses (siehe [enum-LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) für gültige Ereignistypen) das CSISYNCCLIENT-com-Objekt diese Methode aufruft, um den Consumer zu signalisieren.</span><span class="sxs-lookup"><span data-stu-id="8cb01-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="8cb01-636">Parameter</span><span class="sxs-lookup"><span data-stu-id="8cb01-636">Parameters</span></span>

 <span data-ttu-id="8cb01-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="8cb01-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="8cb01-638">Der Ereignistyp dieses Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="8cb01-638">The event type of this event.</span></span> <span data-ttu-id="8cb01-639">Weitere Informationen finden Sie unter [enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for Valid values.</span><span class="sxs-lookup"><span data-stu-id="8cb01-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="8cb01-640">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="8cb01-640">Return values</span></span>

<span data-ttu-id="8cb01-641">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="8cb01-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="8cb01-642">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="8cb01-642">Enumerations</span></span>

<span data-ttu-id="8cb01-643">CSISyncClient verwendet die folgenden Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="8cb01-644">Enum-LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="8cb01-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="8cb01-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-645"></span></span>

<span data-ttu-id="8cb01-646">Diese Enumeration gibt die Fehlerkategorien an, die beim Synchronisieren einer Datei auftreten können.</span><span class="sxs-lookup"><span data-stu-id="8cb01-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="8cb01-647">Enumerator</span><span class="sxs-lookup"><span data-stu-id="8cb01-647">Enumerator</span></span>|<span data-ttu-id="8cb01-648">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="8cb01-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="8cb01-650">Der Synchronisierungsfehler dieses Ereignisses war unerwartet und erfordert möglicherweise besondere Überlegungen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="8cb01-651">In der Standardeinstellung muss der Benutzer möglicherweise eingreifen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="8cb01-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="8cb01-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="8cb01-653">Der Synchronisierungsfehler dieses Ereignisses erfordert keine besondere Überlegung.</span><span class="sxs-lookup"><span data-stu-id="8cb01-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="8cb01-654">Office behandelt es automatisch.</span><span class="sxs-lookup"><span data-stu-id="8cb01-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="8cb01-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="8cb01-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="8cb01-656">Der Synchronisierungsfehler dieses Ereignisses erfordert, dass ein Benutzer diesen auflöst.</span><span class="sxs-lookup"><span data-stu-id="8cb01-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="8cb01-657">Beispielsweise muss ein Benutzer beim Zusammenführen von Konflikten das Dokument öffnen und zusammenführen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="8cb01-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="8cb01-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="8cb01-659">Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Consumer eingreift, aber keine besondere Überlegung durch den Benutzer erfordert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="8cb01-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="8cb01-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="8cb01-661">Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Consumer als Sonderfall interveniert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="8cb01-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="8cb01-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="8cb01-663">Enum-LSCEventType</span><span class="sxs-lookup"><span data-stu-id="8cb01-663">Enum LSCEventType</span></span>
<span data-ttu-id="8cb01-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-664"></span></span>

<span data-ttu-id="8cb01-665">Diese Enumeration gibt den Typ der Ereignisse an, die für eine bestimmte Datei auftreten können.</span><span class="sxs-lookup"><span data-stu-id="8cb01-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="8cb01-666">Enumerator</span><span class="sxs-lookup"><span data-stu-id="8cb01-666">Enumerator</span></span>|<span data-ttu-id="8cb01-667">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="8cb01-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="8cb01-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="8cb01-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="8cb01-670">Änderungen wurden an einer lokalen Datei vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="8cb01-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="8cb01-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="8cb01-672">Ein Benutzer hat eine Datei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="8cb01-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="8cb01-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="8cb01-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="8cb01-674">Dateiänderungen wurden vom Server heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="8cb01-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="8cb01-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="8cb01-676">Hochladen von Dateiänderungen auf den Server abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="8cb01-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="8cb01-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="8cb01-678">Der Merge-Konfliktstatus einer Datei wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="8cb01-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="8cb01-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="8cb01-680">Eine Datei wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="8cb01-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="8cb01-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="8cb01-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="8cb01-682">Eine Datei wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="8cb01-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="8cb01-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="8cb01-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="8cb01-684">Die Synchronisierung wurde für die Dateien eines Benutzers aktiviert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="8cb01-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="8cb01-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="8cb01-686">Dateiänderungen wurden vom Server heruntergeladen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="8cb01-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="8cb01-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="8cb01-688">Mit dem Hochladen von Dateiänderungen auf den Server begonnen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="8cb01-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="8cb01-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="8cb01-690">Dieses Ereignis wird generiert, wenn ein Aufruf von [ILSCLocalSyncClient:: LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient:: ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) renameDatei bewirkt, dass ein Webpfad oder ein lokaler Pfad Konflikt mit einer anderen Datei in der Office-Dateicache.</span><span class="sxs-lookup"><span data-stu-id="8cb01-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="8cb01-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="8cb01-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="8cb01-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="8cb01-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="8cb01-693">Enum-LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="8cb01-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="8cb01-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-694"></span></span>

<span data-ttu-id="8cb01-695">Diese Enumeration gibt den Typ der Ereignisse an, die auftreten können.</span><span class="sxs-lookup"><span data-stu-id="8cb01-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="8cb01-696">Der Consumer muss bestimmte ILSCLocalSyncClient-Funktionen basierend auf dem Ereignistyp aufrufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="8cb01-697">Enumerator</span><span class="sxs-lookup"><span data-stu-id="8cb01-697">Enumerator</span></span>|<span data-ttu-id="8cb01-698">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="8cb01-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="8cb01-700">Ein ILSCEvent ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="8cb01-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="8cb01-701">Der Consumer sollte [ILSCLocalSyncClient::](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) GetChanges aufrufen, um die Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="8cb01-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="8cb01-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="8cb01-703">Die unterstützten Dateierweiterungen wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="8cb01-703">The supported file extensions have changed.</span></span> <span data-ttu-id="8cb01-704">Der Consumer sollte [ILSCLocalSyncClient:: GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) aufrufen, um die neue Liste unterstützter Erweiterungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="8cb01-705">Enum-LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="8cb01-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="8cb01-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-706"></span></span>

<span data-ttu-id="8cb01-707">Diese Enumeration gibt die Flags an, die für eine heuristische Netzwerkkosten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="8cb01-708">Enumerator</span><span class="sxs-lookup"><span data-stu-id="8cb01-708">Enumerator</span></span>|<span data-ttu-id="8cb01-709">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="8cb01-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="8cb01-711">True, wenn die Kosten Heuristik für teure Netzwerke (wie 3G) überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="8cb01-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="8cb01-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="8cb01-713">True, wenn die Kosten Heuristik für Energieverbrauch (wie eine Batterie) überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="8cb01-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="8cb01-714">Enum-LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="8cb01-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="8cb01-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="8cb01-715"></span></span>

<span data-ttu-id="8cb01-716">Diese Enumeration wird verwendet, um den Synchronisierungsstatus einer Datei darzustellen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="8cb01-717">Enumerator</span><span class="sxs-lookup"><span data-stu-id="8cb01-717">Enumerator</span></span>|<span data-ttu-id="8cb01-718">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="8cb01-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="8cb01-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="8cb01-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="8cb01-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="8cb01-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="8cb01-721">True, wenn ausstehende Daten an die Server Datei gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="8cb01-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="8cb01-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="8cb01-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="8cb01-723">True, wenn die Daten aus der Server Datei heruntergeladen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="8cb01-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="8cb01-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="8cb01-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="8cb01-725">True, wenn sich das Daten Büro in der Datei in seinem Cache befindet, ist die neueste Kopie der Daten auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="8cb01-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

