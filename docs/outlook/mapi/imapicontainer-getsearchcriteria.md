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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 7845238722ce81b84210b6f4fc33f9df0abacc07
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349294"
---
# <a name="imapicontainergetsearchcriteria"></a><span data-ttu-id="4d25d-103">IMAPIContainer::GetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="4d25d-103">IMAPIContainer::GetSearchCriteria</span></span>

  
  
<span data-ttu-id="4d25d-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4d25d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4d25d-105">Ruft die Suchkriterien für den Container ab.</span><span class="sxs-lookup"><span data-stu-id="4d25d-105">Obtains the search criteria for the container.</span></span>
  
```cpp
HRESULT GetSearchCriteria(
  ULONG ulFlags,
  LPSRestriction FAR * lppRestriction,
  LPENTRYLIST FAR * lppContainerList,
  ULONG FAR * lpulSearchState
);
```

## <a name="parameters"></a><span data-ttu-id="4d25d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4d25d-106">Parameters</span></span>

 <span data-ttu-id="4d25d-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="4d25d-107">_ulFlags_</span></span>
  
> <span data-ttu-id="4d25d-108">in Eine Bitmaske von Flags, die den Typ der übergebenen Zeichenfolgen steuert.</span><span class="sxs-lookup"><span data-stu-id="4d25d-108">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="4d25d-109">Das folgende Flag kann festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4d25d-109">The following flag can be set:</span></span>
    
<span data-ttu-id="4d25d-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4d25d-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="4d25d-111">Die übergebenen Zeichenfolgen sind im Unicode-Format.</span><span class="sxs-lookup"><span data-stu-id="4d25d-111">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="4d25d-112">Wenn das MAPI_UNICODE-Flag nicht festgelegt ist, werden die Zeichenfolgen im ANSI-Format.</span><span class="sxs-lookup"><span data-stu-id="4d25d-112">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="4d25d-113">_lppRestriction_</span><span class="sxs-lookup"><span data-stu-id="4d25d-113">_lppRestriction_</span></span>
  
> <span data-ttu-id="4d25d-114">Out Ein Zeiger auf einen Zeiger auf eine [SRestriction](srestriction.md) -Struktur, die die Suchkriterien definiert.</span><span class="sxs-lookup"><span data-stu-id="4d25d-114">[out] A pointer to a pointer to an [SRestriction](srestriction.md) structure that defines the search criteria.</span></span> <span data-ttu-id="4d25d-115">Wenn eine Clientanwendung im _lppRestriction_ -Parameter den Wert NULL übergibt, gibt **GetSearchCriteria** keine **SRestriction** -Struktur zurück.</span><span class="sxs-lookup"><span data-stu-id="4d25d-115">If a client application passes NULL in the  _lppRestriction_ parameter, **GetSearchCriteria** does not return an **SRestriction** structure.</span></span> 
    
 <span data-ttu-id="4d25d-116">_lppContainerList_</span><span class="sxs-lookup"><span data-stu-id="4d25d-116">_lppContainerList_</span></span>
  
> <span data-ttu-id="4d25d-117">Out Ein Zeiger auf einen Zeiger auf ein Array von Eintrags Bezeichnern, die Container darstellen, die in die Suche eingeschlossen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4d25d-117">[out] A pointer to a pointer to an array of entry identifiers that represent containers to be included in the search.</span></span> <span data-ttu-id="4d25d-118">Wenn ein Client im _lppContainerList_ -Parameter den Wert NULL übergibt, gibt **GetSearchCriteria** kein Array von Eintrags Bezeichnern zurück.</span><span class="sxs-lookup"><span data-stu-id="4d25d-118">If a client passes NULL in the  _lppContainerList_ parameter, **GetSearchCriteria** does not return an array of entry identifiers.</span></span> 
    
 <span data-ttu-id="4d25d-119">_lpulSearchState_</span><span class="sxs-lookup"><span data-stu-id="4d25d-119">_lpulSearchState_</span></span>
  
> <span data-ttu-id="4d25d-120">Out Ein Zeiger auf eine Bitmaske von Flags, die verwendet werden, um den aktuellen Status der Suche anzugeben.</span><span class="sxs-lookup"><span data-stu-id="4d25d-120">[out] A pointer to a bitmask of flags used to indicate the current state of the search.</span></span> <span data-ttu-id="4d25d-121">Wenn ein Client im _lpulSearchState_ -Parameter den Wert NULL übergibt, gibt **GetSearchCriteria** keine Flags zurück.</span><span class="sxs-lookup"><span data-stu-id="4d25d-121">If a client passes NULL in the  _lpulSearchState_ parameter, **GetSearchCriteria** returns no flags.</span></span> <span data-ttu-id="4d25d-122">Die folgenden Flags können festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="4d25d-122">The following flags can be set:</span></span> 
    
