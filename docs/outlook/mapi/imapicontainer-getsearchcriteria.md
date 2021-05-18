---
title: IMAPIContainerGetSearchCriteria
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIContainer.GetSearchCriteria
api_type:
- COM
ms.assetid: 41b6c162-9984-43a3-b38e-44f0afae67de
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412023"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="80bb9-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="80bb9-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="80bb9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="80bb9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="80bb9-105">Ruft die Suchkriterien für den Container ab.</span><span class="sxs-lookup"><span data-stu-id="80bb9-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="80bb9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="80bb9-106">Parameters</span></span>

 <span data-ttu-id="80bb9-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="80bb9-107">_ulFlags_</span></span>
  
> <span data-ttu-id="80bb9-108">[in] Eine Bitmaske mit Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="80bb9-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="80bb9-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="80bb9-109">The following flag can be set:</span></span>
    
<span data-ttu-id="80bb9-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="80bb9-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="80bb9-111">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="80bb9-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="80bb9-112">Wenn das MAPI_UNICODE nicht festgelegt ist, befinden sich die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="80bb9-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="80bb9-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="80bb9-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="80bb9-114">[out] Ein Zeiger auf einen Zeiger auf eine [SRestriction-Struktur,](srestriction.md) die die Suchkriterien definiert.</span><span class="sxs-lookup"><span data-stu-id="80bb9-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="80bb9-115">Wenn eine Clientanwendung NULL im  _lppRestriction-Parameter_ übergibt, gibt **GetSearchCriteria** keine **SRestriction-Struktur** zurück.</span><span class="sxs-lookup"><span data-stu-id="80bb9-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="80bb9-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="80bb9-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="80bb9-117">[out] Ein Zeiger auf einen Zeiger auf ein Array von Eintragsbezeichnern, die Container darstellen, die in die Suche einbezogen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="80bb9-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="80bb9-118">Wenn ein Client NULL im  _lppContainerList-Parameter übergibt,_ gibt **GetSearchCriteria** kein Array von Eintragsbezeichnern zurück.</span><span class="sxs-lookup"><span data-stu-id="80bb9-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="80bb9-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="80bb9-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="80bb9-120">[out] Ein Zeiger auf eine Bitmaske mit Flags, die verwendet werden, um den aktuellen Status der Suche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="80bb9-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="80bb9-121">Wenn ein Client NULL im  _lpulSearchState-Parameter_ übergibt, gibt **GetSearchCriteria** keine Flags zurück.</span><span class="sxs-lookup"><span data-stu-id="80bb9-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="80bb9-122">Die folgenden Kennzeichen können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="80bb9-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="80bb9-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="80bb9-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="80bb9-124">Die Suche sollte mit hoher Priorität im Vergleich zu anderen Suchen ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="80bb9-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="80bb9-125">Wenn dieses Flag nicht festgelegt ist, wird die Suche mit normaler Priorität im Verhältnis zu anderen Suchen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="80bb9-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="80bb9-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="80bb9-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="80bb9-127">Die Suche befindet sich im CPU-intensiven Modus des Vorgangs und versucht, Nachrichten zu finden, die den Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="80bb9-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="80bb9-128">Wenn dieses Flag nicht festgelegt ist, ist der CPU-intensive Teil des Suchvorgangs beendet.</span><span class="sxs-lookup"><span data-stu-id="80bb9-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="80bb9-129">Dieses Flag hat nur eine Bedeutung, wenn die Suche aktiv ist (d. h. wenn SEARCH_RUNNING festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="80bb9-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="80bb9-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="80bb9-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="80bb9-131">Die Suche sucht in angegebenen Containern und allen untergeordneten Containern nach übereinstimmenden Einträgen.</span><span class="sxs-lookup"><span data-stu-id="80bb9-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="80bb9-132">Wenn dieses Flag nicht festgelegt ist, werden nur die Container durchsucht, die explizit im letzten Aufruf der [IMAPIContainer::SetSearchCriteria-Methode](imapicontainer-setsearchcriteria.md) enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="80bb9-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="80bb9-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="80bb9-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="80bb9-134">Die Suche ist aktiv, und die Inhaltstabelle des Containers wird aktualisiert, um Änderungen im Nachrichtenspeicher oder Adressbuch widerspiegeln zu können.</span><span class="sxs-lookup"><span data-stu-id="80bb9-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="80bb9-135">Wenn dieses Flag nicht festgelegt ist, ist die Suche inaktiv und die Inhaltstabelle statisch.</span><span class="sxs-lookup"><span data-stu-id="80bb9-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="80bb9-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="80bb9-136">Return value</span></span>

