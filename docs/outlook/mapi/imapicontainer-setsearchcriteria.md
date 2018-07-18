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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 93578300e2520dda4a9621b05ac6a79c54eca2ef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19792085"
---
# <a name="imapicontainersetsearchcriteria"></a><span data-ttu-id="51d0f-103">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="51d0f-103">IMAPIContainer::SetSearchCriteria</span></span>

  
  
<span data-ttu-id="51d0f-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="51d0f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="51d0f-105">Stellt die Suchkriterien für den Container her.</span><span class="sxs-lookup"><span data-stu-id="51d0f-105">Establishes search criteria for the container.</span></span>
  
```cpp
HRESULT SetSearchCriteria(
  LPSRestriction lpRestriction,
  LPENTRYLIST lpContainerList,
  ULONG ulSearchFlags
);
```

## <a name="parameters"></a><span data-ttu-id="51d0f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="51d0f-106">Parameters</span></span>

 <span data-ttu-id="51d0f-107">_lpRestriction_</span><span class="sxs-lookup"><span data-stu-id="51d0f-107">_lpRestriction_</span></span>
  
> <span data-ttu-id="51d0f-108">[in] Ein Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien definiert.</span><span class="sxs-lookup"><span data-stu-id="51d0f-108">[in] A pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="51d0f-109">Wenn NULL in der _LpRestriction_ -Parameter übergeben wird, werden die Suchkriterien, die für diesen Container zuletzt verwendet wurden erneut verwendet.</span><span class="sxs-lookup"><span data-stu-id="51d0f-109">If NULL is passed in the  _lpRestriction_ parameter, the search criteria that were used most recently for this container are used again.</span></span> <span data-ttu-id="51d0f-110">NULL darf nicht in _LpRestriction_ für die erste Suche in einem Container übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-110">NULL should not be passed in  _lpRestriction_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="51d0f-111">_lpContainerList_</span><span class="sxs-lookup"><span data-stu-id="51d0f-111">_lpContainerList_</span></span>
  
> <span data-ttu-id="51d0f-112">[in] Ein Zeiger auf ein Array von Eintragsbezeichner, die Container, in die Suche einbezogen werden darstellen.</span><span class="sxs-lookup"><span data-stu-id="51d0f-112">[in] A pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="51d0f-113">Wenn ein Client NULL im Parameter _LpContainerList_ übergibt, werden die zuletzt verwendet, um diesen Container suchen Eintragsbezeichner für die neue Suche verwendet.</span><span class="sxs-lookup"><span data-stu-id="51d0f-113">If a client passes NULL in the  _lpContainerList_ parameter, the entry identifiers used most recently to search this container are used for the new search.</span></span> <span data-ttu-id="51d0f-114">Ein Client sollte nicht NULL _LpContainerList_ für die erste Suche in einem Container übergeben.</span><span class="sxs-lookup"><span data-stu-id="51d0f-114">A client should not pass NULL in  _lpContainerList_ for the first search in a container.</span></span> 
    
 <span data-ttu-id="51d0f-115">_ulSearchFlags_</span><span class="sxs-lookup"><span data-stu-id="51d0f-115">_ulSearchFlags_</span></span>
  
> <span data-ttu-id="51d0f-116">[in] Eine Bitmaske aus Flags, die steuern, wie die Suche ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51d0f-116">[in] A bitmask of flags that control how the search is performed.</span></span> <span data-ttu-id="51d0f-117">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="51d0f-117">The following flags can be set:</span></span>
    
<span data-ttu-id="51d0f-118">BACKGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="51d0f-118">BACKGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="51d0f-119">Die Suche sollte mit normaler Priorität relativ zu anderen Suchvorgänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51d0f-119">The search should run at normal priority relative to other searches.</span></span> <span data-ttu-id="51d0f-120">Dieses Kennzeichen können nicht gleichzeitig als das Flag FOREGROUND_SEARCH festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-120">This flag cannot be set at the same time as the FOREGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="51d0f-121">FOREGROUND_SEARCH</span><span class="sxs-lookup"><span data-stu-id="51d0f-121">FOREGROUND_SEARCH</span></span> 
  
