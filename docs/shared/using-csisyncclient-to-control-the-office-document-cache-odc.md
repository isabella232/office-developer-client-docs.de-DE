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
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="f3753-103">Verwenden von CSISyncClient zum Steuern Office Dokumentcache (ODC)</span><span class="sxs-lookup"><span data-stu-id="f3753-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="f3753-104">Erfahren Sie, wie Sie CSISyncClient zum Steuern des Office Document Cache (ODC) verwenden.</span><span class="sxs-lookup"><span data-stu-id="f3753-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="f3753-105">CSISyncClient ist ein out-of-proc-COM-Server (CsiSyncClient.exe), der Microsoft OneDrive das Verhalten des Office Document Cache (ODC) steuern kann.</span><span class="sxs-lookup"><span data-stu-id="f3753-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="f3753-106">Beispielsweise kann OneDrive odC über CSISyncClient aufrufen, um Dateien auf und von MS-FSSHTTP-aktivierten Endpunkten hochzuladen und herunterzuladen.</span><span class="sxs-lookup"><span data-stu-id="f3753-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="f3753-107">Dies ermöglicht erweiterte servicegesicherte Features in Office, z. B. die gemeinsamen Erstellung und nahtlose Übergänge von offline zu online.</span><span class="sxs-lookup"><span data-stu-id="f3753-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="f3753-108">CsiSyncClient ist in Office Desktop verfügbar (sowohl x86 als auch x64).</span><span class="sxs-lookup"><span data-stu-id="f3753-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="f3753-109">Hinweis: Neuere Versionen von Office möglicherweise mit CsiSyncClient, der Prozess wird jedoch nur zur Abwärtskompatibilität verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3753-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="f3753-110">Die CsiSyncClient-Schnittstelle und die Methode zum Steuern des ODC werden sich in zukünftigen Versionen von Office.</span><span class="sxs-lookup"><span data-stu-id="f3753-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="f3753-111">Die Klassen-ID ist derzeit so festgelegt, dass sie nur auf OneDrive.</span><span class="sxs-lookup"><span data-stu-id="f3753-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="f3753-112">Das COM-Objekt kann als out-of-proc-COM-Server verwendet werden und wird in CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="f3753-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="f3753-113">Aufgrund von Einschränkungen bei Access (die vom ODC verwendet werden) wird der Bittyp Office verwendet, sodass x64 Office ein x64 COM-Objekt oder x86 Office ein x86 COM-Objekt bedeutet.</span><span class="sxs-lookup"><span data-stu-id="f3753-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="f3753-114">Um diese Einschränkung zu umgehen, wird das COM-Objekt CLSCTX_LOCAL_SERVER durch Angabe von CLSCTX_LOCAL_SERVER als Teil der CoCreateInstance als out-of-proc-COM-Server gehostet, was bitübergreifende Kompatibilität ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="f3753-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="f3753-115">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="f3753-115">Interfaces</span></span>

