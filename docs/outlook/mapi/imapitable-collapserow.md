---
title: IMAPITableCollapseRow
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.CollapseRow
api_type:
- COM
ms.assetid: 1a23e555-be26-43fb-a715-cfc4ffa623cd
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e6a180ceb325a705ebf226bb728c52cce7396490
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416174"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="54fb8-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="54fb8-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="54fb8-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="54fb8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="54fb8-105">Reduziert eine erweiterte Tabellen Kategorie, wobei alle untergeordneten Überschriften und Blattzeilen, die der Kategorie angehören, aus der Tabellenansicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="54fb8-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="54fb8-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="54fb8-106">Parameters</span></span>

 <span data-ttu-id="54fb8-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="54fb8-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="54fb8-108">in Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft, auf die durch den _pbInstanceKey_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="54fb8-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="54fb8-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="54fb8-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="54fb8-110">in Ein Zeiger auf die **PR_INSTANCE_KEY** ([pidtaginstancekey (](pidtaginstancekey-canonical-property.md))-Eigenschaft, die die Überschriftenzeile für die Kategorie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="54fb8-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="54fb8-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="54fb8-111">_ulFlags_</span></span>
  
> <span data-ttu-id="54fb8-112">Reserviert muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="54fb8-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="54fb8-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="54fb8-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="54fb8-114">Out Ein Zeiger auf die Gesamtanzahl der Zeilen, die aus der Tabellenansicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="54fb8-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="54fb8-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="54fb8-115">Return value</span></span>

<span data-ttu-id="54fb8-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="54fb8-116">S_OK</span></span> 
  
> <span data-ttu-id="54fb8-117">Der Collapse-Vorgang wurde erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="54fb8-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="54fb8-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="54fb8-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="54fb8-119">Die durch den _pbInstanceKey_ -Parameter angegebene Zeile ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="54fb8-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="54fb8-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="54fb8-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="54fb8-121">Die durch den _pbInstanceKey_ -Parameter angegebene Zeile ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="54fb8-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="54fb8-122">Dieser Fehler ist eine Alternative zu MAPI_E_NOT_FOUND; Dienstanbieter können eine der beiden zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="54fb8-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="54fb8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="54fb8-123">Remarks</span></span>

<span data-ttu-id="54fb8-124">Die **IMAPITable:: CollapseRow** -Methode reduziert eine Tabellen Kategorie und entfernt Sie aus der Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="54fb8-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="54fb8-125">Die Zeilen werden beginnend bei der Zeile reduziert, die von der **PR_INSTANCE_KEY** -Eigenschaft identifiziert wird, auf die durch den _pbInstanceKey_ -Parameter verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="54fb8-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="54fb8-126">Die Anzahl der Zeilen, die aus der Ansicht entfernt werden, wird im Inhalt des _lpulRowCount_ -Parameters zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="54fb8-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="54fb8-127">Benachrichtigungen werden nie für Tabellenzeilen generiert, die aus einer Ansicht als Ergebnis eines Collapse-Vorgangs entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="54fb8-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="54fb8-128">Wenn eine Zeile, die durch eine Textmarke definiert ist, ausgeblendet ist, wird die Textmarke so verschoben, dass Sie auf die nächste sichtbare Zeile zeigt.</span><span class="sxs-lookup"><span data-stu-id="54fb8-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="54fb8-129">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und kategorisieren](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="54fb8-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="54fb8-130">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="54fb8-130">MFCMAPI reference</span></span>

<span data-ttu-id="54fb8-131">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="54fb8-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="54fb8-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="54fb8-132">**File**</span></span>|<span data-ttu-id="54fb8-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="54fb8-133">**Function**</span></span>|<span data-ttu-id="54fb8-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="54fb8-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="54fb8-135">ContentsTableListCtrl. cpp</span><span class="sxs-lookup"><span data-stu-id="54fb8-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="54fb8-136">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="54fb8-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="54fb8-137">MFCMAPI verwendet die **IMAPITable:: CollapseRow** -Methode, um eine Tabellen Kategorie zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="54fb8-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="54fb8-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="54fb8-138">See also</span></span>



[<span data-ttu-id="54fb8-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="54fb8-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="54fb8-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="54fb8-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="54fb8-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="54fb8-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="54fb8-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="54fb8-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="54fb8-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="54fb8-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="54fb8-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="54fb8-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="54fb8-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="54fb8-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="54fb8-146">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="54fb8-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