> <span data-ttu-id="51d0f-122">Die Suche sollte mit hoher Priorität relativ zu anderen Suchvorgänge ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="51d0f-122">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="51d0f-123">Dieses Kennzeichen können nicht gleichzeitig als das Flag BACKGROUND_SEARCH festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-123">This flag cannot be set at the same time as the BACKGROUND_SEARCH flag.</span></span>
    
<span data-ttu-id="51d0f-124">NON_CONTENT_INDEXED_SEARCH</span><span class="sxs-lookup"><span data-stu-id="51d0f-124">NON_CONTENT_INDEXED_SEARCH</span></span>
  
> <span data-ttu-id="51d0f-125">Die Suche sollte Inhaltsindex nicht übereinstimmenden Einträge suchen verwenden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-125">The search should not use content indexing to find matching entries.</span></span> <span data-ttu-id="51d0f-126">Dieses Kennzeichen gilt nur für Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="51d0f-126">This flag is only valid for Exchange stores.</span></span>
    
<span data-ttu-id="51d0f-127">RECURSIVE_SEARCH</span><span class="sxs-lookup"><span data-stu-id="51d0f-127">RECURSIVE_SEARCH</span></span> 
  
> <span data-ttu-id="51d0f-128">Die Suche sollte in der _LpContainerList_ -Parameter und alle untergeordneten Container angegebenen Container enthalten.</span><span class="sxs-lookup"><span data-stu-id="51d0f-128">The search should include the containers specified in the  _lpContainerList_ parameter and all their child containers.</span></span> <span data-ttu-id="51d0f-129">Dieses Kennzeichen können nicht gleichzeitig als das Flag SHALLOW_SEARCH festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-129">This flag cannot be set at the same time as the SHALLOW_SEARCH flag.</span></span> 
    
<span data-ttu-id="51d0f-130">RESTART_SEARCH</span><span class="sxs-lookup"><span data-stu-id="51d0f-130">RESTART_SEARCH</span></span> 
  
> <span data-ttu-id="51d0f-131">Die Suche sollte initiiert, wenn dies der erste Aufruf von **SetSearchCriteria**ist, oder neu gestartet, wenn die Suche nicht aktiv ist.</span><span class="sxs-lookup"><span data-stu-id="51d0f-131">The search should be initiated if this is the first call to **SetSearchCriteria**, or restarted if the search is inactive.</span></span> <span data-ttu-id="51d0f-132">Dieses Kennzeichen können nicht gleichzeitig als das Flag STOP_SEARCH festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-132">This flag cannot be set at the same time as the STOP_SEARCH flag.</span></span>
    
<span data-ttu-id="51d0f-133">SHALLOW_SEARCH</span><span class="sxs-lookup"><span data-stu-id="51d0f-133">SHALLOW_SEARCH</span></span> 
  
> <span data-ttu-id="51d0f-134">Die Suche sollte nur in den Containern im für übereinstimmende Einträge _LpContainerList_ -Parameter angegebene aussehen.</span><span class="sxs-lookup"><span data-stu-id="51d0f-134">The search should look only in the containers specified in the  _lpContainerList_ parameter for matching entries.</span></span> <span data-ttu-id="51d0f-135">Dieses Kennzeichen können nicht gleichzeitig als das Flag RECURSIVE_SEARCH festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-135">This flag cannot be set at the same time as the RECURSIVE_SEARCH flag.</span></span> 
    
<span data-ttu-id="51d0f-136">STOP_SEARCH</span><span class="sxs-lookup"><span data-stu-id="51d0f-136">STOP_SEARCH</span></span> 
  
