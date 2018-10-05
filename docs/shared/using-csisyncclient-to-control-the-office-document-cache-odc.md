---
title: Verwendung von CSISyncClient zum Steuern der Office-Dokument-Cache (ODC)
manager: soliver
ms.date: 07/13/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 394b8e6f-9132-4c98-8fd6-46ad3c871440
description: Erfahren Sie, wie CSISyncClient verwenden, um die Office-Dokument-Cache (ODC) zu steuern.
ms.openlocfilehash: ce33063f88492bcd6f9682a4a6431fb36f138d55
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25399452"
---
# <a name="using-csisyncclient-to-control-the-office-document-cache-odc"></a><span data-ttu-id="dccef-103">Verwendung von CSISyncClient zum Steuern der Office-Dokument-Cache (ODC)</span><span class="sxs-lookup"><span data-stu-id="dccef-103">Using CSISyncClient to control the Office Document Cache (ODC)</span></span>

<span data-ttu-id="dccef-104">Erfahren Sie, wie CSISyncClient verwenden, um die Office-Dokument-Cache (ODC) zu steuern.</span><span class="sxs-lookup"><span data-stu-id="dccef-104">Learn how to use CSISyncClient to control the Office Document Cache (ODC).</span></span>
  
<span data-ttu-id="dccef-105">CSISyncClient ist ein Out-of-Proc-COM-Server (CsiSyncClient.exe), der Microsoft-OneDrive zum Steuern des Verhaltens der Office Dokument Cache (ODC) ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="dccef-105">CSISyncClient is an out-of-proc COM server (CsiSyncClient.exe) that allows Microsoft OneDrive to control the behavior of the Office Document Cache (ODC).</span></span> <span data-ttu-id="dccef-106">Zum Beispiel OneDrive rufen möglicherweise die ODC über CSISyncClient hoch-und Herunterladen von Dateien zu und von Endpunkten MS-FSSHTTP aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dccef-106">For example, OneDrive may call upon the ODC via CSISyncClient to upload and download files to and from MS-FSSHTTP enabled endpoints.</span></span> <span data-ttu-id="dccef-107">Auf diese Weise können die erweiterte Service-Backup-Funktionen in Office, wie gemeinsame dokumenterstellung und nahtlose Übergänge von offline zu online.</span><span class="sxs-lookup"><span data-stu-id="dccef-107">This enables advanced service-backed features in Office, such as co-authoring and seamless transitions from offline to online.</span></span>
  
<span data-ttu-id="dccef-108">CsiSyncClient ist im Office-Desktop (X86 und X64) verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dccef-108">CsiSyncClient is available in Office Desktop (both x86 and x64).</span></span> <span data-ttu-id="dccef-109">Hinweis: Während neuere Versionen von Office mit CsiSyncClient liefern können, wird der Prozess nur für Abwärtskompatibilität verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-109">Note: While newer versions of Office may ship with CsiSyncClient, the process will be used for backward compatibility only.</span></span> <span data-ttu-id="dccef-110">Die CsiSyncClient-Schnittstelle und die Methodik zum Steuern der ODC werden in zukünftigen Versionen von Office ändern.</span><span class="sxs-lookup"><span data-stu-id="dccef-110">The CsiSyncClient interface and the methodology of controlling the ODC will change in future versions of Office.</span></span>
  
<span data-ttu-id="dccef-111">Die Klassen-ID ist derzeit nur auf OneDrive reagieren festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dccef-111">The class ID is currently set to respond only to OneDrive.</span></span>
  
<span data-ttu-id="dccef-112">Das COM-Objekt kann als Out-of-Proc-com-Server verwendet werden und führt im CsiSyncClient.exe.</span><span class="sxs-lookup"><span data-stu-id="dccef-112">The COM object is usable as an out-of-proc COM server and runs in CsiSyncClient.exe.</span></span> <span data-ttu-id="dccef-113">Aufgrund von Einschränkungen mit Access (mit dem die ODC) mit der Bit-Typ, der in diesem Fall X64 Office kommt Office bedeutet, ein X64 dass wunderbare COM-Objekt oder X86 Office bedeutet, dass ein X86 COM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dccef-113">Due to limitations with Access (which the ODC uses), it ships with the bit type that Office comes in, so x64 Office means an x64 COM object, or x86 Office means an x86 COM object.</span></span> <span data-ttu-id="dccef-114">Mit dieser Einschränkung CLSCTX_LOCAL_SERVER angeben, wie Teil der CoCreateInstance das COM-Objekt als ein Out-of-Proc-com-Server verschoben, sodass Cross-Bitness Kompatibilität gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-114">To get around this limitation, specifying CLSCTX_LOCAL_SERVER as part of the CoCreateInstance will have the COM object be hosted as an out-of-proc COM server, allowing cross-bitness compatibility.</span></span>
  
## <a name="interfaces"></a><span data-ttu-id="dccef-115">Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="dccef-115">Interfaces</span></span>

<span data-ttu-id="dccef-116">CSISyncClient verwendet die folgenden Schnittstellen.</span><span class="sxs-lookup"><span data-stu-id="dccef-116">CSISyncClient uses the following interfaces.</span></span>
  
### <a name="interface-ilsclocalsyncclient"></a><span data-ttu-id="dccef-117">Schnittstelle ILSCLocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="dccef-117">Interface ILSCLocalSyncClient</span></span>

<span data-ttu-id="dccef-118">Dies ist die primäre Schnittstelle verwendet, um Dateien in Office zu synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-118">This is the primary interface used to synchronize files in Office.</span></span>
  
- <span data-ttu-id="dccef-119">ProgID: Office.LocalSyncClient</span><span class="sxs-lookup"><span data-stu-id="dccef-119">ProgID: Office.LocalSyncClient</span></span>
- <span data-ttu-id="dccef-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span><span class="sxs-lookup"><span data-stu-id="dccef-120">CLSID: {14286318-B6CF-49a1-81FC-D74AD94902F9}</span></span>
- <span data-ttu-id="dccef-121">Der Typbibliothek: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span><span class="sxs-lookup"><span data-stu-id="dccef-121">TypeLib: {66CDD37F-D313-4e81-8C31-4198F3E42C3C}</span></span>
   
<span data-ttu-id="dccef-122">Das COM-Objekt, das verfügbar gemacht wird, wird als Out-of-Proc-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="dccef-122">The COM object that is exposed is used as an out-of-proc server.</span></span> <span data-ttu-id="dccef-123">Angeben von CLSCTX_LOCAL_SERVER als Teil des CoCreateInstance ermöglicht Kompatibilität zwischen 64-Bit- und 32-Bit-Prozessen.</span><span class="sxs-lookup"><span data-stu-id="dccef-123">Specifying CLSCTX_LOCAL_SERVER as part of CoCreateInstance allows compatability between 64bit and 32bit processes.</span></span>
  