<span data-ttu-id="4d25d-123">SEARCH_FOREGROUND</span><span class="sxs-lookup"><span data-stu-id="4d25d-123">SEARCH_FOREGROUND</span></span> 
  
> <span data-ttu-id="4d25d-124">Die Suche sollte relativ zu anderen Suchvorgängen mit hoher Priorität ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="4d25d-124">The search should run at high priority relative to other searches.</span></span> <span data-ttu-id="4d25d-125">Wenn dieses Flag nicht festgelegt ist, wird die Suche im Verhältnis zu anderen Suchvorgängen mit normaler Priorität ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="4d25d-125">If this flag is not set, the search runs at normal priority relative to other searches.</span></span>
    
<span data-ttu-id="4d25d-126">SEARCH_REBUILD</span><span class="sxs-lookup"><span data-stu-id="4d25d-126">SEARCH_REBUILD</span></span> 
  
> <span data-ttu-id="4d25d-127">Die Suche befindet sich im CPU-intensiven Modus des Vorgangs und versucht, Nachrichten zu finden, die den Kriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="4d25d-127">The search is in the CPU-intensive mode of its operation, trying to locate messages that match the criteria.</span></span> <span data-ttu-id="4d25d-128">Wenn dieses Flag nicht festgelegt ist, ist der CPU-intensive Teil des Suchvorgangs über.</span><span class="sxs-lookup"><span data-stu-id="4d25d-128">If this flag is not set, the CPU-intensive part of the search's operation is over.</span></span> <span data-ttu-id="4d25d-129">Dieses Flag hat nur dann eine Bedeutung, wenn die Suche aktiv ist (d. h., wenn das SEARCH_RUNNING-Flag festgelegt ist).</span><span class="sxs-lookup"><span data-stu-id="4d25d-129">This flag has meaning only if the search is active (that is, if the SEARCH_RUNNING flag is set).</span></span>
    
<span data-ttu-id="4d25d-130">SEARCH_RECURSIVE</span><span class="sxs-lookup"><span data-stu-id="4d25d-130">SEARCH_RECURSIVE</span></span> 
  
> <span data-ttu-id="4d25d-131">Die Suche sucht in den angegebenen Containern und allen untergeordneten Containern nach übereinstimmenden Einträgen.</span><span class="sxs-lookup"><span data-stu-id="4d25d-131">The search is looking in specified containers and all their child containers for matching entries.</span></span> <span data-ttu-id="4d25d-132">Wenn dieses Flag nicht festgelegt ist, werden nur die Container durchsucht, die explizit im letzten Aufruf der [IMAPIContainer:: SetSearchCriteria](imapicontainer-setsearchcriteria.md) -Methode enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="4d25d-132">If this flag is not set, only the containers explicitly included in the last call to the [IMAPIContainer::SetSearchCriteria](imapicontainer-setsearchcriteria.md) method are being searched.</span></span> 
    
<span data-ttu-id="4d25d-133">SEARCH_RUNNING</span><span class="sxs-lookup"><span data-stu-id="4d25d-133">SEARCH_RUNNING</span></span> 
  
> <span data-ttu-id="4d25d-134">Die Suche ist aktiv, und die Inhaltstabelle des Containers wird aktualisiert, um Änderungen im Nachrichtenspeicher oder im Adressbuch widerzuspiegeln.</span><span class="sxs-lookup"><span data-stu-id="4d25d-134">The search is active and the container's contents table is being updated to reflect changes in the message store or address book.</span></span> <span data-ttu-id="4d25d-135">Wenn dieses Flag nicht festgelegt ist, ist die Suche inaktiv und die Tabelle Contents ist statisch.</span><span class="sxs-lookup"><span data-stu-id="4d25d-135">If this flag is not set, the search is inactive and the contents table is static.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="4d25d-136">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4d25d-136">Return value</span></span>

<span data-ttu-id="4d25d-137">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d25d-137">S_OK</span></span> 
  
> <span data-ttu-id="4d25d-138">Die Suchkriterien wurden erfolgreich abgerufen.</span><span class="sxs-lookup"><span data-stu-id="4d25d-138">The search criteria was successfully obtained.</span></span>
    
<span data-ttu-id="4d25d-139">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="4d25d-139">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="4d25d-140">Entweder wurde das MAPI_UNICODE-Flag festgelegt, und die Implementierung unterstützt Unicode nicht, oder MAPI_UNICODE wurde nicht festgelegt, und die Implementierung unterstützt nur Unicode.</span><span class="sxs-lookup"><span data-stu-id="4d25d-140">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="4d25d-141">MAPI_E_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="4d25d-141">MAPI_E_NOT_INITIALIZED</span></span> 
  
> <span data-ttu-id="4d25d-142">Suchkriterien wurden nie für den Container festgelegt.</span><span class="sxs-lookup"><span data-stu-id="4d25d-142">Search criteria were never established for the container.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4d25d-143">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d25d-143">Remarks</span></span>