<span data-ttu-id="80bb9-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="80bb9-137">S_OK</span></span> 
  
> <span data-ttu-id="80bb9-138">Die Suchkriterien wurden erfolgreich ermittelt.</span><span class="sxs-lookup"><span data-stu-id="80bb9-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="80bb9-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="80bb9-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="80bb9-140">Entweder wurde MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="80bb9-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="80bb9-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="80bb9-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="80bb9-142">Suchkriterien wurden nie für den Container festgelegt.</span><span class="sxs-lookup"><span data-stu-id="80bb9-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="80bb9-143">Hinweise</span><span class="sxs-lookup"><span data-stu-id="80bb9-143">Remarks</span></span>

<span data-ttu-id="80bb9-144">Die **IMAPIContainer::GetSearchCriteria-Methode** ruft die Suchkriterien für einen Container ab, der Suchen unterstützt, in der Regel ein Suchergebnisordner.</span><span class="sxs-lookup"><span data-stu-id="80bb9-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="80bb9-145">Sie erstellen Suchkriterien, indem Sie die **IMAPIContainer::SetSearchCriteria-Methode** eines Containers aufrufen.</span><span class="sxs-lookup"><span data-stu-id="80bb9-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="80bb9-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="80bb9-146">Notes to implementers</span></span>

<span data-ttu-id="80bb9-147">Adressbuchcontainer müssen **GetSearchCriteria** möglicherweise nur unterstützen, wenn sie die erweiterten Suchfunktionen bereitstellen, die der **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) -Eigenschaft zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="80bb9-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="80bb9-148">Weitere Informationen zum Implementieren des erweiterten Suchfeatures für Adressbuchcontainer finden Sie unter [Implementing Advanced Searching](implementing-advanced-searching.md).</span><span class="sxs-lookup"><span data-stu-id="80bb9-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="80bb9-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="80bb9-149">Notes to callers</span></span>

<span data-ttu-id="80bb9-150">Wenn Sie mit den Datenstrukturen fertig sind, auf die die  _Parameter lppRestriction_ und  _lppContainerList_ zeigen, rufen Sie [MAPIFreeBuffer](mapifreebuffer.md) einmal auf, damit jede Struktur freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="80bb9-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="80bb9-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="80bb9-151">MFCMAPI reference</span></span>

<span data-ttu-id="80bb9-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="80bb9-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="80bb9-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="80bb9-153">**File**</span></span>|<span data-ttu-id="80bb9-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="80bb9-154">**Function**</span></span>|<span data-ttu-id="80bb9-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="80bb9-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="80bb9-156">HierarchyTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="80bb9-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="80bb9-157">CHierarchyTableDlg::OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="80bb9-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="80bb9-158">MFCMAPI verwendet die **IMAPIContainer::GetSearchCriteria-Methode,** um Suchkriterien aus einem angezeigten Ordner zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="80bb9-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="80bb9-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="80bb9-159">See also</span></span>



[<span data-ttu-id="80bb9-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="80bb9-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="80bb9-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="80bb9-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="80bb9-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="80bb9-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="80bb9-163">PidTagSearch (kanonische Eigenschaft)</span><span class="sxs-lookup"><span data-stu-id="80bb9-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="80bb9-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="80bb9-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="80bb9-165">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="80bb9-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