> <span data-ttu-id="51d0f-137">Die Suche muss angehalten werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-137">The search should be stopped.</span></span> <span data-ttu-id="51d0f-138">Dieses Kennzeichen können nicht gleichzeitig als das Flag RESTART_SEARCH festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-138">This flag cannot be set at the same time as the RESTART_SEARCH flag.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="51d0f-139">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="51d0f-139">Return value</span></span>

<span data-ttu-id="51d0f-140">S_OK</span><span class="sxs-lookup"><span data-stu-id="51d0f-140">S_OK</span></span> 
  
> <span data-ttu-id="51d0f-141">Die Suchkriterien wurde erfolgreich festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51d0f-141">The search criteria was successfully set.</span></span>
    
<span data-ttu-id="51d0f-142">MAPI_E_TOO_COMPLEX</span><span class="sxs-lookup"><span data-stu-id="51d0f-142">MAPI_E_TOO_COMPLEX</span></span> 
  
> <span data-ttu-id="51d0f-143">Der Dienstanbieter unterstützt nicht die angegebenen Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="51d0f-143">The service provider does not support the specified search criteria.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="51d0f-144">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="51d0f-144">Remarks</span></span>

<span data-ttu-id="51d0f-145">Die **IMAPIContainer::SetSearchCriteria** -Methode richtet Suchkriterien für einen Container, der sucht, in der Regel in einem Suchergebnisse Ordner unterstützt.</span><span class="sxs-lookup"><span data-stu-id="51d0f-145">The **IMAPIContainer::SetSearchCriteria** method establishes search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="51d0f-146">Suchergebnisse Ordner enthält Links zu Nachrichten, die den Suchkriterien entsprechen; die Nachrichten werden weiterhin an ihrem ursprünglichen Speicherort gespeichert.</span><span class="sxs-lookup"><span data-stu-id="51d0f-146">A search-results folder contains links to the messages that meet the search criteria; the actual messages are still stored in their original locations.</span></span> <span data-ttu-id="51d0f-147">Nur eindeutigen in einem Suchergebnisse Ordner enthaltenen Daten ist die Inhaltstabelle.</span><span class="sxs-lookup"><span data-stu-id="51d0f-147">The only unique data that is contained in a search-results folder is its contents table.</span></span> <span data-ttu-id="51d0f-148">Die Inhaltstabelle eines Ordners Suchergebnisse hat den zusammengeführten Inhalt des Nachrichtenspeichers, nachdem die Suche Einschränkung angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="51d0f-148">The contents table of a search-results folder has the merged contents of the message store after the search restriction has been applied.</span></span> 
  
<span data-ttu-id="51d0f-149">Suchvorgang funktioniert nur für diese Tabelle zusammengeführten Inhalt. Es wird nicht durch andere Suchergebnisse Ordner gesucht.</span><span class="sxs-lookup"><span data-stu-id="51d0f-149">A search operation works only on this merged contents table; it does not search through other search-results folders.</span></span> <span data-ttu-id="51d0f-150">Die Suchergebnisse zurück, nur die Nachrichten, die den Suchkriterien entsprechen. Die Ordnerhierarchie wird nicht zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="51d0f-150">The search results return only the messages that match the search criteria; the folder hierarchy is not returned.</span></span>
  
<span data-ttu-id="51d0f-151">Steuerelement wird an den Client zurückgegeben, wenn die Suche abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="51d0f-151">Control is returned to the client when the search has finished.</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="51d0f-152">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="51d0f-152">Notes to implementers</span></span>