<span data-ttu-id="f3753-116">CSISyncClient verwendet die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="f3753-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="f3753-117">Schnittstelle ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="f3753-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="f3753-118">Dies ist die primäre Schnittstelle zum Synchronisieren von Dateien in Office.</span><span class="sxs-lookup"><span data-stu-id="f3753-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="f3753-119">ProgID: Office. LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="f3753-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="f3753-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="f3753-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="f3753-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="f3753-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="f3753-122">Das verfügbar gemachte COM-Objekt wird als Out-of-Proc-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="f3753-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="f3753-123">Das Angeben CLSCTX_LOCAL_SERVER als Teil von CoCreateInstance ermöglicht die Kompatibilität zwischen 64-Bit- und 32-Bit-Prozessen.</span><span class="sxs-lookup"><span data-stu-id="f3753-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="f3753-124">Nachdem Sie das COM-Objekt gemeinsam erstellt haben, müssen Sie [zuerst ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="f3753-125">Sobald [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgreich abgeschlossen wurde, können Sie jede API so oft wie gewünscht und in beliebiger Reihenfolge aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="f3753-126">Sie können auch [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) für ein bereits initialisiertes Objekt aufrufen, dies führt jedoch nicht dazu.</span><span class="sxs-lookup"><span data-stu-id="f3753-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="f3753-127">Die Ausnahmen zum vorherigen Absatz sind [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) und [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="f3753-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="f3753-128">Nachdem Sie [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) für das COM-Objekt aufgerufen haben, müssen Sie dieses Objekt zerstören und ein neues erstellen.</span><span class="sxs-lookup"><span data-stu-id="f3753-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="f3753-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) löscht Ihren Untercache, löscht alle zugeordneten Dateiinformationen im Cache, belasse die Dokumente jedoch auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="f3753-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="f3753-130">Außerdem bleibt der Zustand für die Kommunikation mit dem Cache erhalten.</span><span class="sxs-lookup"><span data-stu-id="f3753-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="f3753-131">Auf diese Weise können Sie [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erneut aufrufen, um einen neuen Cache zu erstellen, ohne das COM-Objekt zerstören und neu erstellen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f3753-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="f3753-132">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f3753-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="f3753-133">ILSCLocalSyncClient::D eleteFile</span><span class="sxs-lookup"><span data-stu-id="f3753-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="f3753-134">DeleteFile wird verwendet, um die Dateiinformationen aus dem Cache zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="f3753-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="f3753-135">Bei dieser Methode bleibt die zugeordnete Datei jedoch auf dem Datenträger und auf dem Server.</span><span class="sxs-lookup"><span data-stu-id="f3753-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="f3753-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-136">Parameters</span></span>

 <span data-ttu-id="f3753-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="f3753-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="f3753-138">Die Zeichenfolge, die die ResourceID der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="f3753-139">Dieser Wert darf maximal 128 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-140">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-140">Return values</span></span>

|<span data-ttu-id="f3753-141">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-141">Value</span></span>|<span data-ttu-id="f3753-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-144">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-146">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-148">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="f3753-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="f3753-150">Die angegebene ResourceID befindet sich nicht im Cache.</span><span class="sxs-lookup"><span data-stu-id="f3753-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-152">Initialize wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="f3753-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="f3753-154">Die Datei wird derzeit synchronisiert oder geöffnet und kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="f3753-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-155">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-156">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="f3753-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="f3753-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="f3753-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span></span>

<span data-ttu-id="f3753-159">GetChanges gibt einen Enumerator von ILSCEvent-Objekten zurück und gibt auch ein Token zurück, das für den nächsten Aufruf von GetChanges angegeben wird, vorausgesetzt, der Consumer hat den vorherigen Satz von Ereignissen verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="f3753-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="f3753-160">Ereignisse vor  _dem angegebenen nPreviousChangesToken_ werden gelöscht und sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3753-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="f3753-161">Wenn keine Ereignisse verarbeitet werden sollen, sollte  _pnCurrentChangesToken_ denselben Wert wie  _nPreviousChangesToken_ haben,  _aber ppiEvents_ wird weiterhin festgelegt.</span><span class="sxs-lookup"><span data-stu-id="f3753-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="f3753-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-162">Parameters</span></span>

 <span data-ttu-id="f3753-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="f3753-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="f3753-164">Gibt an, welches Ereignis zuletzt vom Consumer verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="f3753-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="f3753-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="f3753-166">Gibt das neueste Ereignis an, das an den Verbraucher übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="f3753-167">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-167">Must not be null.</span></span>
  
 <span data-ttu-id="f3753-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="f3753-168">_ppiEvents_</span></span>
  
<span data-ttu-id="f3753-169">Ein Aufzählerator für die Ereignisse, die dem Verbraucher übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="f3753-170">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-171">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-171">Return values</span></span>

|<span data-ttu-id="f3753-172">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-172">Value</span></span>|<span data-ttu-id="f3753-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-175">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-177">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-180">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-181">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="f3753-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="f3753-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="f3753-183">GetClientNetworkSyncPermission wird verwendet, um zu abfragen, ob Office Synchronisierungs heuristics für Netzwerkkosten und Energieverbrauch außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="f3753-184">Wenn sie sich 3G oder einem anderen netzwerk mit hohen Kosten befinden oder wenn sie mit Akku betrieben werden oder angeschlossen werden, Office möglicherweise den Netzwerkdatenverkehr bis zu einem bestimmten Zeitpunkt blockieren.</span><span class="sxs-lookup"><span data-stu-id="f3753-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="f3753-185">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-185">Parameters</span></span>

 <span data-ttu-id="f3753-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="f3753-186">_nspType_</span></span>
  
<span data-ttu-id="f3753-187">Ein Flag, das definiert, welche Kosten heuristisch abgefragt werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="f3753-188">Weitere [Informationen finden Sie unter Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="f3753-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="f3753-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="f3753-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="f3753-190">Gibt an, ob die angeforderte Kostenhuristik derzeit außer Kraft gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="f3753-191">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-192">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-192">Return values</span></span>

|<span data-ttu-id="f3753-193">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-193">Value</span></span>|<span data-ttu-id="f3753-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-196">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-198">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-201">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-202">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="f3753-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="f3753-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="f3753-204">GetFileStatus wird verwendet, um Informationen für eine bestimmte Datei zu sammeln: ob sie im Cache vorhanden ist, ob die Kommunikation mit der Serverkopie aussteht und Office 2013 die neuesten Daten aus der lokalen Kopie enthält.</span><span class="sxs-lookup"><span data-stu-id="f3753-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="f3753-205">Es erfordert ein bitweises Flag von [Enum LSCStatusFlag-Werten,](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) um zu bestimmen, welche Informationen das CsiSyncClient COM-Objekt abfragen soll.</span><span class="sxs-lookup"><span data-stu-id="f3753-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="f3753-206">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-206">Parameters</span></span>

 <span data-ttu-id="f3753-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="f3753-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="f3753-208">Die Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="f3753-209">Dieser Wert darf nicht leer sein und darf maximal 128 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="f3753-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="f3753-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="f3753-211">Ein Flag, das definiert, welche Informationen zurückgeben werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-211">A flag which defines what information to return.</span></span> <span data-ttu-id="f3753-212">Siehe [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="f3753-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="f3753-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="f3753-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="f3753-214">Die Zeichenfolge, die den Speicherort der Datei identifiziert, die von  _bstrResourceID auf_ dem Client identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="f3753-215">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-215">Must not be null.</span></span> 
  
 <span data-ttu-id="f3753-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="f3753-216">_pbstrETag_</span></span>
  
<span data-ttu-id="f3753-217">Eine Zeichenfolge, die das eTag für die durch _bstrResourceID identifizierte Datei enthält._</span><span class="sxs-lookup"><span data-stu-id="f3753-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="f3753-218">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-218">Must not be null.</span></span> 
  
 <span data-ttu-id="f3753-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="f3753-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="f3753-220">Ein Flag, das den über _sfRequestedStatus_ angeforderten Status für die durch _bstrResourceID identifizierte Datei enthält._</span><span class="sxs-lookup"><span data-stu-id="f3753-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="f3753-221">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-221">Must not be null.</span></span> <span data-ttu-id="f3753-222">Siehe [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="f3753-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-223">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-223">Return values</span></span>

|<span data-ttu-id="f3753-224">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-224">Value</span></span>|<span data-ttu-id="f3753-225">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-227">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-229">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="f3753-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="f3753-231">Die von  _bstrResourceID_ angegebenen Dateiinformationen sind im Cache nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f3753-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f3753-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="f3753-233">LSCStatusFlag_LocalFileUnchanged angefordert wurde oder die durch  _bstrResourceID_ angegebene Datei gesperrt oder fehlt.</span><span class="sxs-lookup"><span data-stu-id="f3753-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="f3753-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-236">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-237">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="f3753-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="f3753-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="f3753-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span></span>

<span data-ttu-id="f3753-240">GetSupportedFileExtensions gibt eine Liste der durch Pipe getrennten Dateierweiterungen zurück, die derzeit vom CsiSyncClient COM-Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="f3753-241">Beachten Sie, dass sich diese Liste ändern kann, und der Verbraucher wird über das IPartnerActivityCallback-Objekt benachrichtigt, das auf [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) bereitgestellt wird (siehe EventOccured).</span><span class="sxs-lookup"><span data-stu-id="f3753-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="f3753-242">Ein Beispiel für die zurückgegebene Zeichenfolge lautet: "|docx|docm|pptx|"</span><span class="sxs-lookup"><span data-stu-id="f3753-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="f3753-243">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-243">Parameters</span></span>

 <span data-ttu-id="f3753-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="f3753-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="f3753-245">Eine Zeichenfolge, die mit einem durch Pipe getrennten Satz von Dateierweiterungen festgelegt werden soll, die vom CsiSyncClient COM-Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="f3753-246">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-247">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-247">Return values</span></span>

|<span data-ttu-id="f3753-248">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-248">Value</span></span>|<span data-ttu-id="f3753-249">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-251">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-253">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-256">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-257">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="f3753-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="f3753-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="f3753-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span></span>

<span data-ttu-id="f3753-260">Initialize muss die erste aufgerufene Methode sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-260">Initialize must be the first method called.</span></span> <span data-ttu-id="f3753-261">Andernfalls werden alle anderen APIs E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="f3753-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="f3753-262">Das Aufrufen von Initialize für ein bereits initialisiertes Objekt gibt S_OK zurück und führt nichts aus.</span><span class="sxs-lookup"><span data-stu-id="f3753-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="f3753-263">Wenn E_LSC_CACHEMISMATCH zurückgegeben wird, kann der Aufrufer [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) aufrufen, um den Cache zu löschen, der der angegebenen SuppliedID zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f3753-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="f3753-264">In diesem Fall werden jedoch weiterhin andere APIs E_LSC_NOTINITIALIZED.</span><span class="sxs-lookup"><span data-stu-id="f3753-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="f3753-265">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-265">Parameters</span></span>

 <span data-ttu-id="f3753-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="f3753-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="f3753-267">Identifiziert den Consumer und den zu verwendende Cache.</span><span class="sxs-lookup"><span data-stu-id="f3753-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="f3753-268">Darf maximal 32 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="f3753-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="f3753-269">_bstrProgID_</span></span>
  
<span data-ttu-id="f3753-270">Identifiziert das COM-Objekt des Verbrauchers für die zweiwege Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="f3753-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="f3753-271">Darf maximal 39 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="f3753-272">Weitere Informationen zu ProgIDs finden Sie unter [ \< ProgID \> Key.](https://docs.microsoft.com/windows/desktop/com/-progid--key)</span><span class="sxs-lookup"><span data-stu-id="f3753-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="f3753-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="f3753-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="f3753-274">Gibt den Verzeichnisstamm an, in dem lokale Dateien gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="f3753-275">Darf maximal 256 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="f3753-276">Das Verzeichnis muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="f3753-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="f3753-277">_pEventCallback_</span></span>
  
<span data-ttu-id="f3753-278">Die Rückrufschnittstelle, die CsiSyncClient bei Änderungen benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="f3753-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="f3753-279">Weitere Informationen finden Sie unter IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="f3753-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="f3753-280">Dieser Wert darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="f3753-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="f3753-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="f3753-282">Gibt zurück, ob ein neuer Cache erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="f3753-283">Wenn der SuppliedID kein Cache zugeordnet ist, wird ein Cache erstellt.</span><span class="sxs-lookup"><span data-stu-id="f3753-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="f3753-284">Dieser Wert darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-285">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-285">Return values</span></span>

|<span data-ttu-id="f3753-286">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-286">Value</span></span>|<span data-ttu-id="f3753-287">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-289">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-291">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="f3753-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="f3753-293">Einer SuppliedID ist bereits ein Cache zugeordnet, aber eine andere ProgId oder FileSystemDirectoryHint als die bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="f3753-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="f3753-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="f3753-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="f3753-295">Das FileSystemDirectoryHint (oder ein Unterordner) ist bereits in einem anderen Cache vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f3753-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="f3753-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="f3753-297">Die ProgID ist bereits in einem anderen Cache vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f3753-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-298">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-299">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="f3753-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="f3753-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="f3753-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span></span>

<span data-ttu-id="f3753-302">LocalFileChange wird verwendet, um das CsiSyncClient COM-Objekt anzuraten, die angegebene Datei hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="f3753-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="f3753-303">Die Methode bereitet die Datei für den Upload vor, einschließlich des Lesens des aktuellen Inhalts der Datei.</span><span class="sxs-lookup"><span data-stu-id="f3753-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="f3753-304">Wenn ein Upload bereits aussteht, wird der vorherige Upload verworfen und die neuen Inhalte für den Upload vorbereitet.</span><span class="sxs-lookup"><span data-stu-id="f3753-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="f3753-305">Wenn die Datei für die Bearbeitung in einer Anwendung geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei für den Upload vorbereiten zu müssen (die Anwendung sollte diesen Schritt bereits tun, wenn Änderungen vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="f3753-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="f3753-306">Diese Methode ermöglicht Uploads, wenn sie zuvor als blockierte Uploads markiert wurde (siehe [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="f3753-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="f3753-307">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-307">Parameters</span></span>

 <span data-ttu-id="f3753-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="f3753-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="f3753-309">Eine Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="f3753-310">Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="f3753-311">Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die vom FileSystemDirectoryHint angegeben wird, wenn der Aufruf von [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="f3753-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="f3753-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="f3753-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="f3753-313">Eine Zeichenfolge, die die ResourceID der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="f3753-314">Dieser Wert darf maximal 128 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="f3753-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="f3753-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="f3753-316">Eine Zeichenfolge, die die Datei auf dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="f3753-317">Dieser Wert muss nicht leer sein, gültige URL, aber nicht länger als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427 definiert.</span><span class="sxs-lookup"><span data-stu-id="f3753-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-318">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-318">Return values</span></span>

|<span data-ttu-id="f3753-319">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-319">Value</span></span>|<span data-ttu-id="f3753-320">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-322">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-324">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="f3753-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="f3753-326">Die von  _bstrFileSystemPath_ angegebene Datei hat eine andere ResourceID als angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3753-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="f3753-327">Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="f3753-328">Siehe [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="f3753-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="f3753-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="f3753-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="f3753-330">Die Datei wurde in der Mitte des Vorgangs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f3753-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="f3753-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="f3753-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="f3753-332">Die angegebene Dateierweiterung wird vom CsiSyncClient COM-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3753-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="f3753-333">Weitere Informationen finden Sie unter [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="f3753-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="f3753-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="f3753-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="f3753-335">Das COM-Objekt hat keinen Upload geplant, da die Datei im Cache die neuesten Änderungen auf dem Datenträger hatte.</span><span class="sxs-lookup"><span data-stu-id="f3753-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="f3753-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="f3753-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="f3753-337">Die von  _bstrFileSystemPath_ angegebene Datei fehlt oder ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="f3753-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="f3753-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="f3753-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="f3753-339">Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="f3753-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="f3753-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="f3753-343">Die durch  _bstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3753-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="f3753-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="f3753-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="f3753-345">Die angegebene Datei hat bereits ausstehende Änderungen in einem anderen Cache und kann dem Cache des Verbrauchers noch nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="f3753-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="f3753-347">Der bereitgestellte WebPath fällt unter einen anderen Cache.</span><span class="sxs-lookup"><span data-stu-id="f3753-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-348">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-349">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="f3753-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="f3753-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="f3753-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span></span>

<span data-ttu-id="f3753-352">RenameFile zuordnen eine neue URL und einen lokalen Pfad für eine bestimmte ResourceID.</span><span class="sxs-lookup"><span data-stu-id="f3753-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="f3753-353">Wenn die durch die ResourceID angegebene Datei noch nicht im Cache vorhanden ist, wird versucht, sie zu erstellen und zum Download zu markieren.</span><span class="sxs-lookup"><span data-stu-id="f3753-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="f3753-354">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-354">Parameters</span></span>

 <span data-ttu-id="f3753-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="f3753-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="f3753-356">Eine Zeichenfolge, die die ResourceID der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="f3753-357">Dieser Wert darf maximal 128 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="f3753-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="f3753-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="f3753-359">Eine Zeichenfolge, die den neuen lokalen Pfad für die Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="f3753-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="f3753-360">Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="f3753-361">Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="f3753-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="f3753-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="f3753-363">Eine Zeichenfolge, die die neue URL für die Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="f3753-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="f3753-364">Bei diesem Wert muss es sich um eine nicht leere gültige URL, jedoch nicht mehr als INTERNET_MAX_URL_LENGTH, wie von https://support.microsoft.com/kb/208427 definiert.</span><span class="sxs-lookup"><span data-stu-id="f3753-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="f3753-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="f3753-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="f3753-366">Gibt an, ob Uploads an den neuen Speicherort derzeit zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="f3753-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-367">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-367">Return values</span></span>

|<span data-ttu-id="f3753-368">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-368">Value</span></span>|<span data-ttu-id="f3753-369">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-371">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-373">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="f3753-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="f3753-375">Der  _bstrNewFileSystemPath_ oder  _bstrNewWebPath_ ist bereits in einer anderen Datei in einem beliebigen Cache vorhanden.</span><span class="sxs-lookup"><span data-stu-id="f3753-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="f3753-376">Ein Ereignis vom Typ LSCEventType_OnFilePathConflict wird gesendet, wenn dieser Fehler zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="f3753-377">Siehe [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="f3753-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="f3753-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="f3753-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="f3753-379">Die Dateiinformationen wurden während der Ausführung dieser Methode aus dem Cache gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f3753-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="f3753-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="f3753-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="f3753-381">Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="f3753-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="f3753-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="f3753-385">Die angegebene Datei wird derzeit in einer Office synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="f3753-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="f3753-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-386">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-387">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="f3753-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="f3753-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="f3753-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span></span>

<span data-ttu-id="f3753-390">ResetCache löscht den Cache, der der suppliedID zugeordnet ist, die bei Initialize bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="f3753-391">Dies umfasst alle Dateiinformationen, die Dateien werden jedoch sowohl auf dem Client als auch auf dem Server gespeichert.</span><span class="sxs-lookup"><span data-stu-id="f3753-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="f3753-392">Diese Methode belässt das Objekt auch in einem teilweise nicht initialisierten Zustand.</span><span class="sxs-lookup"><span data-stu-id="f3753-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="f3753-393">Die einzigen gültigen Aufrufe danach sind [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) oder [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="f3753-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="f3753-394">Diese Methode kann aufgerufen werden, wenn Initialize fehlschlägt und E_LSC_CACHEMISMATCH zurückgibt und den Cache löscht, der der SuppliedID zugeordnet ist, die mit dem fehlerhaften Aufruf bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="f3753-395">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-395">Parameters</span></span>

<span data-ttu-id="f3753-396">Keine</span><span class="sxs-lookup"><span data-stu-id="f3753-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-397">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-397">Return values</span></span>

|<span data-ttu-id="f3753-398">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-398">Value</span></span>|<span data-ttu-id="f3753-399">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-401">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="f3753-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="f3753-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-404">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-405">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="f3753-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="f3753-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="f3753-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="f3753-408">ServerFileChange weist das CsiSyncClient COM-Objekt an, die angegebene Datei zum Herunterladen zu markieren.</span><span class="sxs-lookup"><span data-stu-id="f3753-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="f3753-409">Wenn die Datei in einer Office zum Bearbeiten geöffnet ist, gibt diese Methode S_OK zurück, ohne die Datei zum Herunterladen zu markieren (die Anwendung sollte diesen Schritt bereits tun, wenn Änderungen vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="f3753-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="f3753-410">Diese Methode lässt Downloads zu, wenn sie zuvor als blockiert markiert wurde (siehe RenameFile).</span><span class="sxs-lookup"><span data-stu-id="f3753-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="f3753-411">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-411">Parameters</span></span>

|<span data-ttu-id="f3753-412">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-412">Parameter</span></span>|<span data-ttu-id="f3753-413">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="f3753-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="f3753-415">Eine Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="f3753-416">Dieser Wert muss ein nicht leerer lokaler Pfad mit maximal 256 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="f3753-417">Dieser Pfad muss sich in der Verzeichnisstruktur befinden, die vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="f3753-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="f3753-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="f3753-419">Eine Zeichenfolge, die die ResourceID der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="f3753-420">Dieser Wert darf maximal 128 Zeichen lang sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="f3753-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="f3753-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="f3753-422">Eine Zeichenfolge, die die Datei auf dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f3753-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="f3753-423">Bei diesem Wert muss es sich um eine nicht leere gültige URL, jedoch nicht mehr als INTERNET_MAX_URL_LENGTH, wie durch https://support.microsoft.com/kb/208427 definiert.</span><span class="sxs-lookup"><span data-stu-id="f3753-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="f3753-424">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-424">Return values</span></span>

|<span data-ttu-id="f3753-425">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-425">Value</span></span>|<span data-ttu-id="f3753-426">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-428">Fehler beim Festlegen des Cacheverbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="f3753-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="f3753-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="f3753-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="f3753-430">Die von  _bstrFileSystemPath_ angegebene Datei hat eine andere ResourceID als angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3753-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="f3753-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="f3753-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="f3753-432">Die angegebene Dateierweiterung wird vom CsiSyncClient COM-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f3753-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="f3753-433">Weitere Informationen finden Sie unter GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="f3753-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="f3753-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="f3753-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="f3753-435">Die Datei wurde in der Mitte des Vorgangs gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f3753-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="f3753-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-437">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="f3753-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="f3753-439">Der angegebene FileSystemPath befindet sich nicht unter dem Verzeichnisstamm, der vom FileSystemDirectoryHint angegeben wurde, als der Aufruf von Initialize ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="f3753-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="f3753-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="f3753-443">Die durch  _bstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.</span><span class="sxs-lookup"><span data-stu-id="f3753-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="f3753-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="f3753-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="f3753-445">Die angegebene Datei hat bereits ausstehende Änderungen in einem anderen Cache und kann dem Cache des Verbrauchers noch nicht zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="f3753-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="f3753-447">Der bereitgestellte WebPath fällt unter einen anderen Cache.</span><span class="sxs-lookup"><span data-stu-id="f3753-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-448">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-449">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="f3753-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="f3753-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="f3753-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="f3753-452">Legt den Cache in einen Online- oder Offlinestatus fest.</span><span class="sxs-lookup"><span data-stu-id="f3753-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="f3753-453">Wenn sie offline Office, wird nicht versucht, mit dem Server für Dateien in diesem Cache zu kommunizieren, unabhängig von der _fBlockUploads-Einstellung_ jeder einzelnen Datei.</span><span class="sxs-lookup"><span data-stu-id="f3753-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="f3753-454">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-454">Parameters</span></span>

 <span data-ttu-id="f3753-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="f3753-455">_fIsOnline_</span></span>
  
<span data-ttu-id="f3753-456">Ein boolescher Wert, der den Verbindungsstatus des Caches bestimmt.</span><span class="sxs-lookup"><span data-stu-id="f3753-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-457">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-457">Return values</span></span>

|<span data-ttu-id="f3753-458">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-458">Value</span></span>|<span data-ttu-id="f3753-459">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-461">Fehler beim Festlegen des Cacheverbindungsstatus.</span><span class="sxs-lookup"><span data-stu-id="f3753-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="f3753-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-463">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-466">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-467">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="f3753-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="f3753-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="f3753-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span></span>

<span data-ttu-id="f3753-470">SetClientNetworkSyncPermission wird verwendet, um die Synchronisierungshuristiken vonOffice für Netzwerkkosten und Energieverbrauch zu überschreiben oder wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f3753-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="f3753-471">Wenn sie sich 3G oder einem anderen netzwerk mit hohen Kosten befinden oder wenn sie mit Akku betrieben werden oder angeschlossen werden, Office möglicherweise den Netzwerkdatenverkehr bis zu einem bestimmten Zeitpunkt blockieren.</span><span class="sxs-lookup"><span data-stu-id="f3753-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="f3753-472">Der Verbraucher dieser API kann sie verwenden, um die heuristischen Office zu überschreiben und die Synchronisierung zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="f3753-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="f3753-473">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-473">Parameters</span></span>

 <span data-ttu-id="f3753-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="f3753-474">_nspType_</span></span>
  
<span data-ttu-id="f3753-475">Ein Flag, das definiert, welche Kosten heuristisch überschrieben werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f3753-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="f3753-476">Weitere [Informationen finden Sie unter Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="f3753-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="f3753-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="f3753-477">_fEnableSync_</span></span>
  
<span data-ttu-id="f3753-478">Gibt an, ob die Synchronisierung erzwingen und damit heuristisch überschrieben oder nicht mehr außer Kraft gesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3753-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-479">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-479">Return values</span></span>

|<span data-ttu-id="f3753-480">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-480">Value</span></span>|<span data-ttu-id="f3753-481">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-483">Fehler beim Überschreiben der Synchronisierung von Heuristiken.</span><span class="sxs-lookup"><span data-stu-id="f3753-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="f3753-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-486">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-487">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="f3753-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="f3753-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="f3753-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span></span>

<span data-ttu-id="f3753-490">Entlädt den Cache aus dem COM-Objekt und führt schließende Vorgänge aus.</span><span class="sxs-lookup"><span data-stu-id="f3753-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="f3753-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUSS aufgerufen werden, bevor das COM-Objekt zerstört wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="f3753-492">Nach dem Aufgerufenen können keine anderen APIs aufgerufen werden, das COM-Objekt MUSS zerstört und ein neues erstellt werden, wenn Sie vorgänge fortsetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="f3753-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="f3753-493">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-493">Parameters</span></span>

<span data-ttu-id="f3753-494">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3753-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-495">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-495">Return values</span></span>

|<span data-ttu-id="f3753-496">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-496">Value</span></span>|<span data-ttu-id="f3753-497">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-499">Fehler beim Uninitialisieren.</span><span class="sxs-lookup"><span data-stu-id="f3753-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="f3753-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="f3753-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="f3753-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde in der Vergangenheit nicht erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="f3753-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-502">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-503">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="f3753-504">Schnittstelle IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="f3753-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="f3753-505">Diese Schnittstelle stellt eine Liste der ILSCEvent-Ereignisse dar.</span><span class="sxs-lookup"><span data-stu-id="f3753-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="f3753-506">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f3753-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="f3753-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="f3753-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="f3753-508">Ruft das nächste Ereignis aus der Liste der Ereignisse ab.</span><span class="sxs-lookup"><span data-stu-id="f3753-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="f3753-509">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-509">Parameters</span></span>

 <span data-ttu-id="f3753-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="f3753-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="f3753-511">Ein Zeiger auf eine ILSCEvent-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="f3753-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-512">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-512">Return values</span></span>

|<span data-ttu-id="f3753-513">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-513">Value</span></span>|<span data-ttu-id="f3753-514">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-516">Es gibt keine weiteren Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="f3753-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="f3753-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-517">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-518">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="f3753-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="f3753-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="f3753-520">Setzt den Enumerationszähler auf das erste Ereignis zurück.</span><span class="sxs-lookup"><span data-stu-id="f3753-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="f3753-521">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-521">Parameters</span></span>

<span data-ttu-id="f3753-522">Keine.</span><span class="sxs-lookup"><span data-stu-id="f3753-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-523">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-523">Return values</span></span>

<span data-ttu-id="f3753-524">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="f3753-525">Schnittstelle ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="f3753-525">Interface ILSCEvent</span></span>

<span data-ttu-id="f3753-526">Diese Schnittstelle stellt ein Synchronisierungsereignis dar.</span><span class="sxs-lookup"><span data-stu-id="f3753-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="f3753-527">Alle Informationen zum Ereignis können von der Schnittstelle abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="f3753-528">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f3753-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="f3753-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="f3753-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="f3753-530">Beachten Sie, dass dieser Wert aufgefüllt wird, wenn [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) aufgerufen wird, nicht beim Erstellen des Ereignisses. Daher haben Sie nur den aktuellen Status der Datei und nicht den Status der Datei, wenn sich der Konfliktstatus geändert hat.</span><span class="sxs-lookup"><span data-stu-id="f3753-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="f3753-531">Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnLocalConflictStateChanged.</span><span class="sxs-lookup"><span data-stu-id="f3753-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="f3753-532">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-532">Parameters</span></span>

 <span data-ttu-id="f3753-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="f3753-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="f3753-534">Der aktuelle Konfliktstatus der Datei, die dem Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f3753-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-535">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-535">Return values</span></span>

<span data-ttu-id="f3753-536">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="f3753-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="f3753-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="f3753-538">Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="f3753-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="f3753-539">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-539">Parameters</span></span>

 <span data-ttu-id="f3753-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="f3753-540">_pnError_</span></span>
  
<span data-ttu-id="f3753-541">Der diesem Ereignis zugeordnete Fehler.</span><span class="sxs-lookup"><span data-stu-id="f3753-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-542">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-542">Return values</span></span>

<span data-ttu-id="f3753-543">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="f3753-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="f3753-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="f3753-545">Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="f3753-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="f3753-546">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-546">Parameters</span></span>

 <span data-ttu-id="f3753-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="f3753-547">_pbstrETag_</span></span>
  
<span data-ttu-id="f3753-548">Das diesem Ereignis zugeordnete ETag</span><span class="sxs-lookup"><span data-stu-id="f3753-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-549">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-549">Return values</span></span>

<span data-ttu-id="f3753-550">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="f3753-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="f3753-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="f3753-552">Ruft den Typ für dieses Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="f3753-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="f3753-553">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-553">Parameters</span></span>

 <span data-ttu-id="f3753-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="f3753-554">_pnEventType_</span></span>
  
<span data-ttu-id="f3753-555">Der Ereignistyp dieses Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="f3753-555">The event type of this event.</span></span> <span data-ttu-id="f3753-556">Gültige [Werte finden Sie unter Enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)</span><span class="sxs-lookup"><span data-stu-id="f3753-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="f3753-557">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-558">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-558">Return values</span></span>

|<span data-ttu-id="f3753-559">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-559">Value</span></span>|<span data-ttu-id="f3753-560">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-562">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-563">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-564">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="f3753-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="f3753-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="f3753-566">Ruft den lokalen Arbeitspfad für dieses Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="f3753-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="f3753-567">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-567">Parameters</span></span>

 <span data-ttu-id="f3753-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="f3753-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="f3753-569">Der lokale Pfad der Datei, zu der dieses Ereignis führt.</span><span class="sxs-lookup"><span data-stu-id="f3753-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-570">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-570">Return values</span></span>

<span data-ttu-id="f3753-571">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="f3753-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="f3753-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="f3753-573">Ruft die Ressourcen-ID für das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="f3753-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="f3753-574">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-574">Parameters</span></span>

 <span data-ttu-id="f3753-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="f3753-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="f3753-576">Die ResourceID der Datei, die diesem Ereignis zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f3753-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="f3753-577">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-577">Return values</span></span>

<span data-ttu-id="f3753-578">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="f3753-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="f3753-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="f3753-580">Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="f3753-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="f3753-581">Wenn ein Aufruf von [ILSCLocalSyncClient::LocalFileChange, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange) [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) einen Webpfad- oder Lokalen Pfad-Kollision mit einer anderen Datei im Office-Dateicache verursachen würde, wird dieses Ereignis generiert.</span><span class="sxs-lookup"><span data-stu-id="f3753-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="f3753-582">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-582">Parameters</span></span>

 <span data-ttu-id="f3753-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="f3753-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="f3753-584">Die ResourceID, die dazu führte, dass dieses Ereignis generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="f3753-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="f3753-585">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-586">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-586">Return values</span></span>

<span data-ttu-id="f3753-587">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="f3753-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="f3753-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="f3753-589">Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded.</span><span class="sxs-lookup"><span data-stu-id="f3753-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="f3753-590">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-590">Parameters</span></span>

 <span data-ttu-id="f3753-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="f3753-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="f3753-592">Der diesem Ereignis zugeordnete Fehlertyp.</span><span class="sxs-lookup"><span data-stu-id="f3753-592">The error type associated with this event.</span></span> <span data-ttu-id="f3753-593">Mögliche Werte finden Sie [unter Enum LSCEventType.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType)</span><span class="sxs-lookup"><span data-stu-id="f3753-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="f3753-594">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-595">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-595">Return values</span></span>

|<span data-ttu-id="f3753-596">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-596">Value</span></span>|<span data-ttu-id="f3753-597">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-599">Mindestens ein Parameter ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-600">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-601">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="f3753-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="f3753-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="f3753-603">Dieser Wert wird nur aufgefüllt, wenn [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict.</span><span class="sxs-lookup"><span data-stu-id="f3753-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="f3753-604">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-604">Parameters</span></span>

 <span data-ttu-id="f3753-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="f3753-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="f3753-606">Gibt den diesem Ereignis zugeordneten Webpfad an.</span><span class="sxs-lookup"><span data-stu-id="f3753-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="f3753-607">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-608">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-608">Return values</span></span>

<span data-ttu-id="f3753-609">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="f3753-610">Schnittstelle ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="f3753-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="f3753-611">Diese Schnittstelle enthält zusätzliche Informationen zu einem Synchronisierungsereignis.</span><span class="sxs-lookup"><span data-stu-id="f3753-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="f3753-612">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f3753-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="f3753-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="f3753-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="f3753-614">Ruft die Fehlerketteninformationen zu einem Synchronisierungsereignis ab.</span><span class="sxs-lookup"><span data-stu-id="f3753-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="f3753-615">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-615">Parameters</span></span>

 <span data-ttu-id="f3753-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="f3753-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="f3753-617">Eine Zeichenfolge zum Halten der Fehlerketteninformationen.</span><span class="sxs-lookup"><span data-stu-id="f3753-617">A string to hold the error chain information.</span></span> <span data-ttu-id="f3753-618">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="f3753-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-619">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-619">Return values</span></span>

|<span data-ttu-id="f3753-620">Wert</span><span class="sxs-lookup"><span data-stu-id="f3753-620">Value</span></span>|<span data-ttu-id="f3753-621">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="f3753-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="f3753-623">Die installierte Version von Office unterstützt diese Schnittstelle nicht</span><span class="sxs-lookup"><span data-stu-id="f3753-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="f3753-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="f3753-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="f3753-625">Mindestens einer der Parameterwerte ist ungültig.</span><span class="sxs-lookup"><span data-stu-id="f3753-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="f3753-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="f3753-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="f3753-627">Die Informationen zur Fehlerkette sind nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f3753-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="f3753-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="f3753-628">S_OK</span></span>  <br/> |<span data-ttu-id="f3753-629">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="f3753-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="f3753-630">Schnittstelle IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="f3753-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="f3753-631">Diese Schnittstelle stellt eine Rückruffunktion für das CSISyncClient COM-Objekt bereit.</span><span class="sxs-lookup"><span data-stu-id="f3753-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="f3753-632">**Öffentliche Memberfunktionen**</span><span class="sxs-lookup"><span data-stu-id="f3753-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="f3753-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="f3753-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="f3753-634">Dies ist eine Rückruffunktion für das Objekt, das dem CsiSyncClient COM-Objekt übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="f3753-635">Es wird erwartet, dass beim Auftreten eines Ereignisses (siehe [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) für gültige Ereignistypen) das CsiSyncClient COM-Objekt diese Methode aufruft und den Consumer signalisiert.</span><span class="sxs-lookup"><span data-stu-id="f3753-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="f3753-636">Parameter</span><span class="sxs-lookup"><span data-stu-id="f3753-636">Parameters</span></span>

 <span data-ttu-id="f3753-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="f3753-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="f3753-638">Der Ereignistyp dieses Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="f3753-638">The event type of this event.</span></span> <span data-ttu-id="f3753-639">Gültige Werte finden Sie unter [Enum LSCEventTypeOccurred.](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred)</span><span class="sxs-lookup"><span data-stu-id="f3753-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="f3753-640">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="f3753-640">Return values</span></span>

<span data-ttu-id="f3753-641">Gibt immer S_OK.</span><span class="sxs-lookup"><span data-stu-id="f3753-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="f3753-642">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="f3753-642">Enumerations</span></span>

<span data-ttu-id="f3753-643">CSISyncClient verwendet die folgenden Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="f3753-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="f3753-644">Enum LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="f3753-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="f3753-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-645"><a name="Enum_LSCEventSyncErrorType"> </a></span></span>

<span data-ttu-id="f3753-646">Diese Aufzählung gibt die Kategorien von Fehlern an, die beim Synchronisieren einer Datei auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f3753-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="f3753-647">Enumerator</span><span class="sxs-lookup"><span data-stu-id="f3753-647">Enumerator</span></span>|<span data-ttu-id="f3753-648">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="f3753-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="f3753-650">Der Synchronisierungsfehler dieses Ereignisses war unerwartet und kann besondere Beachtung erfordern.</span><span class="sxs-lookup"><span data-stu-id="f3753-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="f3753-651">Standardmäßig muss der Benutzer möglicherweise eingreifen.</span><span class="sxs-lookup"><span data-stu-id="f3753-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="f3753-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="f3753-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="f3753-653">Der Synchronisierungsfehler dieses Ereignisses muss nicht besonders berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="f3753-654">Office wird automatisch ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f3753-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="f3753-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="f3753-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="f3753-656">Der Synchronisierungsfehler dieses Ereignisses erfordert, dass ein Benutzer ihn löst.</span><span class="sxs-lookup"><span data-stu-id="f3753-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="f3753-657">Beispielsweise erfordert der Zusammenführungskonfliktfehler, dass ein Benutzer das Dokument öffnet und zusammenführen muss.</span><span class="sxs-lookup"><span data-stu-id="f3753-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="f3753-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="f3753-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="f3753-659">Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Verbraucher interveniert, sollte jedoch vom Benutzer nicht besonders berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="f3753-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="f3753-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="f3753-661">Der Synchronisierungsfehler dieses Ereignisses erfordert, dass der Verbraucher als Sonderfall interveniert.</span><span class="sxs-lookup"><span data-stu-id="f3753-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="f3753-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="f3753-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="f3753-663">Enum LSCEventType</span><span class="sxs-lookup"><span data-stu-id="f3753-663">Enum LSCEventType</span></span>
<span data-ttu-id="f3753-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-664"><a name="Enum_LSCEventType"> </a></span></span>

<span data-ttu-id="f3753-665">Diese Enumeration gibt den Typ der Ereignisse an, die für eine bestimmte Datei auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f3753-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="f3753-666">Enumerator</span><span class="sxs-lookup"><span data-stu-id="f3753-666">Enumerator</span></span>|<span data-ttu-id="f3753-667">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="f3753-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="f3753-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="f3753-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="f3753-670">An einer lokalen Datei wurden Änderungen vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="f3753-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="f3753-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="f3753-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="f3753-672">Ein Benutzer hat eine Datei geöffnet.</span><span class="sxs-lookup"><span data-stu-id="f3753-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="f3753-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="f3753-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="f3753-674">Das Herunterladen von Dateiänderungen vom Server wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f3753-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="f3753-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="f3753-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="f3753-676">Das Hochladen von Dateiänderungen auf den Server wurde abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="f3753-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="f3753-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="f3753-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="f3753-678">Der Seriendruckkonfliktstatus einer Datei hat sich geändert.</span><span class="sxs-lookup"><span data-stu-id="f3753-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="f3753-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="f3753-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="f3753-680">Es wurde eine Datei hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f3753-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="f3753-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="f3753-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="f3753-682">Eine Datei wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="f3753-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="f3753-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="f3753-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="f3753-684">Die Synchronisierung wurde für die Dateien eines Benutzers aktiviert.</span><span class="sxs-lookup"><span data-stu-id="f3753-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="f3753-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="f3753-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="f3753-686">Das Herunterladen von Dateiänderungen vom Server wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="f3753-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="f3753-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="f3753-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="f3753-688">Es wurde begonnen, Dateiänderungen auf den Server hochzuladen.</span><span class="sxs-lookup"><span data-stu-id="f3753-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="f3753-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="f3753-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="f3753-690">Dieses Ereignis wird generiert, wenn ein Aufruf von [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) einen Webpfad- oder lokalen Pfadzusammenstoß mit einer anderen Datei im Office-Dateicache verursacht.</span><span class="sxs-lookup"><span data-stu-id="f3753-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="f3753-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="f3753-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="f3753-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="f3753-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="f3753-693">Enum LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="f3753-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="f3753-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-694"><a name="Enum_LSCEventTypeOccurred"> </a></span></span>

<span data-ttu-id="f3753-695">Diese Aufzählung gibt den Typ der Ereignisse an, die auftreten können.</span><span class="sxs-lookup"><span data-stu-id="f3753-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="f3753-696">Der Consumer muss bestimmte ILSCLocalSyncClient-Funktionen basierend auf dem Ereignistyp aufrufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="f3753-697">Enumerator</span><span class="sxs-lookup"><span data-stu-id="f3753-697">Enumerator</span></span>|<span data-ttu-id="f3753-698">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="f3753-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="f3753-700">Ein ILSCEvent ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="f3753-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="f3753-701">Der Consumer sollte [ILSCLocalSyncClient::GetChanges aufrufen, ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) um die Daten abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="f3753-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="f3753-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="f3753-703">Die unterstützten Dateierweiterungen haben sich geändert.</span><span class="sxs-lookup"><span data-stu-id="f3753-703">The supported file extensions have changed.</span></span> <span data-ttu-id="f3753-704">Der Consumer sollte [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) aufrufen, um die neue Liste der unterstützten Erweiterungen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="f3753-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="f3753-705">Enum LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="f3753-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="f3753-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span></span>

<span data-ttu-id="f3753-707">Diese Enumeration gibt die Flags an, die für eine Heuristik der Netzwerkkosten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f3753-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="f3753-708">Enumerator</span><span class="sxs-lookup"><span data-stu-id="f3753-708">Enumerator</span></span>|<span data-ttu-id="f3753-709">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="f3753-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="f3753-711">True, wenn die Kostenhuristik für teure Netzwerke (z. B. 3G) außer Kraft gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="f3753-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="f3753-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="f3753-713">True, wenn die Kostenhuristik für den Energieverbrauch (z. B. ein Akku) außer Kraft gesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="f3753-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="f3753-714">Enum LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="f3753-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="f3753-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="f3753-715"><a name="Enum_LSCStatusFlag"> </a></span></span>

<span data-ttu-id="f3753-716">Diese Enumeration wird verwendet, um den Synchronisierungsstatus einer Datei zu repräsentieren.</span><span class="sxs-lookup"><span data-stu-id="f3753-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="f3753-717">Enumerator</span><span class="sxs-lookup"><span data-stu-id="f3753-717">Enumerator</span></span>|<span data-ttu-id="f3753-718">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f3753-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="f3753-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="f3753-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="f3753-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="f3753-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="f3753-721">True, wenn ausstehende Daten an die Serverdatei gesendet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f3753-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="f3753-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="f3753-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="f3753-723">True, wenn ausstehende Daten aus der Serverdatei heruntergeladen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="f3753-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="f3753-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="f3753-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="f3753-725">True, wenn die Daten, Office die Datei im Cache enthält, die neueste Kopie der Daten auf dem Datenträger sind.</span><span class="sxs-lookup"><span data-stu-id="f3753-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