<span data-ttu-id="4d25d-144">Die **IMAPIContainer:: GetSearchCriteria** -Methode ruft die Suchkriterien für einen Container ab, der Suchvorgänge unterstützt, in der Regel einen Suchergebnisordner.</span><span class="sxs-lookup"><span data-stu-id="4d25d-144">The **IMAPIContainer::GetSearchCriteria** method obtains the search criteria for a container that supports searches, typically a search-results folder.</span></span> <span data-ttu-id="4d25d-145">Sie erstellen Suchkriterien, indem Sie die **IMAPIContainer:: SetSearchCriteria** -Methode eines Containers aufrufen.</span><span class="sxs-lookup"><span data-stu-id="4d25d-145">You create search criteria by calling a container's **IMAPIContainer::SetSearchCriteria** method.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4d25d-146">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="4d25d-146">Notes to implementers</span></span>

<span data-ttu-id="4d25d-147">Adressbuchcontainer müssen **GetSearchCriteria** möglicherweise nur unterstützen, wenn Sie die erweiterten Suchfunktionen zur Verfügung stellen, die der **PR_SEARCH** ([pidtagsearch (](pidtagsearch-canonical-property.md))-Eigenschaft zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="4d25d-147">Address book containers may need to support **GetSearchCriteria** only if they provide the advanced search capabilities associated with the **PR_SEARCH** ([PidTagSearch](pidtagsearch-canonical-property.md)) property.</span></span> <span data-ttu-id="4d25d-148">Weitere Informationen dazu, wie Sie die erweiterte Suchfunktion für Adressbuchcontainer implementieren, finden Sie unter [Implementieren der erweiterten](implementing-advanced-searching.md)Suche.</span><span class="sxs-lookup"><span data-stu-id="4d25d-148">For more information about how to implement the advanced search feature for address book containers, see [Implementing Advanced Searching](implementing-advanced-searching.md).</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4d25d-149">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="4d25d-149">Notes to callers</span></span>

<span data-ttu-id="4d25d-150">Wenn Sie die Datenstrukturen, auf die durch die Parameter _lppRestriction_ und _lppContainerList_ verwiesen wird, nicht mehr aufgerufen haben, rufen Sie [mapifreebufferfreigegeben](mapifreebuffer.md) einmal für jede Struktur auf, die freigegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="4d25d-150">When you are finished with the data structures pointed to by the  _lppRestriction_ and  _lppContainerList_ parameters, call [MAPIFreeBuffer](mapifreebuffer.md) once for each structure to be released.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="4d25d-151">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="4d25d-151">MFCMAPI reference</span></span>

<span data-ttu-id="4d25d-152">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4d25d-152">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="4d25d-153">**Datei**</span><span class="sxs-lookup"><span data-stu-id="4d25d-153">**File**</span></span>|<span data-ttu-id="4d25d-154">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="4d25d-154">**Function**</span></span>|<span data-ttu-id="4d25d-155">**Comment**</span><span class="sxs-lookup"><span data-stu-id="4d25d-155">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="4d25d-156">HierarchyTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="4d25d-156">HierarchyTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="4d25d-157">CHierarchyTableDlg:: OnEditSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="4d25d-157">CHierarchyTableDlg::OnEditSearchCriteria</span></span>  <br/> |<span data-ttu-id="4d25d-158">MFCMAPI verwendet die **IMAPIContainer:: GetSearchCriteria** -Methode, um Suchkriterien aus einem anzuzeigenden Ordner abzurufen.</span><span class="sxs-lookup"><span data-stu-id="4d25d-158">MFCMAPI uses the **IMAPIContainer::GetSearchCriteria** method to obtain search criteria from a folder to display.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4d25d-159">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d25d-159">See also</span></span>



[<span data-ttu-id="4d25d-160">IMAPIContainer::SetSearchCriteria</span><span class="sxs-lookup"><span data-stu-id="4d25d-160">IMAPIContainer::SetSearchCriteria</span></span>](imapicontainer-setsearchcriteria.md)
  
[<span data-ttu-id="4d25d-161">IMAPIFolder::CreateFolder</span><span class="sxs-lookup"><span data-stu-id="4d25d-161">IMAPIFolder::CreateFolder</span></span>](imapifolder-createfolder.md)
  
[<span data-ttu-id="4d25d-162">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4d25d-162">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4d25d-163">Kanonische Pidtagsearch (-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="4d25d-163">PidTagSearch Canonical Property</span></span>](pidtagsearch-canonical-property.md)
  
[<span data-ttu-id="4d25d-164">IMAPIContainer : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="4d25d-164">IMAPIContainer : IMAPIProp</span></span>](imapicontainerimapiprop.md)


[<span data-ttu-id="4d25d-165">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="4d25d-165">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

