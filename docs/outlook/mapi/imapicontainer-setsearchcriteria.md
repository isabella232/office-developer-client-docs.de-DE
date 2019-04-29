---
title: IMAPIContainerSetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.SetSearchCriteria
api_type:
- COM
ms.assetid: b5eb1841-e450-4024-aeaa-3b5a492ddb99
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: a6168e8fced2fff3a7f9d273e47ed2410ac4c010
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427199"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="70ce3-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="70ce3-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="70ce3-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70ce3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70ce3-105">Legt Suchkriterien für den Container fest.</span><span class="sxs-lookup"><span data-stu-id="70ce3-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="70ce3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="70ce3-106">Parameters</span></span>

 <span data-ttu-id="70ce3-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="70ce3-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="70ce3-108">in Ein Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien definiert.</span><span class="sxs-lookup"><span data-stu-id="70ce3-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="70ce3-109">Wenn NULL im _lpRestriction_ -Parameter übergeben wird, werden die Suchkriterien, die zuletzt für diesen Container verwendet wurden, erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="70ce3-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="70ce3-110">NULL sollte in _lpRestriction_ nicht für die erste Suche in einem Container übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="70ce3-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="70ce3-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="70ce3-112">in Ein Zeiger auf ein Array von Eintrags Bezeichnern, die Container darstellen, die in die Suche eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="70ce3-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="70ce3-113">Wenn ein Client im _lpContainerList_ -Parameter den Wert NULL übergibt, werden die in letzter Zeit verwendeten Eintrags-IDs für die neue Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="70ce3-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="70ce3-114">Ein Client sollte NULL in _lpContainerList_ für die erste Suche in einem Container nicht weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="70ce3-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="70ce3-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="70ce3-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="70ce3-116">in Eine Bitmaske von Flags, die Steuern, wie die Suche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="70ce3-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="70ce3-117">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="70ce3-117">The following flags can be set:</span></span>
    
<span data-ttu-id="70ce3-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="70ce3-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="70ce3-119">Die Suche sollte im Verhältnis zu anderen Suchvorgängen mit normaler Priorität ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="70ce3-120">Dieses Flag kann nicht gleichzeitig mit dem FOREGROUND_SEARCH-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="70ce3-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="70ce3-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="70ce3-122">Die Suche sollte relativ zu anderen Suchvorgängen mit hoher Priorität ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="70ce3-123">Dieses Flag kann nicht gleichzeitig mit dem BACKGROUND_SEARCH-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="70ce3-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="70ce3-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="70ce3-125">Die Suche sollte nicht die Inhaltsindizierung verwenden, um übereinstimmende Einträge zu finden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="70ce3-126">Dieses Flag gilt nur für Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="70ce3-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="70ce3-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="70ce3-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="70ce3-128">Die Suche muss die im Parameter _lpContainerList_ und alle untergeordneten Container angegebenen Container aufweisen.</span><span class="sxs-lookup"><span data-stu-id="70ce3-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="70ce3-129">Dieses Flag kann nicht gleichzeitig mit dem SHALLOW_SEARCH-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="70ce3-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="70ce3-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="70ce3-131">Die Suche sollte initiiert werden, wenn dies der erste Aufruf von **SetSearchCriteria**ist, oder neu gestartet, wenn die Suche inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="70ce3-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="70ce3-132">Dieses Flag kann nicht gleichzeitig mit dem STOP_SEARCH-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="70ce3-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="70ce3-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="70ce3-134">Die Suche sollte nur in den im _lpContainerList_ -Parameter angegebenen Containern für übereinstimmende Einträge aussehen.</span><span class="sxs-lookup"><span data-stu-id="70ce3-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="70ce3-135">Dieses Flag kann nicht gleichzeitig mit dem RECURSIVE_SEARCH-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="70ce3-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="70ce3-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="70ce3-137">Die Suche sollte beendet werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-137">The search should be stopped.</span></span> <span data-ttu-id="70ce3-138">Dieses Flag kann nicht gleichzeitig mit dem RESTART_SEARCH-Flag festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="70ce3-139">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70ce3-139">Return value</span></span>

<span data-ttu-id="70ce3-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="70ce3-140">S_OK</span></span> 
  
> <span data-ttu-id="70ce3-141">Die Suchkriterien wurden erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="70ce3-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="70ce3-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="70ce3-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="70ce3-143">Der Dienstanbieter unterstützt die angegebenen Suchkriterien nicht.</span><span class="sxs-lookup"><span data-stu-id="70ce3-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70ce3-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70ce3-144">Remarks</span></span>

<span data-ttu-id="70ce3-145">Mit der **IMAPIContainer:: SetSearchCriteria** -Methode werden Suchkriterien für einen Container festgelegt, der Suchvorgänge unterstützt, in der Regel ein Suchergebnisordner.</span><span class="sxs-lookup"><span data-stu-id="70ce3-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="70ce3-146">Ein Suchergebnisordner enthält Links zu den Nachrichten, die den Suchkriterien entsprechen. die tatsächlichen Nachrichten werden weiterhin an ihren ursprünglichen Speicherorten gespeichert.</span><span class="sxs-lookup"><span data-stu-id="70ce3-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="70ce3-147">Die einzigen eindeutigen Daten, die in einem Ordner mit Suchergebnissen enthalten sind, sind die Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="70ce3-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="70ce3-148">Die Inhaltstabelle eines Suchergebnis Ordners enthält die zusammengeführten Inhalte des Nachrichtenspeichers, nachdem die sucheinschränkung angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="70ce3-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="70ce3-149">Ein Suchvorgang funktioniert nur in dieser zusammengeführten Inhaltstabelle; andere Suchergebnisordner werden nicht durchsucht.</span><span class="sxs-lookup"><span data-stu-id="70ce3-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="70ce3-150">In den Suchergebnissen werden nur die Nachrichten zurückgegeben, die den Suchkriterien entsprechen. die Ordnerhierarchie wird nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="70ce3-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="70ce3-151">Die Steuerung wird an den Client zurückgegeben, wenn die Suche abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="70ce3-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="70ce3-152">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="70ce3-152">Notes to implementers</span></span>