<span data-ttu-id="51d0f-153">Address Book Containern erstellen Suchkriterien Einschränkungen auf ihren Inhalt Tabellen anwenden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-153">Address book containers establish search criteria by applying restrictions to their contents tables.</span></span> <span data-ttu-id="51d0f-154">Weitere Informationen zu Suchkriterien und address Book Containern, finden Sie unter [Implementieren erweiterte Suche](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="51d0f-154">For more information about search criteria and address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
<span data-ttu-id="51d0f-155">Sie sollten unterstützen öffnen, kopieren, verschieben und delete-Vorgänge auf die Nachrichten in Suchergebnissen Ordnern, nicht auf den Suchergebnisse Ordner selbst.</span><span class="sxs-lookup"><span data-stu-id="51d0f-155">You should support open, copy, move, and delete operations on the messages within search-results folders, not on the search-results folder itself.</span></span> <span data-ttu-id="51d0f-156">Lassen Sie nicht Nachrichten innerhalb erstellt oder in einem Suchergebnisse Ordner kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="51d0f-156">Do not allow messages to be created within or copied into a search-results folder.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="51d0f-157">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="51d0f-157">Notes to callers</span></span>

<span data-ttu-id="51d0f-158">Legen Sie zum Suchen der Empfänger der Nachricht _LpRestriction_ So zeigen Sie auf eine Einschränkung Unterobjekts mit dem **UlSubObject** -Element in der [SSubRestriction](ssubrestriction.md) -Struktur auf **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="51d0f-158">To search for message recipients, set  _lpRestriction_ to point to a subobject restriction with the **ulSubObject** member in the [SSubRestriction](ssubrestriction.md) structure set to **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)).</span></span> <span data-ttu-id="51d0f-159">Legen Sie zum Suchen nach Anlagen des **UlSubObject** Members auf **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="51d0f-159">To search for attachments, set the **ulSubObject** member to **PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)).</span></span> <span data-ttu-id="51d0f-160">Legen Sie den **LpRes** Member So zeigen Sie auf eine eigenschaftseinschränkung, die die Suchkriterien für die Empfänger oder Anlagen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="51d0f-160">Set the **lpRes** member to point to a property restriction that describes the search criteria for the recipients or attachments.</span></span> 
  
<span data-ttu-id="51d0f-161">Um für Dateianlagen zu suchen, die die Erweiterung .mss haben, legen Sie beispielsweise **UlSubObject** auf **PR_MESSAGE_ATTACHMENTS** und **LpRes** , die eine eigenschaftseinschränkung, die mit **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md) übereinstimmt ) mit. mss.</span><span class="sxs-lookup"><span data-stu-id="51d0f-161">For example, to look for file attachments that have the extension .mss, set **ulSubObject** to **PR_MESSAGE_ATTACHMENTS** and **lpRes** to a property restriction that matches **PR_ATTACH_EXTENSION** ([PidTagAttachExtension](pidtagattachextension-canonical-property.md)) with .mss.</span></span>
  
<span data-ttu-id="51d0f-162">Festlegen des Flags FOREGROUND_SEARCH in der _UlSearchFlags_ -Parameter kann eine Beeinträchtigung der Systemleistung führen.</span><span class="sxs-lookup"><span data-stu-id="51d0f-162">Setting the FOREGROUND_SEARCH flag in the  _ulSearchFlags_ parameter could cause a decrease in system performance.</span></span> 
  
<span data-ttu-id="51d0f-163">**SetSearchCriteria** können Sie die Suchkriterien bereits in Bearbeitung einer Suche ändern.</span><span class="sxs-lookup"><span data-stu-id="51d0f-163">You can use **SetSearchCriteria** to change the search criteria of a search already in progress.</span></span> <span data-ttu-id="51d0f-164">Sie können neue Einschränkungen, neue Listen der Ordner für die Suche und eine neue Suche Priorität wie aktualisieren eine Suche auf eine höhere Priorität angeben.</span><span class="sxs-lookup"><span data-stu-id="51d0f-164">You can specify new restrictions, new lists of folders to search, and a new search priority, such as upgrading a search to a higher priority.</span></span> <span data-ttu-id="51d0f-165">Änderungen in Search Priorität bewirken keine vorhandene Suche neu starten, jedoch können weitere Änderungen an den Suchkriterien.</span><span class="sxs-lookup"><span data-stu-id="51d0f-165">Changes in search priority do not cause an existing search to restart, but other changes to search criteria can.</span></span> 
  