<span data-ttu-id="dccef-124">Nachdem Sie das COM-Objekt gemeinsam erstellt haben, müssen Sie zuerst [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-124">Once you've co-created the COM object, you MUST call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) first.</span></span> <span data-ttu-id="dccef-125">Sobald [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erfolgreich abgeschlossen wurde, können Sie eine beliebige API so oft wie gewünscht und in beliebiger Reihenfolge aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-125">Once [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has completed successfully, you may call any API as often as you wish and in any order.</span></span> <span data-ttu-id="dccef-126">Sie können auch [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) für ein bereits initialisiertes Objekt aufrufen, aber dies hat keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="dccef-126">You may also call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) on an already initialized object, but this does nothing.</span></span> 
  
<span data-ttu-id="dccef-127">Ausnahmen zu den vorherigen Absatz sind [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) und [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="dccef-127">The exceptions to the previous paragraph are [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) and [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="dccef-128">Nach dem Aufruf von [ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) auf das COM-Objekt müssen Sie dieses Objekt löschen und erstellen Sie einen neuen Anwendungspool.</span><span class="sxs-lookup"><span data-stu-id="dccef-128">After you call [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) on the COM object, you MUST destroy that object and create a new one.</span></span> <span data-ttu-id="dccef-129">[ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) wird Ihre Subcache löschen, löschen alle zugehörigen Dateiinformationen im Cache, doch lassen Sie die Dokumente auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="dccef-129">[ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) will delete your subcache, delete all associated file information in the cache, but leave the documents on disk.</span></span> <span data-ttu-id="dccef-130">Es intakt auch den Status für die Kommunikation mit dem Cache.</span><span class="sxs-lookup"><span data-stu-id="dccef-130">It also leaves the state intact for communicating with the cache.</span></span> <span data-ttu-id="dccef-131">Dadurch können Sie zum Aufrufen der [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) erneut aus, um einen neuen Cache ohne zerstören und das COM-Objekt neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="dccef-131">This allows you to call [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) again to create a new cache without having to destroy and recreate the COM object.</span></span> 
  
<span data-ttu-id="dccef-132">**Öffentliche Member-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="dccef-132">**Public member functions**</span></span>

#### <a name="ilsclocalsyncclientdeletefile"></a><span data-ttu-id="dccef-133">ILSCLocalSyncClient::DeleteFile</span><span class="sxs-lookup"><span data-stu-id="dccef-133">ILSCLocalSyncClient::DeleteFile</span></span>

<span data-ttu-id="dccef-134">DeleteFile wird verwendet, um die Dateiinformationen aus dem Cache zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="dccef-134">DeleteFile is used to remove the file information from the cache.</span></span> <span data-ttu-id="dccef-135">Diese Methode wird jedoch die zugehörige Datei auf der Festplatte und auf dem Server lassen.</span><span class="sxs-lookup"><span data-stu-id="dccef-135">However, this method will leave the associated file on disk and on the server.</span></span>
  
`HRESULT ILSCLocalSyncClient::DeleteFile ([in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="dccef-136">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-136">Parameters</span></span>

 <span data-ttu-id="dccef-137">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="dccef-137">_bstrResourceID_</span></span>
  
<span data-ttu-id="dccef-138">Die Zeichenfolge, die die ResourceID der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-138">The string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="dccef-139">Dieser Wert muss eine nicht leere mit bis zu 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="dccef-139">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-140">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-140">Return values</span></span>

|<span data-ttu-id="dccef-141">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-141">Value</span></span>|<span data-ttu-id="dccef-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-142">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-143">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-143">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-144">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-144">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-145">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-145">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-146">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-146">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-147">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-147">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-148">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-148">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-149">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="dccef-149">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="dccef-150">Der angegebene ResourceID ist nicht im Cache.</span><span class="sxs-lookup"><span data-stu-id="dccef-150">The given ResourceID is not in the cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-151">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-151">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-152">Die Initialisierung wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-152">Initialize has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-153">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="dccef-153">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="dccef-154">Die Datei wird derzeit synchronisiert oder geöffnet und kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-154">The file is currently synchronizing or open and cannot be deleted.</span></span>  <br/> |
|<span data-ttu-id="dccef-155">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-155">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-156">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-156">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetchanges"></a><span data-ttu-id="dccef-157">ILSCLocalSyncClient::GetChanges</span><span class="sxs-lookup"><span data-stu-id="dccef-157">ILSCLocalSyncClient::GetChanges</span></span>
<span data-ttu-id="dccef-158"><a name="ILSCLocalSyncClient_GetChanges"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-158"></span></span>

<span data-ttu-id="dccef-159">GetChanges gibt einen Enumerator von ILSCEvent-Objekten und auch gibt ein Token, das auf den nächsten Aufruf von GetChanges, vorausgesetzt, dass der Consumer verarbeitet wurden, die vorherige Gruppe von Ereignissen erfolgt ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-159">GetChanges returns an enumerator of ILSCEvent objects, and also returns a token that is given to the next call to GetChanges, assuming the consumer has processed the previous set of events.</span></span> <span data-ttu-id="dccef-160">Ereignisse vor dem _nPreviousChangesToken_ angegeben werden gelöscht und nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dccef-160">Events before the  _nPreviousChangesToken_ specified will be deleted and unavailable.</span></span> <span data-ttu-id="dccef-161">Wenn es keine Ereignisse sind verarbeitet werden, _PnCurrentChangesToken_ sollte den gleichen Wert wie _nPreviousChangesToken_sein, sondern _PpiEvents_ wird weiterhin festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-161">If there are no events to be processed,  _pnCurrentChangesToken_ should be the same value as  _nPreviousChangesToken_, but  _ppiEvents_ will still be set.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetChanges ([in] LONG nPreviousChangesToken, [out] LONG * pnCurrentChangesToken, [out] IEnumLSCEvent ** ppiEvents)`

##### <a name="parameters"></a><span data-ttu-id="dccef-162">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-162">Parameters</span></span>

 <span data-ttu-id="dccef-163">_nPreviousChangesToken_</span><span class="sxs-lookup"><span data-stu-id="dccef-163">_nPreviousChangesToken_</span></span>
  
<span data-ttu-id="dccef-164">Gibt an, welches Ereignis zuletzt vom Consumer verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-164">Identifies which event was last processed by the consumer.</span></span> 
  
 <span data-ttu-id="dccef-165">_pnCurrentChangesToken_</span><span class="sxs-lookup"><span data-stu-id="dccef-165">_pnCurrentChangesToken_</span></span>
  
<span data-ttu-id="dccef-166">Gibt das letzte Ereignis an Consumer übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-166">Identifies the most recent event being handed to the consumer.</span></span> <span data-ttu-id="dccef-167">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-167">Must not be null.</span></span>
  
 <span data-ttu-id="dccef-168">_ppiEvents_</span><span class="sxs-lookup"><span data-stu-id="dccef-168">_ppiEvents_</span></span>
  
<span data-ttu-id="dccef-169">Ein Enumerator für die Ereignisse, die an die Consumer übergeben.</span><span class="sxs-lookup"><span data-stu-id="dccef-169">An enumerator for the events handed to the consumer.</span></span> <span data-ttu-id="dccef-170">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-170">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-171">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-171">Return values</span></span>

|<span data-ttu-id="dccef-172">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-172">Value</span></span>|<span data-ttu-id="dccef-173">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-173">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-174">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-174">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-175">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-175">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-176">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-176">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-177">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-177">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-178">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-178">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-179">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-179">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-180">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-180">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-181">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-181">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetclientnetworksyncpermission"></a><span data-ttu-id="dccef-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="dccef-182">ILSCLocalSyncClient::GetClientNetworkSyncPermission</span></span>

<span data-ttu-id="dccef-183">GetClientNetworkSyncPermission wird verwendet, um abzufragen, ob die Synchronisierung des Office-Heuristik für Netzwerk-Kosten und Stromverbrauchs außer Kraft gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-183">GetClientNetworkSyncPermission is used to query whether Office's synchronizing heuristics for network cost and power usage are overridden.</span></span> <span data-ttu-id="dccef-184">Auf einer 3G oder ein anderes Netzwerk hohe Kosten oder bei der Ausführung auf Batterie im Vergleich zu eingesteckt wird, können Office bis zu einem Zeitpunkt mehr angebracht Netzwerkverkehr zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-184">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span>
  
`HRESULT ILSCLocalSyncClient::GetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [out] VARIANT_BOOL * pfSyncEnabled)`

##### <a name="parameters"></a><span data-ttu-id="dccef-185">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-185">Parameters</span></span>

 <span data-ttu-id="dccef-186">_nspType_</span><span class="sxs-lookup"><span data-stu-id="dccef-186">_nspType_</span></span>
  
<span data-ttu-id="dccef-187">Ein Flag, das welche Kosten heuristische zur Abfrage definiert.</span><span class="sxs-lookup"><span data-stu-id="dccef-187">A flag which defines which cost heuristic to query.</span></span> <span data-ttu-id="dccef-188">Finden Sie unter [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="dccef-188">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span> 
  
 <span data-ttu-id="dccef-189">_pfSyncEnabled_</span><span class="sxs-lookup"><span data-stu-id="dccef-189">_pfSyncEnabled_</span></span>
  
<span data-ttu-id="dccef-190">Gibt an, ob die angeforderte Kosten Heuristik derzeit überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-190">Specifies whether the requested cost heuristic is currently overridden or not.</span></span> <span data-ttu-id="dccef-191">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-191">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-192">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-192">Return values</span></span>

|<span data-ttu-id="dccef-193">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-193">Value</span></span>|<span data-ttu-id="dccef-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-194">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-195">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-195">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-196">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-196">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-197">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-197">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-198">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-198">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-199">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-199">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-200">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-200">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-201">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-201">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-202">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-202">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetfilestatus"></a><span data-ttu-id="dccef-203">ILSCLocalSyncClient::GetFileStatus</span><span class="sxs-lookup"><span data-stu-id="dccef-203">ILSCLocalSyncClient::GetFileStatus</span></span>

<span data-ttu-id="dccef-204">GetFileStatus wird verwendet, um das Sammeln von Informationen für eine bestimmte Datei:, ob im Cache vorhanden ist, hat ausstehende Kommunikation mit der Kopie auf dem Server und Office 2013 den aktuellsten Datumsdaten aus der lokalen Kopie hat.</span><span class="sxs-lookup"><span data-stu-id="dccef-204">GetFileStatus is used to gather information for a specific file: whether it exists in the cache, if it has pending communication with the server copy, and if Office 2013 has the most up to date data from the local copy.</span></span> <span data-ttu-id="dccef-205">Es erfordert eine bitweise Kennzeichnung von [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) Werten, welche Informationen bestimmen die CsiSyncClient COM-Objekt für Abfragen.</span><span class="sxs-lookup"><span data-stu-id="dccef-205">It requires a bitwise flag of [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag) values to determine what information the CsiSyncClient COM object is to query for.</span></span> 
  
`HRESULT ILSCLocalSyncClient::GetFileStatus ([in] BSTR bstrResourceID, [in] LSCStatusFlag sfRequestedStatus, [out] BSTR * pbstrFileSystemPath, [out] BSTR * pbstrETag, [out] LSCStatusFlag * psfFileStatus)`

##### <a name="parameters"></a><span data-ttu-id="dccef-206">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-206">Parameters</span></span>

 <span data-ttu-id="dccef-207">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="dccef-207">_bstrResourceID_</span></span>
  
<span data-ttu-id="dccef-208">Die Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-208">The string which identifies the file on the client.</span></span> <span data-ttu-id="dccef-209">Dieser Wert muss nicht leer ist, mit bis zu 128 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-209">This value must be non-empty, with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="dccef-210">_sfRequestedStatus_</span><span class="sxs-lookup"><span data-stu-id="dccef-210">_sfRequestedStatus_</span></span>
  
<span data-ttu-id="dccef-211">Ein Flag das definiert, welche Informationen zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="dccef-211">A flag which defines what information to return.</span></span> <span data-ttu-id="dccef-212">Finden Sie unter [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="dccef-212">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
 <span data-ttu-id="dccef-213">_pbstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="dccef-213">_pbstrFileSystemPath_</span></span>
  
<span data-ttu-id="dccef-214">Die Zeichenfolge, die den Speicherort der Datei _BstrResourceID_ auf dem Client identifizierten angibt.</span><span class="sxs-lookup"><span data-stu-id="dccef-214">The string which identifies the location of the file identified by  _bstrResourceID_ on the client.</span></span> <span data-ttu-id="dccef-215">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-215">Must not be null.</span></span> 
  
 <span data-ttu-id="dccef-216">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="dccef-216">_pbstrETag_</span></span>
  
<span data-ttu-id="dccef-217">Eine Zeichenfolge, die das eTag für die Datei _BstrResourceID_identifizierten enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-217">A string which will contain the eTag for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="dccef-218">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-218">Must not be null.</span></span> 
  
 <span data-ttu-id="dccef-219">_psfFileStatus_</span><span class="sxs-lookup"><span data-stu-id="dccef-219">_psfFileStatus_</span></span>
  
<span data-ttu-id="dccef-220">Ein Flag, das den Status über _SfRequestedStatus_ für die Datei _BstrResourceID_identifizierten angefordert enthalten wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-220">A flag which will contain the status requested via  _sfRequestedStatus_ for the file identified by  _bstrResourceID_.</span></span> <span data-ttu-id="dccef-221">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-221">Must not be null.</span></span> <span data-ttu-id="dccef-222">Finden Sie unter [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span><span class="sxs-lookup"><span data-stu-id="dccef-222">See [Enum LSCStatusFlag](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCStatusFlag).</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-223">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-223">Return values</span></span>

|<span data-ttu-id="dccef-224">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-224">Value</span></span>|<span data-ttu-id="dccef-225">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-225">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-226">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-226">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-227">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-227">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-228">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-228">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-229">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-229">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-230">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="dccef-230">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="dccef-231">Die Dateiinformationen durch _BstrResourceID_ angegeben ist im Cache nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="dccef-231">The file information specified by  _bstrResourceID_ does not exist in the cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-232">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="dccef-232">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="dccef-233">LSCStatusFlag_LocalFileUnchanged angefordert wurde oder durch _BstrResourceID_ angegebene Datei ist gesperrt oder fehlt.</span><span class="sxs-lookup"><span data-stu-id="dccef-233">LSCStatusFlag_LocalFileUnchanged was requested or the file specified by  _bstrResourceID_ is locked or missing.</span></span>  <br/> |
|<span data-ttu-id="dccef-234">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-234">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-235">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-235">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-236">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-236">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-237">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-237">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientgetsupportedfileextensions"></a><span data-ttu-id="dccef-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="dccef-238">ILSCLocalSyncClient::GetSupportedFileExtensions</span></span>
<span data-ttu-id="dccef-239"><a name="ILSCLocalSyncClient_GetSupportedFileExtensions"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-239"></span></span>

<span data-ttu-id="dccef-240">GetSupportedFileExtensions gibt eine Liste der senkrechte Striche getrennte Dateierweiterungen, die derzeit von der CsiSyncClient COM-Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-240">GetSupportedFileExtensions returns a list of pipe-delimited file extensions which are currently supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="dccef-241">Beachten Sie, dass dieser Liste kann sich ändern, und der Consumer über eine Änderung über das IPartnerActivityCallback-Objekt, das auf [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (finden Sie unter EventOccured) bereitgestellt benachrichtigt.</span><span class="sxs-lookup"><span data-stu-id="dccef-241">Note that this list may change, and the consumer will be notified of a change via the IPartnerActivityCallback object provided on [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) (See EventOccured).</span></span> 
  
<span data-ttu-id="dccef-242">Ein Beispiel für die Zeichenfolge zurückgegeben wird wie folgt: "| Docx | Docm | Pptx |"</span><span class="sxs-lookup"><span data-stu-id="dccef-242">An example of the string returned is as follows: "|docx|docm|pptx|"</span></span>
  
`HRESULT ILSCLocalSyncClient::GetSupportedFileExtensions ([out] BSTR * pbstrSupportedFileExtensions)`

##### <a name="parameters"></a><span data-ttu-id="dccef-243">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-243">Parameters</span></span>

 <span data-ttu-id="dccef-244">_pbstrSupportedFileExtensions_</span><span class="sxs-lookup"><span data-stu-id="dccef-244">_pbstrSupportedFileExtensions_</span></span>
  
<span data-ttu-id="dccef-245">Eine Zeichenfolge mit einer senkrechte Striche getrennte Dateierweiterungen unterstützt das CsiSyncClient COM-Objekt festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dccef-245">A string to be set with a pipe-delimited set of file extensions supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="dccef-246">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-246">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-247">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-247">Return values</span></span>

|<span data-ttu-id="dccef-248">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-248">Value</span></span>|<span data-ttu-id="dccef-249">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-249">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-250">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-250">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-251">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-251">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-252">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-252">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-253">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-253">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-254">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-254">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-255">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-255">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-256">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-256">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-257">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-257">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientinitialize"></a><span data-ttu-id="dccef-258">ILSCLocalSyncClient::Initialize</span><span class="sxs-lookup"><span data-stu-id="dccef-258">ILSCLocalSyncClient::Initialize</span></span>
<span data-ttu-id="dccef-259"><a name="ILSCLocalSyncClient_Initialize"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-259"></span></span>

<span data-ttu-id="dccef-260">Initialize muss die erste Methode aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-260">Initialize must be the first method called.</span></span> <span data-ttu-id="dccef-261">Andernfalls wird allen anderen APIs E_LSC_NOTINITIALIZED zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="dccef-261">Otherwise, all other APIs will return E_LSC_NOTINITIALIZED.</span></span> <span data-ttu-id="dccef-262">Initialize für ein bereits initialisiertes Objekt aufrufen, gibt S_OK zurück und hat keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="dccef-262">Calling Initialize on an already initialized object returns S_OK and does nothing.</span></span> <span data-ttu-id="dccef-263">Wenn E_LSC_CACHEMISMATCH zurückgegeben wird, kann der Aufrufer [ILSCLocalSyncClient::ResetCache](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) zum Löschen des Caches mit der angegebenen SuppliedID verknüpften aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-263">If E_LSC_CACHEMISMATCH is returned, the caller may call [ILSCLocalSyncClient::ResetCache ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ResetCache) to delete the cache associated with the given SuppliedID.</span></span> <span data-ttu-id="dccef-264">Allerdings werden in diesem Fall andere APIs weiterhin E_LSC_NOTINITIALIZED zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-264">However, in this case other APIs will still return E_LSC_NOTINITIALIZED.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Initialize ([in] BSTR bstrSuppliedID, [in] BSTR bstrProgID, [in] BSTR bstrFileSystemDirectoryHint, [in] IPartnerActivityCallback * pEventCallback, [out] VARIANT_BOOL * pfCreatedNewCache)`

##### <a name="parameters"></a><span data-ttu-id="dccef-265">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-265">Parameters</span></span>

 <span data-ttu-id="dccef-266">_bstrSuppliedID_</span><span class="sxs-lookup"><span data-stu-id="dccef-266">_bstrSuppliedID_</span></span>
  
<span data-ttu-id="dccef-267">Identifiziert die Consumer und der cache verwendet.</span><span class="sxs-lookup"><span data-stu-id="dccef-267">Identifies the consumer and which cache to use.</span></span> <span data-ttu-id="dccef-268">Muss nicht leeren mit bis zu 32 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="dccef-268">Must be non-empty with a maximum of 32 characters.</span></span> 
  
 <span data-ttu-id="dccef-269">_bstrProgID_</span><span class="sxs-lookup"><span data-stu-id="dccef-269">_bstrProgID_</span></span>
  
<span data-ttu-id="dccef-270">Identifiziert die Consumer COM-Objekt für die bidirektionale Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="dccef-270">Identifies the consumer's COM object for two-way communication.</span></span> <span data-ttu-id="dccef-271">Muss nicht leeren mit maximal 39 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="dccef-271">Must be non-empty with a maximum of 39 characters.</span></span> <span data-ttu-id="dccef-272">Finden Sie unter [ \<ProgID\> Schlüssel](https://docs.microsoft.com/windows/desktop/com/-progid--key) Weitere Informationen zu ProgIDs.</span><span class="sxs-lookup"><span data-stu-id="dccef-272">See [\<ProgID\> Key](https://docs.microsoft.com/windows/desktop/com/-progid--key) for more information about ProgIDs.</span></span> 
  
 <span data-ttu-id="dccef-273">_bstrFileSystemDirectoryHint_</span><span class="sxs-lookup"><span data-stu-id="dccef-273">_bstrFileSystemDirectoryHint_</span></span>
  
<span data-ttu-id="dccef-274">Gibt das Stammverzeichnis an, in dem lokale Dateien gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="dccef-274">Identifies the directory root in which local files will be stored.</span></span> <span data-ttu-id="dccef-275">Muss nicht leeren mit maximal 256 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="dccef-275">Must be non-empty with a maximum of 256 characters.</span></span> <span data-ttu-id="dccef-276">Das Verzeichnis muss bereits vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-276">The directory must already exist.</span></span> 
  
 <span data-ttu-id="dccef-277">_pEventCallback_</span><span class="sxs-lookup"><span data-stu-id="dccef-277">_pEventCallback_</span></span>
  
<span data-ttu-id="dccef-278">Das Callback-Schnittstelle die CsiSyncClient auf Änderungen informiert wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-278">The callback interface which CsiSyncClient will notify on changes.</span></span> <span data-ttu-id="dccef-279">Finden Sie unter IPartnerActivityCallback::EventOccurred.</span><span class="sxs-lookup"><span data-stu-id="dccef-279">See IPartnerActivityCallback::EventOccurred.</span></span> <span data-ttu-id="dccef-280">Dieser Wert darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-280">This value must not be null.</span></span> 
  
 <span data-ttu-id="dccef-281">_pfCreatedNewCache_</span><span class="sxs-lookup"><span data-stu-id="dccef-281">_pfCreatedNewCache_</span></span>
  
<span data-ttu-id="dccef-282">Gibt zurück, ob ein neuer Cache erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-282">Returns whether a new cache was created.</span></span> <span data-ttu-id="dccef-283">Wenn kein Cache mit der SuppliedID verknüpft ist, wird eine erstellt.</span><span class="sxs-lookup"><span data-stu-id="dccef-283">If no cache is associated with the SuppliedID, one will be created.</span></span> <span data-ttu-id="dccef-284">Dieser Wert darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-284">This value must not be null.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-285">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-285">Return values</span></span>

|<span data-ttu-id="dccef-286">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-286">Value</span></span>|<span data-ttu-id="dccef-287">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-287">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-288">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-288">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-289">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-289">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-290">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-290">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-291">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-291">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-292">E_LSC_CACHEMISMATCH</span><span class="sxs-lookup"><span data-stu-id="dccef-292">E_LSC_CACHEMISMATCH</span></span>  <br/> |<span data-ttu-id="dccef-293">Eine SuppliedID bereits einen mit ihm verbundenen Cache hat, jedoch eine unterschiedliche ProgId oder FileSystemDirectoryHint als bereitgestellten.</span><span class="sxs-lookup"><span data-stu-id="dccef-293">A SuppliedID already has a cache associated with it, but has a different ProgId or FileSystemDirectoryHint than the ones provided.</span></span>  <br/> |
|<span data-ttu-id="dccef-294">E_LSC_DIRECTORYHINTCONFLICT</span><span class="sxs-lookup"><span data-stu-id="dccef-294">E_LSC_DIRECTORYHINTCONFLICT</span></span>  <br/> |<span data-ttu-id="dccef-295">Die FileSystemDirectoryHint (oder einen Unterordner) auf einem anderen Cache bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-295">The FileSystemDirectoryHint (or a subfolder) already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-296">E_LAC_PROGIDCONFLICT</span><span class="sxs-lookup"><span data-stu-id="dccef-296">E_LAC_PROGIDCONFLICT</span></span>  <br/> |<span data-ttu-id="dccef-297">Die ProgID auf einem anderen Cache ist bereits vorhanden.</span><span class="sxs-lookup"><span data-stu-id="dccef-297">The ProgID already exists on a different cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-298">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-298">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-299">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-299">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientlocalfilechange"></a><span data-ttu-id="dccef-300">ILSCLocalSyncClient::LocalFileChange</span><span class="sxs-lookup"><span data-stu-id="dccef-300">ILSCLocalSyncClient::LocalFileChange</span></span>
<span data-ttu-id="dccef-301"><a name="ILSCLocalSyncClient_LocalFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-301"></span></span>

<span data-ttu-id="dccef-302">LocalFileChange wird verwendet, um das CsiSyncClient COM-Objekt zu versuchen, die angegebene Datei hochladen zu informieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-302">LocalFileChange is used to tell the CsiSyncClient COM object to attempt to upload the specified file.</span></span> <span data-ttu-id="dccef-303">Die Methode wird die Datei für den Upload, lesen die aktuellen Inhalt der Datei einschließlich vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="dccef-303">The method will prepare the file for upload, including reading the file's current contents.</span></span> <span data-ttu-id="dccef-304">Wenn ein Upload noch aussteht, vorherigen Uploads werden verworfen, und den neuen Inhalt für die vorbereitet hochladen.</span><span class="sxs-lookup"><span data-stu-id="dccef-304">If an upload is already pending, the previous upload will be discarded and the new contents prepared for upload.</span></span> <span data-ttu-id="dccef-305">Wenn die Datei zur Bearbeitung in einer Anwendung geöffnet ist, gibt diese Methode S_OK zurück, ohne zuvor die Datei für den Upload (die Anwendung sollte bereits diesen Schritt tun, wenn Änderungen vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="dccef-305">If the file is open for editing in an application, this method will return S_OK without preparing the file for upload (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="dccef-306">Diese Methode ermöglicht Uploads Wenn sie als markiert wurde hochgeladen blockierte zuvor (siehe [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span><span class="sxs-lookup"><span data-stu-id="dccef-306">This method will allow uploads if it was marked as uploads blocked previously (see [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile)).</span></span>
  
`HRESULT ILSCLocalSyncClient::LocalFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="dccef-307">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-307">Parameters</span></span>

 <span data-ttu-id="dccef-308">_bstrFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="dccef-308">_bstrFileSystemPath_</span></span>
  
<span data-ttu-id="dccef-309">Eine Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-309">A string which identifies the file on the client.</span></span> <span data-ttu-id="dccef-310">Dieser Wert muss eine nicht leere lokaler Pfad mit maximal 256 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-310">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="dccef-311">In diesem Pfad muss in der Verzeichnisstruktur durch die FileSystemDirectoryHint angegeben wird, wenn der Aufruf von [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) vorgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-311">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was made.</span></span> 
  
 <span data-ttu-id="dccef-312">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="dccef-312">_bstrResourceID_</span></span>
  
<span data-ttu-id="dccef-313">Eine Zeichenfolge, die die ResourceID der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-313">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="dccef-314">Dieser Wert muss eine nicht leere mit bis zu 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="dccef-314">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="dccef-315">_bstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="dccef-315">_bstrWebPath_</span></span>
  
<span data-ttu-id="dccef-316">Eine Zeichenfolge, die die Datei auf dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-316">A string which identifies the file on the server.</span></span> <span data-ttu-id="dccef-317">Dieser Wert muss nicht leeren, gültige URL, aber nicht mehr als INTERNET_MAX_URL_LENGTH, durch die definierten https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="dccef-317">This value must be non-empty, valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-318">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-318">Return values</span></span>

|<span data-ttu-id="dccef-319">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-319">Value</span></span>|<span data-ttu-id="dccef-320">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-320">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-321">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-321">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-322">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-322">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-323">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-323">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-324">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-324">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-325">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="dccef-325">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="dccef-326">Durch _BstrFileSystemPath_ angegebene Datei hat einen anderen ResourceID als angegeben.</span><span class="sxs-lookup"><span data-stu-id="dccef-326">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span> <span data-ttu-id="dccef-327">Wenn dieser Fehler zurückgegeben wird, wird ein Ereignis vom Typ LSCEventType_OnFilePathConflict gesendet.</span><span class="sxs-lookup"><span data-stu-id="dccef-327">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="dccef-328">Finden Sie unter [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="dccef-328">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="dccef-329">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="dccef-329">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="dccef-330">Die Datei wurde gelöschten Mid-Vorgang.</span><span class="sxs-lookup"><span data-stu-id="dccef-330">The file was deleted mid-operation.</span></span>  <br/> |
|<span data-ttu-id="dccef-331">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="dccef-331">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="dccef-332">Die angegebene Dateierweiterung wird durch das CsiSyncClient COM-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dccef-332">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="dccef-333">Finden Sie unter [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span><span class="sxs-lookup"><span data-stu-id="dccef-333">See [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions).</span></span>  <br/> |
|<span data-ttu-id="dccef-334">E_LSC_FILEUPTODATE</span><span class="sxs-lookup"><span data-stu-id="dccef-334">E_LSC_FILEUPTODATE</span></span>  <br/> |<span data-ttu-id="dccef-335">Das COM-Objekt keinen Upload planen, weil der Datei im Cache der letzten Änderung vom Datenträger waren.</span><span class="sxs-lookup"><span data-stu-id="dccef-335">The COM object did not schedule an upload because the file in the cache had the most recent changes from the disk.</span></span>  <br/> |
|<span data-ttu-id="dccef-336">E_LSC_LOCALFILEUNAVAILABLE</span><span class="sxs-lookup"><span data-stu-id="dccef-336">E_LSC_LOCALFILEUNAVAILABLE</span></span>  <br/> |<span data-ttu-id="dccef-337">Durch _BstrFileSystemPath_ angegebene Datei ist nicht vorhanden oder gesperrt.</span><span class="sxs-lookup"><span data-stu-id="dccef-337">The file specified by  _bstrFileSystemPath_ is missing or locked.</span></span>  <br/> |
|<span data-ttu-id="dccef-338">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="dccef-338">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="dccef-339">Der angegebene FileSystemPath ist nicht unter dem Stammverzeichnis, durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-339">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="dccef-340">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-340">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-341">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-341">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-342">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="dccef-342">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="dccef-343">Durch _BstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.</span><span class="sxs-lookup"><span data-stu-id="dccef-343">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="dccef-344">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="dccef-344">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="dccef-345">Die angegebene Datei bereits hat ausstehende Änderungen in einem anderen Cache und kann nicht noch die Consumer Cache zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-345">The file specified already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="dccef-346">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="dccef-347">Die bereitgestellten WebPath fällt unter einem anderen Cache.</span><span class="sxs-lookup"><span data-stu-id="dccef-347">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-348">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-348">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-349">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-349">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientrenamefile"></a><span data-ttu-id="dccef-350">ILSCLocalSyncClient::RenameFile</span><span class="sxs-lookup"><span data-stu-id="dccef-350">ILSCLocalSyncClient::RenameFile</span></span>
<span data-ttu-id="dccef-351"><a name="ILSCLocalSyncClient_RenameFile"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-351"></span></span>

<span data-ttu-id="dccef-352">RenameFile wird eine neue URL und den lokalen Pfad für einen bestimmten ResourceID zuordnen.</span><span class="sxs-lookup"><span data-stu-id="dccef-352">RenameFile will associate a new URL and local path for a given ResourceID.</span></span> <span data-ttu-id="dccef-353">Wenn die Datei mit der ResourceID angegebenen im Cache nicht bereits vorhanden ist, wird ein Versuch unternommen werden, erstellen und für den Download markieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-353">If the file specified by the ResourceID doesn't already exist in the cache, an attempt will be made to create it and mark it for download.</span></span>
  
`HRESULT ILSCLocalSyncClient::RenameFile ([in] BSTR bstrResourceID, [in] BSTR bstrNewFileSystemPath, [in] BSTR bstrNewWebPath, [in] VARIANT_BOOL fBlockUploads)`

##### <a name="parameters"></a><span data-ttu-id="dccef-354">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-354">Parameters</span></span>

 <span data-ttu-id="dccef-355">_bstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="dccef-355">_bstrResourceID_</span></span>
  
<span data-ttu-id="dccef-356">Eine Zeichenfolge, die die ResourceID der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-356">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="dccef-357">Dieser Wert muss eine nicht leere mit bis zu 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="dccef-357">This value must be non-empty with a maximum of 128 characters.</span></span> 
  
 <span data-ttu-id="dccef-358">_bstrNewFileSystemPath_</span><span class="sxs-lookup"><span data-stu-id="dccef-358">_bstrNewFileSystemPath_</span></span>
  
<span data-ttu-id="dccef-359">Eine Zeichenfolge, die den neuen lokalen Pfad für die Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="dccef-359">A string which specifies the new local path for the file.</span></span> <span data-ttu-id="dccef-360">Dieser Wert muss eine nicht leere lokaler Pfad mit maximal 256 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-360">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="dccef-361">In diesem Pfad muss in der Verzeichnisstruktur durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-361">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span> 
  
 <span data-ttu-id="dccef-362">_bstrNewWebPath_</span><span class="sxs-lookup"><span data-stu-id="dccef-362">_bstrNewWebPath_</span></span>
  
<span data-ttu-id="dccef-363">Eine Zeichenfolge, die die neue URL für die Datei angibt.</span><span class="sxs-lookup"><span data-stu-id="dccef-363">A string which specifies the new URL for the file.</span></span> <span data-ttu-id="dccef-364">Dieser Wert muss nicht leeren gültige URL, aber nicht mehr als INTERNET_MAX_URL_LENGTH, durch die definierten https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="dccef-364">This value must be non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span> 
  
 <span data-ttu-id="dccef-365">_fBlockUploads_</span><span class="sxs-lookup"><span data-stu-id="dccef-365">_fBlockUploads_</span></span>
  
<span data-ttu-id="dccef-366">Gibt an, ob Uploads am neuen Speicherort derzeit zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="dccef-366">Specifies whether uploads to the new location are allowed currently.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-367">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-367">Return values</span></span>

|<span data-ttu-id="dccef-368">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-368">Value</span></span>|<span data-ttu-id="dccef-369">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-369">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-370">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-370">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-371">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-371">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-372">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-372">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-373">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-373">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-374">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="dccef-374">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="dccef-375">Die _BstrNewFileSystemPath_ oder _BstrNewWebPath_ bereits vorhanden sind auf eine andere Datei in einem Cache.</span><span class="sxs-lookup"><span data-stu-id="dccef-375">The  _bstrNewFileSystemPath_ or  _bstrNewWebPath_ already exist on another file in any cache.</span></span> <span data-ttu-id="dccef-376">Wenn dieser Fehler zurückgegeben wird, wird ein Ereignis vom Typ LSCEventType_OnFilePathConflict gesendet.</span><span class="sxs-lookup"><span data-stu-id="dccef-376">An event of type LSCEventType_OnFilePathConflict is sent when this error is returned.</span></span> <span data-ttu-id="dccef-377">Finden Sie unter [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span><span class="sxs-lookup"><span data-stu-id="dccef-377">See [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges).</span></span>  <br/> |
|<span data-ttu-id="dccef-378">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="dccef-378">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="dccef-379">Die Dateiinformationen wurde aus dem Cache gelöscht, während diese Methode ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-379">The file information was deleted from the cache while this method was running.</span></span>  <br/> |
|<span data-ttu-id="dccef-380">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="dccef-380">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="dccef-381">Der angegebene FileSystemPath ist nicht unter dem Stammverzeichnis, durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-381">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="dccef-382">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-382">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-383">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-383">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-384">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="dccef-384">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="dccef-385">Die angegebene Datei wird in einer Office-Anwendung derzeit synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="dccef-385">The file specified is currently synchronizing in an Office application.</span></span>  <br/> |
|<span data-ttu-id="dccef-386">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-386">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-387">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-387">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientresetcache"></a><span data-ttu-id="dccef-388">ILSCLocalSyncClient::ResetCache</span><span class="sxs-lookup"><span data-stu-id="dccef-388">ILSCLocalSyncClient::ResetCache</span></span>
<span data-ttu-id="dccef-389"><a name="ILSCLocalSyncClient_ResetCache"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-389"></span></span>

<span data-ttu-id="dccef-390">ResetCache löscht den Cache der SuppliedID, die auf Initialize bereitgestellt wurde zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dccef-390">ResetCache will delete the cache associated with the SuppliedID that was provided on Initialize.</span></span> <span data-ttu-id="dccef-391">Dies umfasst alle Dateiinformationen, aber verlassen die Dateien auf dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="dccef-391">This includes all of the file information, but will leave the files on both the client and the server.</span></span> <span data-ttu-id="dccef-392">Diese Methode bewirkt, dass auch das Objekt eine teilweise nicht initialisiert.</span><span class="sxs-lookup"><span data-stu-id="dccef-392">This method also leaves the object in a partially uninitialized state.</span></span> <span data-ttu-id="dccef-393">Der einzige gültige Anrufe nach Dies sind [ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) oder [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span><span class="sxs-lookup"><span data-stu-id="dccef-393">The only valid calls after this are [ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) or [ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize).</span></span> <span data-ttu-id="dccef-394">Diese Methode kann aufgerufen werden, wenn Initialize schlägt fehl und E_LSC_CACHEMISMATCH gibt, und löscht den Cache der SuppliedID, die mit der fehlerhaften Anruf bereitgestellt wurde zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dccef-394">This method MAY be called if Initialize fails and returns E_LSC_CACHEMISMATCH, and will delete the cache associated with the SuppliedID that was provided with the failing call.</span></span>
  
`HRESULT ILSCLocalSyncClient::ResetCache()`

##### <a name="parameters"></a><span data-ttu-id="dccef-395">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-395">Parameters</span></span>

<span data-ttu-id="dccef-396">Keine</span><span class="sxs-lookup"><span data-stu-id="dccef-396">None</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-397">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-397">Return values</span></span>

|<span data-ttu-id="dccef-398">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-398">Value</span></span>|<span data-ttu-id="dccef-399">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-399">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-400">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-400">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-401">Der Aufruf ist fehlerhaft.</span><span class="sxs-lookup"><span data-stu-id="dccef-401">The call failed.</span></span>  <br/> |
|<span data-ttu-id="dccef-402">E_LSC_NOTINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-402">E_LSC_NOTINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-403">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht erfolgreich in der Vergangenheit aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-403">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) was not successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-404">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-404">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-405">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-405">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientserverfilechange"></a><span data-ttu-id="dccef-406">ILSCLocalSyncClient::ServerFileChange</span><span class="sxs-lookup"><span data-stu-id="dccef-406">ILSCLocalSyncClient::ServerFileChange</span></span>
<span data-ttu-id="dccef-407"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-407"></span></span>

<span data-ttu-id="dccef-408">ServerFileChange weist das CsiSyncClient COM-Objekt die angegebene Datei für den Download markieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-408">ServerFileChange tells the CsiSyncClient COM object to mark the specified file for download.</span></span> <span data-ttu-id="dccef-409">Wenn die Datei in einer Office-Anwendung für die Bearbeitung geöffnet ist, gibt diese Methode S_OK zurück, ohne markieren die Datei zum Herunterladen (die Anwendung sollte bereits diesen Schritt tun, wenn Änderungen vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="dccef-409">If the file is open in an Office application for edit, this method will return S_OK without marking the file for download (the application should already do this step if there are changes).</span></span>
  
<span data-ttu-id="dccef-410">Diese Methode ermöglicht, Downloads, wenn er als markiert wurde downloads blockierte zuvor (Siehe RenameFile).</span><span class="sxs-lookup"><span data-stu-id="dccef-410">This method will allow downloads if it was marked as downloads blocked previously (see RenameFile).</span></span>
  
`HRESULT ILSCLocalSyncClient::ServerFileChange ([in] BSTR bstrFileSystemPath, [in] BSTR bstrWebPath, [in] BSTR bstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="dccef-411">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-411">Parameters</span></span>

|<span data-ttu-id="dccef-412">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-412">Parameter</span></span>|<span data-ttu-id="dccef-413">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-413">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-414">bstrFileSystemPath</span><span class="sxs-lookup"><span data-stu-id="dccef-414">bstrFileSystemPath</span></span>  <br/> |<span data-ttu-id="dccef-415">Eine Zeichenfolge, die die Datei auf dem Client identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-415">A string which identifies the file on the client.</span></span> <span data-ttu-id="dccef-416">Dieser Wert muss eine nicht leere lokaler Pfad mit maximal 256 Zeichen sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-416">This value must be a non-empty local path with a maximum of 256 characters.</span></span> <span data-ttu-id="dccef-417">In diesem Pfad muss in der Verzeichnisstruktur durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-417">This path must be in the directory tree specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="dccef-418">bstrResourceID</span><span class="sxs-lookup"><span data-stu-id="dccef-418">bstrResourceID</span></span>  <br/> |<span data-ttu-id="dccef-419">Eine Zeichenfolge, die die ResourceID der Datei identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-419">A string which identifies the ResourceID of the file.</span></span> <span data-ttu-id="dccef-420">Dieser Wert muss eine nicht leere mit bis zu 128 Zeichen.</span><span class="sxs-lookup"><span data-stu-id="dccef-420">This value must be non-empty with a maximum of 128 characters.</span></span>  <br/> |
|<span data-ttu-id="dccef-421">bstrWebPath</span><span class="sxs-lookup"><span data-stu-id="dccef-421">bstrWebPath</span></span>  <br/> |<span data-ttu-id="dccef-422">Eine Zeichenfolge, die die Datei auf dem Server identifiziert.</span><span class="sxs-lookup"><span data-stu-id="dccef-422">A string which identifies the file on the server.</span></span> <span data-ttu-id="dccef-423">Dieser Wert muss eine gültige URL nicht leer, wird jedoch nicht mehr als INTERNET_MAX_URL_LENGTH, durch die definierten https://support.microsoft.com/kb/208427.</span><span class="sxs-lookup"><span data-stu-id="dccef-423">This value must be a non-empty valid URL, but no longer than INTERNET_MAX_URL_LENGTH, as defined by https://support.microsoft.com/kb/208427.</span></span>  <br/> |
   
##### <a name="return-values"></a><span data-ttu-id="dccef-424">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-424">Return values</span></span>

|<span data-ttu-id="dccef-425">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-425">Value</span></span>|<span data-ttu-id="dccef-426">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-426">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-427">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-427">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-428">Fehler bei der Cache Connectivity Zustand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dccef-428">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="dccef-429">E_LSC_CONFLICTINGFILE</span><span class="sxs-lookup"><span data-stu-id="dccef-429">E_LSC_CONFLICTINGFILE</span></span>  <br/> |<span data-ttu-id="dccef-430">Durch _BstrFileSystemPath_ angegebene Datei hat einen anderen ResourceID als angegeben.</span><span class="sxs-lookup"><span data-stu-id="dccef-430">The file specified by  _bstrFileSystemPath_ has a different ResourceID than specified.</span></span>  <br/> |
|<span data-ttu-id="dccef-431">E_LSC_FILENOTSUPPORTED</span><span class="sxs-lookup"><span data-stu-id="dccef-431">E_LSC_FILENOTSUPPORTED</span></span>  <br/> |<span data-ttu-id="dccef-432">Die angegebene Dateierweiterung wird durch das CsiSyncClient COM-Objekt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dccef-432">The given file extension is not supported by the CsiSyncClient COM object.</span></span> <span data-ttu-id="dccef-433">Finden Sie unter GetSupportedFileExtensions.</span><span class="sxs-lookup"><span data-stu-id="dccef-433">See GetSupportedFileExtensions.</span></span>  <br/> |
|<span data-ttu-id="dccef-434">E_LSC_FILENOTFOUND</span><span class="sxs-lookup"><span data-stu-id="dccef-434">E_LSC_FILENOTFOUND</span></span>  <br/> |<span data-ttu-id="dccef-435">Die Datei wurde in Mid Vorgang gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dccef-435">The file was deleted in mid-operation.</span></span>  <br/> |
|<span data-ttu-id="dccef-436">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-436">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-437">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-437">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-438">E_LSC_LOCALPATHNOTMAPPED</span><span class="sxs-lookup"><span data-stu-id="dccef-438">E_LSC_LOCALPATHNOTMAPPED</span></span>  <br/> |<span data-ttu-id="dccef-439">Der angegebene FileSystemPath ist nicht unter dem Stammverzeichnis, durch die FileSystemDirectoryHint angegeben werden, wenn die Initialize aufgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-439">The given FileSystemPath is not under the directory root specified by the FileSystemDirectoryHint when the call to Initialize was made.</span></span>  <br/> |
|<span data-ttu-id="dccef-440">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-440">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-441">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-441">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-442">E_LSC_PATHMISMATCH</span><span class="sxs-lookup"><span data-stu-id="dccef-442">E_LSC_PATHMISMATCH</span></span>  <br/> |<span data-ttu-id="dccef-443">Durch _BstrResourceID_ angegebene Datei hat einen anderen FileSystemPath als angegeben.</span><span class="sxs-lookup"><span data-stu-id="dccef-443">The file specified by  _bstrResourceID_ has a different FileSystemPath than specified.</span></span>  <br/> |
|<span data-ttu-id="dccef-444">E_LSC_PENDINGCHANGESINCACHE</span><span class="sxs-lookup"><span data-stu-id="dccef-444">E_LSC_PENDINGCHANGESINCACHE</span></span>  <br/> |<span data-ttu-id="dccef-445">Die angegebene Datei bereits ausstehende Änderungen in einem anderen Cache wurde und nicht noch die Consumer Cache zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-445">The specified file already has pending changes in a different cache and cannot yet be associated with the consumer's cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span><span class="sxs-lookup"><span data-stu-id="dccef-446">E_LSC_SERVERPATHINDIFFERENTCACHE</span></span>  <br/> |<span data-ttu-id="dccef-447">Die bereitgestellten WebPath fällt unter einem anderen Cache.</span><span class="sxs-lookup"><span data-stu-id="dccef-447">The WebPath provided falls under a different cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-448">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-448">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-449">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-449">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientconnectivitystate"></a><span data-ttu-id="dccef-450">ILSCLocalSyncClient::SetClientConnectivityState</span><span class="sxs-lookup"><span data-stu-id="dccef-450">ILSCLocalSyncClient::SetClientConnectivityState</span></span>
<span data-ttu-id="dccef-451"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-451"></span></span>

<span data-ttu-id="dccef-452">Wird der Cache in einem Zustand online oder offline.</span><span class="sxs-lookup"><span data-stu-id="dccef-452">Sets the cache into an online or offline state.</span></span> <span data-ttu-id="dccef-453">Wenn offline, versucht Office nicht mit dem Server für alle Dateien in diesem Cache, unabhängig von der Einstellung für jede einzelne Datei _fBlockUploads_ kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-453">If offline, Office will not attempt to communicate with the server for any files in that cache, regardless of each individual file's  _fBlockUploads_ setting.</span></span> 
  
`HRESULT ILSCLocalSyncClient::SetClientConnectivityState ([in] VARIANT_BOOL fIsOnline)`

##### <a name="parameters"></a><span data-ttu-id="dccef-454">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-454">Parameters</span></span>

 <span data-ttu-id="dccef-455">_fIsOnline_</span><span class="sxs-lookup"><span data-stu-id="dccef-455">_fIsOnline_</span></span>
  
<span data-ttu-id="dccef-456">Ermitteln des Status der Konnektivität des Caches ein boolescher Wert.</span><span class="sxs-lookup"><span data-stu-id="dccef-456">A boolean determining the connectivity state of the cache.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-457">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-457">Return values</span></span>

|<span data-ttu-id="dccef-458">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-458">Value</span></span>|<span data-ttu-id="dccef-459">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-459">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-460">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-460">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-461">Fehler bei der Cache Connectivity Zustand festgelegt.</span><span class="sxs-lookup"><span data-stu-id="dccef-461">Failure to set the cache connectivity state.</span></span>  <br/> |
|<span data-ttu-id="dccef-462">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-462">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-463">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-463">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-464">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-464">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-465">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-465">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-466">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-466">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-467">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-467">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientsetclientnetworksyncpermission"></a><span data-ttu-id="dccef-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span><span class="sxs-lookup"><span data-stu-id="dccef-468">ILSCLocalSyncClient::SetClientNetworkSyncPermission</span></span>
<span data-ttu-id="dccef-469"><a name="ILSCLocalSyncClient_ServerFileChange"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-469"></span></span>

<span data-ttu-id="dccef-470">SetClientNetworkSyncPermission wird verwendet, um entweder Override oder des RestoreOffice synchronisieren Heuristik für Netzwerk Verwendung Kosten und Leistung.</span><span class="sxs-lookup"><span data-stu-id="dccef-470">SetClientNetworkSyncPermission is used to either override or restoreOffice's synchronizing heuristics for network cost and power usage.</span></span> <span data-ttu-id="dccef-471">Auf einer 3G oder ein anderes Netzwerk hohe Kosten oder bei der Ausführung auf Batterie im Vergleich zu eingesteckt wird, können Office bis zu einem Zeitpunkt mehr angebracht Netzwerkverkehr zu blockieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-471">When on a 3G or other high cost network, or when running on battery versus being plugged in, Office may choose to block network traffic until a more opportune time.</span></span> <span data-ttu-id="dccef-472">Consumer dieser API können sie außer Kraft setzen des Office-Heuristik und erzwingen die Synchronisierung erfolgen.</span><span class="sxs-lookup"><span data-stu-id="dccef-472">The consumer of this API can use it to override Office's heuristics and force synchronizing to occur.</span></span>
  
`HRESULT ILSCLocalSyncClient::SetClientNetworkSyncPermission ([in] LSCNetworkSyncPermissionType nspType, [in] VARIANT_BOOL fEnableSync)`

##### <a name="parameters"></a><span data-ttu-id="dccef-473">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-473">Parameters</span></span>

 <span data-ttu-id="dccef-474">_nspType_</span><span class="sxs-lookup"><span data-stu-id="dccef-474">_nspType_</span></span>
  
<span data-ttu-id="dccef-475">Ein Kennzeichen, die definiert, welche Kosten heuristische außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="dccef-475">A flag which defines which cost heuristic to override.</span></span> <span data-ttu-id="dccef-476">Finden Sie unter [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span><span class="sxs-lookup"><span data-stu-id="dccef-476">See [Enum LSCNetworkSyncPermissionType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCNetworkSyncPermissionType).</span></span>
  
 <span data-ttu-id="dccef-477">_fEnableSync_</span><span class="sxs-lookup"><span data-stu-id="dccef-477">_fEnableSync_</span></span>
  
<span data-ttu-id="dccef-478">Gibt an, ob So erzwingen Sie synchronisieren auf, daher Überschreiben dieser Kosten heuristische, oder es nicht mehr zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="dccef-478">Specifies whether to force synchronizing on, thus overriding that cost heuristic, or to no longer override it.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-479">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-479">Return values</span></span>

|<span data-ttu-id="dccef-480">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-480">Value</span></span>|<span data-ttu-id="dccef-481">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-481">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-482">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-482">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-483">Fehler beim Synchronisieren von Heuristik außer Kraft gesetzt.</span><span class="sxs-lookup"><span data-stu-id="dccef-483">Failure to override synchronizing heuristics.</span></span>  <br/> |
|<span data-ttu-id="dccef-484">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-484">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-485">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-485">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-486">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-486">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-487">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-487">The call succeeded.</span></span>  <br/> |
   
#### <a name="ilsclocalsyncclientuninitialize"></a><span data-ttu-id="dccef-488">ILSCLocalSyncClient::Uninitialize</span><span class="sxs-lookup"><span data-stu-id="dccef-488">ILSCLocalSyncClient::Uninitialize</span></span>
<span data-ttu-id="dccef-489"><a name="ILSCLocalSyncClient_Uninitialize"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-489"></span></span>

<span data-ttu-id="dccef-490">Entlädt den Cache aus dem COM-Objekt und schließende Tag vom Typ Vorgänge ausführen.</span><span class="sxs-lookup"><span data-stu-id="dccef-490">Unloads the cache from the COM object and perform closing operations.</span></span> <span data-ttu-id="dccef-491">[ILSCLocalSyncClient::Uninitialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUSS vor dem Löschen des COM-Objekts aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-491">[ILSCLocalSyncClient::Uninitialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Uninitialize) MUST be called before destroying the COM object.</span></span> <span data-ttu-id="dccef-492">Nach dem Aufrufen keine anderen APIs aufgerufen werden kann, muss das COM-Objekt gelöscht werden, und eine neue erstellt wird, wenn Vorgänge fortgesetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="dccef-492">Once called, no other APIs can be called, the COM object MUST be destroyed and a new one created if you wish to continue operations.</span></span> 
  
`HRESULT ILSCLocalSyncClient::Uninitialize ()`

##### <a name="parameters"></a><span data-ttu-id="dccef-493">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-493">Parameters</span></span>

<span data-ttu-id="dccef-494">Keine.</span><span class="sxs-lookup"><span data-stu-id="dccef-494">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-495">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-495">Return values</span></span>

|<span data-ttu-id="dccef-496">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-496">Value</span></span>|<span data-ttu-id="dccef-497">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-497">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-498">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-498">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-499">Fehler beim Initialisieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-499">Failure to uninitialize.</span></span>  <br/> |
|<span data-ttu-id="dccef-500">E_LSC_NOINITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dccef-500">E_LSC_NOINITIALIZED</span></span>  <br/> |<span data-ttu-id="dccef-501">[ILSCLocalSyncClient::Initialize](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) wurde nicht in der Vergangenheit erfolgreich aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-501">[ILSCLocalSyncClient::Initialize ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_Initialize) has not been successfully called in the past.</span></span>  <br/> |
|<span data-ttu-id="dccef-502">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-502">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-503">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-503">The call succeeded.</span></span>  <br/> |
   
### <a name="interface-ienumlscevent"></a><span data-ttu-id="dccef-504">Schnittstelle IEnumLSCEvent</span><span class="sxs-lookup"><span data-stu-id="dccef-504">Interface IEnumLSCEvent</span></span>

<span data-ttu-id="dccef-505">Diese Schnittstelle stellt eine Liste der ILSCEvent Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="dccef-505">This interface represents a list of ILSCEvent events.</span></span>
  
<span data-ttu-id="dccef-506">**Öffentliche Member-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="dccef-506">**Public member functions**</span></span>

#### <a name="ienumlsceventfnext"></a><span data-ttu-id="dccef-507">IEnumLSCEvent::FNext</span><span class="sxs-lookup"><span data-stu-id="dccef-507">IEnumLSCEvent::FNext</span></span>

<span data-ttu-id="dccef-508">Ruft das nächste Ereignis aus der Liste der Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="dccef-508">Retrieves the next event from the list of events.</span></span>
  
`HRESULT IEnumLSCEvent::FNext ([out] ILSCEvent ** ppiLSCEvent)`

##### <a name="parameters"></a><span data-ttu-id="dccef-509">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-509">Parameters</span></span>

 <span data-ttu-id="dccef-510">_ppiLSCEvent_</span><span class="sxs-lookup"><span data-stu-id="dccef-510">_ppiLSCEvent_</span></span>
  
<span data-ttu-id="dccef-511">Ein Zeiger auf eine ILSCEvent-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="dccef-511">A pointer to an ILSCEvent interface.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-512">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-512">Return values</span></span>

|<span data-ttu-id="dccef-513">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-513">Value</span></span>|<span data-ttu-id="dccef-514">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-514">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-515">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-515">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-516">Es sind keine weiteren Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="dccef-516">There are no more events.</span></span>  <br/> |
|<span data-ttu-id="dccef-517">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-517">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-518">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-518">The call was successful.</span></span>  <br/> |
   
#### <a name="ienumlsceventreset"></a><span data-ttu-id="dccef-519">IEnumLSCEvent::Reset</span><span class="sxs-lookup"><span data-stu-id="dccef-519">IEnumLSCEvent::Reset</span></span>

<span data-ttu-id="dccef-520">Setzt den Enumerator auf das erste Ereignis zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-520">Resets the enumerator to the first event.</span></span>
  
`HRESULT IEnumLSCEvent::Reset ()`

##### <a name="parameters"></a><span data-ttu-id="dccef-521">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-521">Parameters</span></span>

<span data-ttu-id="dccef-522">Keine.</span><span class="sxs-lookup"><span data-stu-id="dccef-522">None.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-523">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-523">Return values</span></span>

<span data-ttu-id="dccef-524">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-524">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent"></a><span data-ttu-id="dccef-525">Schnittstelle ILSCEvent</span><span class="sxs-lookup"><span data-stu-id="dccef-525">Interface ILSCEvent</span></span>

<span data-ttu-id="dccef-526">Diese Schnittstelle stellt ein Ereignis synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-526">This interface represents a synchronizing event.</span></span> <span data-ttu-id="dccef-527">Alle Informationen über das Ereignis kann über die Benutzeroberfläche abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-527">All information about the event can be retrieved from the interface.</span></span>
  
<span data-ttu-id="dccef-528">**Öffentliche Member-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="dccef-528">**Public member functions**</span></span>

#### <a name="ilsceventgetconflictstatus"></a><span data-ttu-id="dccef-529">ILSCEvent::GetConflictStatus</span><span class="sxs-lookup"><span data-stu-id="dccef-529">ILSCEvent::GetConflictStatus</span></span>

<span data-ttu-id="dccef-530">Beachten Sie, dass dieser Wert [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) aufgerufen wird nicht, wenn das Ereignis erstellt wurde, damit Sie nur verfügen, werden den aktuellen Status der Datei, die nicht den Status der Datei ein, wenn der Status Konflikt geändert, aufgefüllt wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-530">Note that this value is populated when [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) is called, not when the event was created, so you will only have the current status of the file, not the status of the file when the conflict status changed.</span></span> 
  
<span data-ttu-id="dccef-531">Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnLocalConflictStateChanged ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-531">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnLocalConflictStateChanged.</span></span> 
  
`HRESULT ILSCEvent::GetConflictStatus ([out] VARIANT_BOOL * pfIsInConflict)`

##### <a name="parameters"></a><span data-ttu-id="dccef-532">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-532">Parameters</span></span>

 <span data-ttu-id="dccef-533">_pfIsInConflict_</span><span class="sxs-lookup"><span data-stu-id="dccef-533">_pfIsInConflict_</span></span>
  
<span data-ttu-id="dccef-534">Der aktuelle Konflikt Status der Datei mit dem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-534">The current conflict status of the file associated with the event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-535">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-535">Return values</span></span>

<span data-ttu-id="dccef-536">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-536">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeterror"></a><span data-ttu-id="dccef-537">ILSCEvent::GetError</span><span class="sxs-lookup"><span data-stu-id="dccef-537">ILSCEvent::GetError</span></span>

<span data-ttu-id="dccef-538">Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-538">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetError ([out] LONG * pnError)`

##### <a name="parameters"></a><span data-ttu-id="dccef-539">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-539">Parameters</span></span>

 <span data-ttu-id="dccef-540">_pnError_</span><span class="sxs-lookup"><span data-stu-id="dccef-540">_pnError_</span></span>
  
<span data-ttu-id="dccef-541">Der Fehler, die mit diesem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-541">The error associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-542">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-542">Return values</span></span>

<span data-ttu-id="dccef-543">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-543">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetetag"></a><span data-ttu-id="dccef-544">ILSCEvent::GetETag</span><span class="sxs-lookup"><span data-stu-id="dccef-544">ILSCEvent::GetETag</span></span>

<span data-ttu-id="dccef-545">Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-545">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetETag ([out] BSTR * pbstrETag)`

##### <a name="parameters"></a><span data-ttu-id="dccef-546">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-546">Parameters</span></span>

 <span data-ttu-id="dccef-547">_pbstrETag_</span><span class="sxs-lookup"><span data-stu-id="dccef-547">_pbstrETag_</span></span>
  
<span data-ttu-id="dccef-548">Das ETag mit diesem Ereignis verknüpft ist</span><span class="sxs-lookup"><span data-stu-id="dccef-548">The ETag associated with this event</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-549">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-549">Return values</span></span>

<span data-ttu-id="dccef-550">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-550">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgeteventtype"></a><span data-ttu-id="dccef-551">ILSCEvent::GetEventType</span><span class="sxs-lookup"><span data-stu-id="dccef-551">ILSCEvent::GetEventType</span></span>

<span data-ttu-id="dccef-552">Ruft den Typ für dieses Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="dccef-552">Gets the type for this event.</span></span>
  
`HRESULT ILSCEvent::GetEventType ([out] LSCEventType * pnEventType)`

##### <a name="parameters"></a><span data-ttu-id="dccef-553">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-553">Parameters</span></span>

 <span data-ttu-id="dccef-554">_pnEventType_</span><span class="sxs-lookup"><span data-stu-id="dccef-554">_pnEventType_</span></span>
  
<span data-ttu-id="dccef-555">Den Ereignistyp dieses Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="dccef-555">The event type of this event.</span></span> <span data-ttu-id="dccef-556">Gültige Werte finden Sie unter [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) .</span><span class="sxs-lookup"><span data-stu-id="dccef-556">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for valid values.</span></span> <span data-ttu-id="dccef-557">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-557">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-558">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-558">Return values</span></span>

|<span data-ttu-id="dccef-559">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-559">Value</span></span>|<span data-ttu-id="dccef-560">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-560">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-561">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-561">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-562">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-562">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-563">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-563">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-564">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-564">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetlocalworkingpath"></a><span data-ttu-id="dccef-565">ILSCEvent::GetLocalWorkingPath</span><span class="sxs-lookup"><span data-stu-id="dccef-565">ILSCEvent::GetLocalWorkingPath</span></span>

<span data-ttu-id="dccef-566">Ruft den lokalen Arbeitspfad für dieses Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="dccef-566">Gets the local working path for this event.</span></span>
  
`HRESULT ILSCEvent::GetLocalWorkingPath ([out] BSTR * pbstrLocalWorkingPath)`

##### <a name="parameters"></a><span data-ttu-id="dccef-567">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-567">Parameters</span></span>

 <span data-ttu-id="dccef-568">_pbstrLocalWorkingPath_</span><span class="sxs-lookup"><span data-stu-id="dccef-568">_pbstrLocalWorkingPath_</span></span>
  
<span data-ttu-id="dccef-569">Der lokale Pfad der Datei auf der dieses Ereignis bezieht.</span><span class="sxs-lookup"><span data-stu-id="dccef-569">The local path of the file to which this event pertains.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-570">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-570">Return values</span></span>

<span data-ttu-id="dccef-571">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-571">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceid"></a><span data-ttu-id="dccef-572">ILSCEvent::GetResourceID</span><span class="sxs-lookup"><span data-stu-id="dccef-572">ILSCEvent::GetResourceID</span></span>

<span data-ttu-id="dccef-573">Ruft die Ressourcen-ID für das Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="dccef-573">Gets the resource ID for the event.</span></span>
  
`HRESULT ILSCEvent::GetResourceID ([out] BSTR * pbstrResourceID)`

##### <a name="parameters"></a><span data-ttu-id="dccef-574">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-574">Parameters</span></span>

 <span data-ttu-id="dccef-575">_pbstrResourceID_</span><span class="sxs-lookup"><span data-stu-id="dccef-575">_pbstrResourceID_</span></span>
  
<span data-ttu-id="dccef-576">Die ResourceID der Datei mit diesem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-576">The ResourceID of the file associated with this event.</span></span>
  
##### <a name="return-values"></a><span data-ttu-id="dccef-577">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-577">Return values</span></span>

<span data-ttu-id="dccef-578">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-578">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetresourceidattempted"></a><span data-ttu-id="dccef-579">ILSCEvent::GetResourceIDAttempted</span><span class="sxs-lookup"><span data-stu-id="dccef-579">ILSCEvent::GetResourceIDAttempted</span></span>

<span data-ttu-id="dccef-580">Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-580">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> <span data-ttu-id="dccef-581">Wenn Sie ein Anruf an [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange)oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) einen Konflikt Web oder lokalen Pfad durch eine andere Datei in den Cache für den Office-Dateien, würde dies Ereignis wird generiert.</span><span class="sxs-lookup"><span data-stu-id="dccef-581">When a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) would cause a Web Path or Local Path collision with another file in the Office file cache, this event is generated.</span></span> 
  
`HRESULT ILSCEvent::GetResourceIDAttempted ([out] BSTR * pbstrResourceIDAttempted)`

##### <a name="parameters"></a><span data-ttu-id="dccef-582">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-582">Parameters</span></span>

 <span data-ttu-id="dccef-583">_pbstrResourceIDAttempted_</span><span class="sxs-lookup"><span data-stu-id="dccef-583">_pbstrResourceIDAttempted_</span></span>
  
<span data-ttu-id="dccef-584">Die ResourceID, das dieses Ereignis generiert werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-584">The ResourceID that caused this event to get generated.</span></span> <span data-ttu-id="dccef-585">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-585">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-586">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-586">Return values</span></span>

<span data-ttu-id="dccef-587">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-587">Always returns S_OK.</span></span> 
  
#### <a name="ilsceventgetsyncerrortype"></a><span data-ttu-id="dccef-588">ILSCEvent::GetSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="dccef-588">ILSCEvent::GetSyncErrorType</span></span>

<span data-ttu-id="dccef-589">Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnServerChangesDownloaded oder LSCEventType_OnLocalChangesUploaded ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-589">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnServerChangesDownloaded or LSCEventType_OnLocalChangesUploaded.</span></span> 
  
`HRESULT ILSCEvent::GetSyncErrorType ([out] LSCEventSyncErrorType * pnSyncErrorType)`

##### <a name="parameters"></a><span data-ttu-id="dccef-590">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-590">Parameters</span></span>

 <span data-ttu-id="dccef-591">_pnSyncErrorType_</span><span class="sxs-lookup"><span data-stu-id="dccef-591">_pnSyncErrorType_</span></span>
  
<span data-ttu-id="dccef-592">Den Fehlertyp mit diesem Ereignis verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-592">The error type associated with this event.</span></span> <span data-ttu-id="dccef-593">Mögliche Werte finden Sie unter [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) .</span><span class="sxs-lookup"><span data-stu-id="dccef-593">See [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) for potential values.</span></span> <span data-ttu-id="dccef-594">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-594">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-595">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-595">Return values</span></span>

|<span data-ttu-id="dccef-596">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-596">Value</span></span>|<span data-ttu-id="dccef-597">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-597">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-598">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-598">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-599">Ein oder mehrere Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-599">One or more parameters are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-600">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-600">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-601">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-601">The call was successful.</span></span>  <br/> |
   
#### <a name="ilsceventgetwebpath"></a><span data-ttu-id="dccef-602">ILSCEvent::GetWebPath</span><span class="sxs-lookup"><span data-stu-id="dccef-602">ILSCEvent::GetWebPath</span></span>

<span data-ttu-id="dccef-603">Dieser Wert wird nur aufgefüllt, wenn die [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) des Ereignisses LSCEventType_OnFilePathConflict ist.</span><span class="sxs-lookup"><span data-stu-id="dccef-603">This value is only populated when the [Enum LSCEventType](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventType) of the event is LSCEventType_OnFilePathConflict.</span></span> 
  
`HRESULT ILSCEvent::GetWebPath ([out] BSTR * pbstrWebPath)`

##### <a name="parameters"></a><span data-ttu-id="dccef-604">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-604">Parameters</span></span>

 <span data-ttu-id="dccef-605">_pbstrWebPath_</span><span class="sxs-lookup"><span data-stu-id="dccef-605">_pbstrWebPath_</span></span>
  
<span data-ttu-id="dccef-606">Gibt den Web-Pfad dieses Ereignis zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="dccef-606">Specifies the Web Path associated with this event.</span></span> <span data-ttu-id="dccef-607">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-607">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-608">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-608">Return values</span></span>

<span data-ttu-id="dccef-609">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-609">Always returns S_OK.</span></span> 
  
### <a name="interface-ilscevent2"></a><span data-ttu-id="dccef-610">Schnittstelle ILSCEvent2</span><span class="sxs-lookup"><span data-stu-id="dccef-610">Interface ILSCEvent2</span></span>

<span data-ttu-id="dccef-611">Diese Schnittstelle enthält zusätzliche Informationen zu einem Ereignis synchronisieren.</span><span class="sxs-lookup"><span data-stu-id="dccef-611">This interface holds additional information about a synchronizing event.</span></span>
  
<span data-ttu-id="dccef-612">**Öffentliche Member-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="dccef-612">**Public member functions**</span></span>

#### <a name="ilscevent2geterrorchain"></a><span data-ttu-id="dccef-613">ILSCEvent2::GetErrorChain</span><span class="sxs-lookup"><span data-stu-id="dccef-613">ILSCEvent2::GetErrorChain</span></span>

<span data-ttu-id="dccef-614">Ruft die Kette Fehlerinformationen zu einem Synchronisieren von Ereignis ab.</span><span class="sxs-lookup"><span data-stu-id="dccef-614">Gets the error chain information about a synchronizing event.</span></span>
  
`HRESULT ILSCEvent2::GetErrorChain ([out] BSTR * pbstrErrorChain)`

##### <a name="parameters"></a><span data-ttu-id="dccef-615">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-615">Parameters</span></span>

 <span data-ttu-id="dccef-616">_pbstrErrorChain_</span><span class="sxs-lookup"><span data-stu-id="dccef-616">_pbstrErrorChain_</span></span>
  
<span data-ttu-id="dccef-617">Eine Zeichenfolge, die die Fehlerinformationen Kette enthalten soll.</span><span class="sxs-lookup"><span data-stu-id="dccef-617">A string to hold the error chain information.</span></span> <span data-ttu-id="dccef-618">Darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="dccef-618">Must not be null.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-619">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-619">Return values</span></span>

|<span data-ttu-id="dccef-620">Wert</span><span class="sxs-lookup"><span data-stu-id="dccef-620">Value</span></span>|<span data-ttu-id="dccef-621">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-621">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-622">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="dccef-622">E_NOTIMPL</span></span>  <br/> |<span data-ttu-id="dccef-623">Die installierte Version von Office wird diese Schnittstelle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dccef-623">The installed version of Office does not support this interface</span></span>  <br/> |
|<span data-ttu-id="dccef-624">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="dccef-624">E_INVALIDARG</span></span>  <br/> |<span data-ttu-id="dccef-625">Eine oder mehrere der Werte für Parameter sind ungültig.</span><span class="sxs-lookup"><span data-stu-id="dccef-625">One or more of the parameter values are invalid.</span></span>  <br/> |
|<span data-ttu-id="dccef-626">E_FAIL</span><span class="sxs-lookup"><span data-stu-id="dccef-626">E_FAIL</span></span>  <br/> |<span data-ttu-id="dccef-627">Die Fehlerinformationen Kette ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="dccef-627">The error chain information is not available.</span></span>  <br/> |
|<span data-ttu-id="dccef-628">S_OK</span><span class="sxs-lookup"><span data-stu-id="dccef-628">S_OK</span></span>  <br/> |<span data-ttu-id="dccef-629">Der Aufruf war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="dccef-629">The call was successful.</span></span>  <br/> |
   
### <a name="interface-ipartneractivitycallback"></a><span data-ttu-id="dccef-630">Schnittstelle IPartnerActivityCallback</span><span class="sxs-lookup"><span data-stu-id="dccef-630">Interface IPartnerActivityCallback</span></span>

<span data-ttu-id="dccef-631">Diese Schnittstelle stellt eine Rückruffunktion, die das CSISyncClient COM-Objekt.</span><span class="sxs-lookup"><span data-stu-id="dccef-631">This interface provides a callback function to the CSISyncClient COM object.</span></span>
  
<span data-ttu-id="dccef-632">**Öffentliche Member-Funktionen**</span><span class="sxs-lookup"><span data-stu-id="dccef-632">**Public member functions**</span></span>

#### <a name="ipartneractivitycallbackeventoccurred"></a><span data-ttu-id="dccef-633">IPartnerActivityCallback::EventOccurred</span><span class="sxs-lookup"><span data-stu-id="dccef-633">IPartnerActivityCallback::EventOccurred</span></span>

<span data-ttu-id="dccef-634">Dies ist eine Rückruffunktion für das Objekt, das CsiSyncClient COM-Objekt zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="dccef-634">This is a callback function on the object given to the CsiSyncClient COM object.</span></span> <span data-ttu-id="dccef-635">Es wird erwartet, dass beim Eintreten Ereignisses dieses (Gültige Ereignistypen finden Sie unter [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) ) CsiSyncClient COM-Objekt dieser Methode, den Consumer Signalisierung aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-635">It's expected that when an Event occurs (see [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid event types), the CsiSyncClient COM object will call this method, signalling the consumer.</span></span> 
  
`HRESULT IPartnerActivityCallback::EventOccurred ([in] LSCEventTypeOccurred eEventTypeOccurred)`

##### <a name="parameters"></a><span data-ttu-id="dccef-636">Parameter</span><span class="sxs-lookup"><span data-stu-id="dccef-636">Parameters</span></span>

 <span data-ttu-id="dccef-637">_eEventTypeOccurred_</span><span class="sxs-lookup"><span data-stu-id="dccef-637">_eEventTypeOccurred_</span></span>
  
<span data-ttu-id="dccef-638">Den Ereignistyp dieses Ereignisses.</span><span class="sxs-lookup"><span data-stu-id="dccef-638">The event type of this event.</span></span> <span data-ttu-id="dccef-639">Gültige Werte finden Sie unter [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) .</span><span class="sxs-lookup"><span data-stu-id="dccef-639">See [Enum LSCEventTypeOccurred](using-csisyncclient-to-control-the-office-document-cache-odc.md#Enum_LSCEventTypeOccurred) for valid values.</span></span> 
  
##### <a name="return-values"></a><span data-ttu-id="dccef-640">Rückgabewerte</span><span class="sxs-lookup"><span data-stu-id="dccef-640">Return values</span></span>

<span data-ttu-id="dccef-641">Gibt immer S_OK zurück.</span><span class="sxs-lookup"><span data-stu-id="dccef-641">Always returns S_OK.</span></span>
  
## <a name="enumerations"></a><span data-ttu-id="dccef-642">Enumerationen</span><span class="sxs-lookup"><span data-stu-id="dccef-642">Enumerations</span></span>

<span data-ttu-id="dccef-643">CSISyncClient verwendet die folgenden Aufzählungen.</span><span class="sxs-lookup"><span data-stu-id="dccef-643">CSISyncClient uses the following enumerations.</span></span>
  
### <a name="enum-lsceventsyncerrortype"></a><span data-ttu-id="dccef-644">Enum LSCEventSyncErrorType</span><span class="sxs-lookup"><span data-stu-id="dccef-644">Enum LSCEventSyncErrorType</span></span>
<span data-ttu-id="dccef-645"><a name="Enum_LSCEventSyncErrorType"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-645"></span></span>

<span data-ttu-id="dccef-646">Diese Enumeration gibt die Kategorien von Fehlern, die beim Synchronisieren einer Datei auftreten können.</span><span class="sxs-lookup"><span data-stu-id="dccef-646">This enumeration specifies the categories of errors that can occur while synchronizing a file.</span></span>
  
|<span data-ttu-id="dccef-647">Enumerator</span><span class="sxs-lookup"><span data-stu-id="dccef-647">Enumerator</span></span>|<span data-ttu-id="dccef-648">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-648">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span><span class="sxs-lookup"><span data-stu-id="dccef-649">LSCEventSyncErrorType_UserInterventionRequiredUnexpected</span></span>  <br/> |<span data-ttu-id="dccef-650">Synchronisieren von Fehlers dieses Ereignisses wurde unerwartet und besondere Aufmerksamkeit erfordern.</span><span class="sxs-lookup"><span data-stu-id="dccef-650">The synchronizing error of this event was unexpected, and may require special consideration.</span></span> <span data-ttu-id="dccef-651">Der Benutzer möglicherweise eingreifen.</span><span class="sxs-lookup"><span data-stu-id="dccef-651">By default, the user may have to intervene.</span></span>  <br/> |
|<span data-ttu-id="dccef-652">LSCEventSyncErrorType_NoInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="dccef-652">LSCEventSyncErrorType_NoInterventionRequired</span></span>  <br/> |<span data-ttu-id="dccef-653">Der Synchronisierung von Fehler dieses Ereignisses braucht nicht besonders beachtet.</span><span class="sxs-lookup"><span data-stu-id="dccef-653">The synchronizing error of this event does not need special consideration.</span></span> <span data-ttu-id="dccef-654">Office wird es automatisch behandelt werden.</span><span class="sxs-lookup"><span data-stu-id="dccef-654">Office will handle it automatically.</span></span>  <br/> |
|<span data-ttu-id="dccef-655">LSCEventSyncErrorType_UserInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="dccef-655">LSCEventSyncErrorType_UserInterventionRequired</span></span>  <br/> |<span data-ttu-id="dccef-656">Der Synchronisierung von Fehler dieses Ereignisses bewirkt, dass einen Benutzer Behebung.</span><span class="sxs-lookup"><span data-stu-id="dccef-656">The synchronizing error of this event requires a user to resolve it.</span></span> <span data-ttu-id="dccef-657">Fehler beim Zusammenführen der Konflikt muss beispielsweise ein Benutzer öffnen Sie das Dokument und zusammenführen.</span><span class="sxs-lookup"><span data-stu-id="dccef-657">For example, merge conflict error requires a user to open the document and merge it.</span></span>  <br/> |
|<span data-ttu-id="dccef-658">LSCEventSyncErrorType_WaitingOnClient</span><span class="sxs-lookup"><span data-stu-id="dccef-658">LSCEventSyncErrorType_WaitingOnClient</span></span>  <br/> |<span data-ttu-id="dccef-659">Der Synchronisierung von Fehler dieses Ereignisses erfordert den Consumer eingreifen, aber nicht besonders beachtet durch den Benutzer erforderlich sein soll.</span><span class="sxs-lookup"><span data-stu-id="dccef-659">The synchronizing error of this event requires the consumer to intervene, but should not require special consideration by the user.</span></span>  <br/> |
|<span data-ttu-id="dccef-660">LSCEventSyncErrorType_ClientInterventionRequired</span><span class="sxs-lookup"><span data-stu-id="dccef-660">LSCEventSyncErrorType_ClientInterventionRequired</span></span>  <br/> |<span data-ttu-id="dccef-661">Der Synchronisierung Fehler dieses Ereignisses erfordert den Consumer als Sonderfall eingreifen.</span><span class="sxs-lookup"><span data-stu-id="dccef-661">The synchronizing error of this event requires the consumer to intervene as a special case.</span></span>  <br/> |
|<span data-ttu-id="dccef-662">LSCEventSyncErrorType_Max</span><span class="sxs-lookup"><span data-stu-id="dccef-662">LSCEventSyncErrorType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtype"></a><span data-ttu-id="dccef-663">Enum LSCEventType</span><span class="sxs-lookup"><span data-stu-id="dccef-663">Enum LSCEventType</span></span>
<span data-ttu-id="dccef-664"><a name="Enum_LSCEventType"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-664"></span></span>

<span data-ttu-id="dccef-665">Diese Enumeration gibt die Art der Ereignisse, die für eine bestimmte Datei auftreten können.</span><span class="sxs-lookup"><span data-stu-id="dccef-665">This enumeration specifies the type of events that can occur for a particular file.</span></span>
  
|<span data-ttu-id="dccef-666">Enumerator</span><span class="sxs-lookup"><span data-stu-id="dccef-666">Enumerator</span></span>|<span data-ttu-id="dccef-667">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-667">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-668">LSCEventType_None</span><span class="sxs-lookup"><span data-stu-id="dccef-668">LSCEventType_None</span></span>  <br/> ||
|<span data-ttu-id="dccef-669">LSCEventType_OnLocalChanges</span><span class="sxs-lookup"><span data-stu-id="dccef-669">LSCEventType_OnLocalChanges</span></span>  <br/> |<span data-ttu-id="dccef-670">Änderungen wurden in einer lokalen Datei vorgenommen.</span><span class="sxs-lookup"><span data-stu-id="dccef-670">Changes were made to a local file.</span></span>  <br/> |
|<span data-ttu-id="dccef-671">LSCEventType_OnOpenedByUser</span><span class="sxs-lookup"><span data-stu-id="dccef-671">LSCEventType_OnOpenedByUser</span></span>  <br/> |<span data-ttu-id="dccef-672">Ein Benutzer eine Datei geöffnet wurde.</span><span class="sxs-lookup"><span data-stu-id="dccef-672">A user opened a file.</span></span>  <br/> |
|<span data-ttu-id="dccef-673">LSCEventType_OnServerChangesDownloaded</span><span class="sxs-lookup"><span data-stu-id="dccef-673">LSCEventType_OnServerChangesDownloaded</span></span>  <br/> |<span data-ttu-id="dccef-674">Herunterladen der Datei Änderungen vom Server ist beendet.</span><span class="sxs-lookup"><span data-stu-id="dccef-674">Finished downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="dccef-675">LSCEventType_OnLocalChangesUploaded</span><span class="sxs-lookup"><span data-stu-id="dccef-675">LSCEventType_OnLocalChangesUploaded</span></span>  <br/> |<span data-ttu-id="dccef-676">Beendet die Datei Änderungen an den Server hochladen.</span><span class="sxs-lookup"><span data-stu-id="dccef-676">Finished uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="dccef-677">LSCEventType_OnLocalConflictStateChanged</span><span class="sxs-lookup"><span data-stu-id="dccef-677">LSCEventType_OnLocalConflictStateChanged</span></span>  <br/> |<span data-ttu-id="dccef-678">Der Zusammenführung Konflikt Status einer Datei wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="dccef-678">The merge conflict state of a file has changed.</span></span>  <br/> |
|<span data-ttu-id="dccef-679">LSCEventType_OnFileAdded</span><span class="sxs-lookup"><span data-stu-id="dccef-679">LSCEventType_OnFileAdded</span></span>  <br/> |<span data-ttu-id="dccef-680">Eine Datei wurde hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="dccef-680">A file was added.</span></span>  <br/> |
|<span data-ttu-id="dccef-681">LSCEventType_OnFileDeleted</span><span class="sxs-lookup"><span data-stu-id="dccef-681">LSCEventType_OnFileDeleted</span></span>  <br/> |<span data-ttu-id="dccef-682">Eine Datei wurde gelöscht.</span><span class="sxs-lookup"><span data-stu-id="dccef-682">A file was deleted.</span></span>  <br/> |
|<span data-ttu-id="dccef-683">LSCEventType_OnSyncEnabled</span><span class="sxs-lookup"><span data-stu-id="dccef-683">LSCEventType_OnSyncEnabled</span></span>  <br/> |<span data-ttu-id="dccef-684">Synchronisieren von wurde für Dateien des Benutzers aktiviert.</span><span class="sxs-lookup"><span data-stu-id="dccef-684">Synchronizing was enabled for a user's files.</span></span>  <br/> |
|<span data-ttu-id="dccef-685">LSCEventType_OnServerChangesDownloadStarted</span><span class="sxs-lookup"><span data-stu-id="dccef-685">LSCEventType_OnServerChangesDownloadStarted</span></span>  <br/> |<span data-ttu-id="dccef-686">Download von Änderungen vom Server gestartet.</span><span class="sxs-lookup"><span data-stu-id="dccef-686">Started downloading file changes from the server.</span></span>  <br/> |
|<span data-ttu-id="dccef-687">LSCEventType_OnLocalChangesUploadStarted</span><span class="sxs-lookup"><span data-stu-id="dccef-687">LSCEventType_OnLocalChangesUploadStarted</span></span>  <br/> |<span data-ttu-id="dccef-688">Schritte Hochladen der Datei Änderungen an den Server.</span><span class="sxs-lookup"><span data-stu-id="dccef-688">Started uploading file changes to the server.</span></span>  <br/> |
|<span data-ttu-id="dccef-689">LSCEventType_OnFilePathConflict</span><span class="sxs-lookup"><span data-stu-id="dccef-689">LSCEventType_OnFilePathConflict</span></span>  <br/> |<span data-ttu-id="dccef-690">Dieses Ereignis wird generiert, wenn ein Aufruf von [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), oder [ILSCLocalSyncClient::RenameFile](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) führt zu einem Konflikt Web oder lokalen Pfad durch eine andere Datei in der Zwischenspeicher für Office-Datei.</span><span class="sxs-lookup"><span data-stu-id="dccef-690">This event is generated when a call to [ILSCLocalSyncClient::LocalFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_LocalFileChange), [ILSCLocalSyncClient::ServerFileChange ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_ServerFileChange), or [ILSCLocalSyncClient::RenameFile ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_RenameFile) causes a Web Path or Local Path collision with another file in the Office file cache.</span></span>  <br/> |
|<span data-ttu-id="dccef-691">LSCEventType_OnFileForked</span><span class="sxs-lookup"><span data-stu-id="dccef-691">LSCEventType_OnFileForked</span></span>  <br/> ||
|<span data-ttu-id="dccef-692">LSCEventType_Max</span><span class="sxs-lookup"><span data-stu-id="dccef-692">LSCEventType_Max</span></span>  <br/> ||
   
### <a name="enum-lsceventtypeoccurred"></a><span data-ttu-id="dccef-693">Enum LSCEventTypeOccurred</span><span class="sxs-lookup"><span data-stu-id="dccef-693">Enum LSCEventTypeOccurred</span></span>
<span data-ttu-id="dccef-694"><a name="Enum_LSCEventTypeOccurred"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-694"></span></span>

<span data-ttu-id="dccef-695">Diese Enumeration gibt die Art der Ereignisse, die auftreten können.</span><span class="sxs-lookup"><span data-stu-id="dccef-695">This enumeration specifies the type of events that can occur.</span></span> <span data-ttu-id="dccef-696">Consumer muss bestimmte basierte auf den Ereignistyp ILSCLocalSyncClient-Funktionen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-696">The consumer needs to call specific ILSCLocalSyncClient functions based on the event type.</span></span>
  
|<span data-ttu-id="dccef-697">Enumerator</span><span class="sxs-lookup"><span data-stu-id="dccef-697">Enumerator</span></span>|<span data-ttu-id="dccef-698">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-698">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-699">LSCEventTypeOccurred_GetChanges</span><span class="sxs-lookup"><span data-stu-id="dccef-699">LSCEventTypeOccurred_GetChanges</span></span>  <br/> |<span data-ttu-id="dccef-700">Ein ILSCEvent ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="dccef-700">An ILSCEvent has occurred.</span></span> <span data-ttu-id="dccef-701">Consumer sollte [ILSCLocalSyncClient::GetChanges](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) zum Abrufen der Daten aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-701">The consumer should call [ILSCLocalSyncClient::GetChanges ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetChanges) to retrieve the data.</span></span>  <br/> |
|<span data-ttu-id="dccef-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span><span class="sxs-lookup"><span data-stu-id="dccef-702">LSCEventTypeOccurred_GetSupportedFileExtensions</span></span>  <br/> |<span data-ttu-id="dccef-703">Die unterstützten Dateierweiterungen wurden geändert.</span><span class="sxs-lookup"><span data-stu-id="dccef-703">The supported file extensions have changed.</span></span> <span data-ttu-id="dccef-704">Consumer sollte [ILSCLocalSyncClient::GetSupportedFileExtensions](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) zum Abrufen der neuen Liste mit unterstützten Erweiterungen aufrufen.</span><span class="sxs-lookup"><span data-stu-id="dccef-704">The consumer should call [ILSCLocalSyncClient::GetSupportedFileExtensions ](using-csisyncclient-to-control-the-office-document-cache-odc.md#ILSCLocalSyncClient_GetSupportedFileExtensions) to retrieve the new list of supported extensions.</span></span>  <br/> |
   
### <a name="enum-lscnetworksyncpermissiontype"></a><span data-ttu-id="dccef-705">Enum LSCNetworkSyncPermissionType</span><span class="sxs-lookup"><span data-stu-id="dccef-705">Enum LSCNetworkSyncPermissionType</span></span>
<span data-ttu-id="dccef-706"><a name="Enum_LSCNetworkSyncPermissionType"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-706"></span></span>

<span data-ttu-id="dccef-707">Diese Enumeration gibt die Kennzeichen für ein Netzwerk Kosten heuristische verwendet.</span><span class="sxs-lookup"><span data-stu-id="dccef-707">This enumeration specifies the flags used for a network cost heuristic.</span></span> 

|<span data-ttu-id="dccef-708">Enumerator</span><span class="sxs-lookup"><span data-stu-id="dccef-708">Enumerator</span></span>|<span data-ttu-id="dccef-709">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-709">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-710">LSCNetworkSyncPermissionType_HighCost</span><span class="sxs-lookup"><span data-stu-id="dccef-710">LSCNetworkSyncPermissionType_HighCost</span></span>  <br/> |<span data-ttu-id="dccef-711">True, wenn die Heuristik Kosten für teuren Netzwerke (z. B. 3 G) überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-711">True if the cost heuristic for expensive networks (such as 3G) is overridden.</span></span>  <br/> |
|<span data-ttu-id="dccef-712">LSCNetworkSyncPermissionType_HighPowerUsage</span><span class="sxs-lookup"><span data-stu-id="dccef-712">LSCNetworkSyncPermissionType_HighPowerUsage</span></span>  <br/> |<span data-ttu-id="dccef-713">True, wenn die Heuristik Kosten für die Verwendung von Power (beispielsweise eine Batterie) überschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="dccef-713">True if the cost heuristic for power usage (such as a battery) is overridden.</span></span>  <br/> |
   
### <a name="enum-lscstatusflag"></a><span data-ttu-id="dccef-714">Enum LSCStatusFlag</span><span class="sxs-lookup"><span data-stu-id="dccef-714">Enum LSCStatusFlag</span></span>
<span data-ttu-id="dccef-715"><a name="Enum_LSCStatusFlag"> </a></span><span class="sxs-lookup"><span data-stu-id="dccef-715"></span></span>

<span data-ttu-id="dccef-716">Diese Enumeration wird den Status Synchronisieren einer Datei darstellen.</span><span class="sxs-lookup"><span data-stu-id="dccef-716">This enumeration is used to represent the synchronize status of a file.</span></span> 
  
|<span data-ttu-id="dccef-717">Enumerator</span><span class="sxs-lookup"><span data-stu-id="dccef-717">Enumerator</span></span>|<span data-ttu-id="dccef-718">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dccef-718">Description</span></span>|
|:-----|:-----|
|<span data-ttu-id="dccef-719">LCSStatusFlag_None</span><span class="sxs-lookup"><span data-stu-id="dccef-719">LCSStatusFlag_None</span></span>  <br/> ||
|<span data-ttu-id="dccef-720">LSCStatusFlag_UploadPending</span><span class="sxs-lookup"><span data-stu-id="dccef-720">LSCStatusFlag_UploadPending</span></span>  <br/> |<span data-ttu-id="dccef-721">True, wenn es an die Server-Datei zu sendenden Daten steht.</span><span class="sxs-lookup"><span data-stu-id="dccef-721">True if there is pending data to send to the server file.</span></span>  <br/> |
|<span data-ttu-id="dccef-722">LSCStatusFlag_DownloadPending</span><span class="sxs-lookup"><span data-stu-id="dccef-722">LSCStatusFlag_DownloadPending</span></span>  <br/> |<span data-ttu-id="dccef-723">True, wenn es ausstehende Daten aus der Serverdatei herunterladen.</span><span class="sxs-lookup"><span data-stu-id="dccef-723">True if there is pending data to download from the server file.</span></span>  <br/> |
|<span data-ttu-id="dccef-724">LSCStatusFlag_LocalFileUnchanged</span><span class="sxs-lookup"><span data-stu-id="dccef-724">LSCStatusFlag_LocalFileUnchanged</span></span>  <br/> |<span data-ttu-id="dccef-725">True, wenn die Daten für die Datei im Cache befindet ist die aktuellste Kopie der Daten auf dem Datenträger.</span><span class="sxs-lookup"><span data-stu-id="dccef-725">True if the data Office has on the file in its cache is the most recent copy of the data on disk.</span></span>  <br/> |
   