<span data-ttu-id="70ce3-153">Adressbuchcontainer legen Suchkriterien fest, indem Sie Einschränkungen auf Ihre Inhaltstabellen anwenden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="70ce3-154">Weitere Informationen zu Suchkriterien und Adressbuch Containern finden Sie unter [Implementieren der erweiterten Suche](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="70ce3-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="70ce3-155">Sie sollten öffnen-, Kopier-, Verschiebungs-und Löschvorgänge für die Nachrichten in Suchergebnis Ordnern unterstützen, nicht im Ordner "Suchergebnisse" selbst.</span><span class="sxs-lookup"><span data-stu-id="70ce3-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="70ce3-156">Lassen Sie keine Nachrichten innerhalb oder in einen Suchergebnisordner kopieren.</span><span class="sxs-lookup"><span data-stu-id="70ce3-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="70ce3-157">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="70ce3-157">Notes to callers</span></span>

<span data-ttu-id="70ce3-158">Zum Suchen nach Nachrichtenempfängern legen Sie fest, dass _lpRestriction_ auf eine SubObject-Einschränkung zeigt, wobei das **ulSubObject** -Element in der [SSubRestriction](ssubrestriction.md) -Struktur auf **PR_MESSAGE_RECIPIENTS** ([pidtagmessagerecipients (](pidtagmessagerecipients-canonical-property.md)) festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="70ce3-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="70ce3-159">Legen Sie das **ulSubObject** -Element auf **PR_MESSAGE_ATTACHMENTS** ([pidtagmessageattachments (](pidtagmessageattachments-canonical-property.md)) fest, um nach Anlagen zu suchen.</span><span class="sxs-lookup"><span data-stu-id="70ce3-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="70ce3-160">Legen Sie fest, dass das **lpRes** -Element auf eine Eigenschaftseinschränkung zeigt, die die Suchkriterien für die Empfänger oder Anlagen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="70ce3-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="70ce3-161">Um beispielsweise nach Dateianlagen mit der Erweiterung. MSS zu suchen, legen Sie **ulSubObject** auf **PR_MESSAGE_ATTACHMENTS** und **lpRes** auf eine Eigenschaftseinschränkung fest, die mit **PR_ATTACH_EXTENSION** übereinstimmt ([pidtagattachextension (](pidtagattachextension-canonical-property.md) ) mit. MSS.</span><span class="sxs-lookup"><span data-stu-id="70ce3-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="70ce3-162">Das Festlegen des FOREGROUND_SEARCH-Flags im _ulSearchFlags_ -Parameter kann zu einer Verringerung der Systemleistung führen.</span><span class="sxs-lookup"><span data-stu-id="70ce3-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="70ce3-163">Sie können **SetSearchCriteria** verwenden, um die Suchkriterien einer bereits ausgeführten Suche zu ändern.</span><span class="sxs-lookup"><span data-stu-id="70ce3-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="70ce3-164">Sie können neue Einschränkungen, neue Ordnerlisten für die Suche und eine neue Suchpriorität angeben, wie beispielsweise das Upgrade einer Suche auf eine höhere Priorität.</span><span class="sxs-lookup"><span data-stu-id="70ce3-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="70ce3-165">Änderungen der Suchpriorität führen nicht zu einem Neustart einer vorhandenen Suche, andere Änderungen an den Suchkriterien können jedoch vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="70ce3-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="70ce3-166">Wenn Sie einen Suchergebnisordner verwenden, können Sie entweder den Ordner löschen oder ihn zur späteren Verwendung geöffnet lassen.</span><span class="sxs-lookup"><span data-stu-id="70ce3-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="70ce3-167">Wenn Sie den Ordner Suchergebnisse löschen, werden nur die Nachrichten Links gelöscht.</span><span class="sxs-lookup"><span data-stu-id="70ce3-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="70ce3-168">Die tatsächlichen Nachrichten verbleiben in ihren übergeordneten Ordnern.</span><span class="sxs-lookup"><span data-stu-id="70ce3-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="70ce3-169">Weitere Informationen zu Suchergebnis Ordnern finden Sie unter [MAPI Search Folders](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="70ce3-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="70ce3-170">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="70ce3-170">MFCMAPI reference</span></span>

<span data-ttu-id="70ce3-171">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="70ce3-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="70ce3-172">**Datei**</span><span class="sxs-lookup"><span data-stu-id="70ce3-172">**File**</span></span>|<span data-ttu-id="70ce3-173">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="70ce3-173">**Function**</span></span>|<span data-ttu-id="70ce3-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="70ce3-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="70ce3-175">HierarchyTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="70ce3-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="70ce3-176">CHierarchyTableDlg:: OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="70ce3-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="70ce3-177">MFCMAPI verwendet die **IMAPIContainer:: SetSearchCriteria** -Methode, um Suchkriterien für einen Ordner zu schreiben, nachdem Sie von einem Benutzer bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="70ce3-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="70ce3-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70ce3-178">See also</span></span>



[<span data-ttu-id="70ce3-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="70ce3-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="70ce3-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="70ce3-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="70ce3-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="70ce3-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="70ce3-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="70ce3-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="70ce3-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="70ce3-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="70ce3-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="70ce3-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="70ce3-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="70ce3-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="70ce3-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="70ce3-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="70ce3-187">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="70ce3-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