<span data-ttu-id="51d0f-166">Wenn Sie über die Verwendung eines Ordners-Ergebnisse sind, können Sie den Ordner löschen oder lassen Sie ihn zur späteren Verwendung geöffnet bleiben.</span><span class="sxs-lookup"><span data-stu-id="51d0f-166">When you are through using a search-results folder, you can either delete the folder or let it remain open for later use.</span></span> <span data-ttu-id="51d0f-167">Wenn Sie den Suchergebnisse Ordner löschen, werden nur Nachricht Links gelöscht.</span><span class="sxs-lookup"><span data-stu-id="51d0f-167">If you do delete the search-results folder, only message links are deleted.</span></span> <span data-ttu-id="51d0f-168">Die tatsächlichen Nachrichten verbleiben in die übergeordneten Ordner.</span><span class="sxs-lookup"><span data-stu-id="51d0f-168">The actual messages remain in their parent folders.</span></span> 
  
<span data-ttu-id="51d0f-169">Weitere Informationen zu Suchergebnissen Ordnern finden Sie unter [Suchordner MAPI](mapi-search-folders.md).</span><span class="sxs-lookup"><span data-stu-id="51d0f-169">For more information about search-results folders, see [MAPI Search Folders](mapi-search-folders.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="51d0f-170">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="51d0f-170">MFCMAPI reference</span></span>

<span data-ttu-id="51d0f-171">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="51d0f-171">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="51d0f-172">**Datei**</span><span class="sxs-lookup"><span data-stu-id="51d0f-172">**File**</span></span>|<span data-ttu-id="51d0f-173">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="51d0f-173">**Function**</span></span>|<span data-ttu-id="51d0f-174">**Comment**</span><span class="sxs-lookup"><span data-stu-id="51d0f-174">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="51d0f-175">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="51d0f-175">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="51d0f-176">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="51d0f-176">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="51d0f-177">MFCMAPI (engl.) verwendet die **IMAPIContainer::SetSearchCriteria** -Methode zum Schreiben von Suchkriterien für einen Ordner, nachdem ein Benutzer es bearbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="51d0f-177">MFCMAPI uses the **IMAPIContainer::SetSearchCriteria** method to write search criteria for a folder after a user has edited it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="51d0f-178">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="51d0f-178">See also</span></span>



[<span data-ttu-id="51d0f-179">IMAPIContainer::GetContentsTable</span><span class="sxs-lookup"><span data-stu-id="51d0f-179">IMAPIContainer::GetContentsTable</span></span>](imapicontainer-getcontentstable.md)
  
[<span data-ttu-id="51d0f-180">IMAPIContainer::OpenEntry</span><span class="sxs-lookup"><span data-stu-id="51d0f-180">IMAPIContainer::OpenEntry</span></span>](imapicontainer-openentry.md)
  
[<span data-ttu-id="51d0f-181">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="51d0f-181">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="51d0f-182">IMAPIFolder : IMAPIContainer</span><span class="sxs-lookup"><span data-stu-id="51d0f-182">IMAPIFolder : IMAPIContainer</span></span>](imapifolderimapicontainer.md)
  
[<span data-ttu-id="51d0f-183">SPropertyRestriction</span><span class="sxs-lookup"><span data-stu-id="51d0f-183">SPropertyRestriction</span></span>](spropertyrestriction.md)
  
[<span data-ttu-id="51d0f-184">SRestriction</span><span class="sxs-lookup"><span data-stu-id="51d0f-184">SRestriction</span></span>](srestriction.md)
  
[<span data-ttu-id="51d0f-185">SSubRestriction</span><span class="sxs-lookup"><span data-stu-id="51d0f-185">SSubRestriction</span></span>](ssubrestriction.md)
  
[<span data-ttu-id="51d0f-186">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="51d0f-186">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="51d0f-187">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="51d0f-187">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

