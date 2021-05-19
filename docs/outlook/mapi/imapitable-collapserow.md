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
# <a name="imapitablecollapserow"></a><span data-ttu-id="68ead-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="68ead-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="68ead-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="68ead-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="68ead-105">Reduziert eine erweiterte Tabellenkategorie, indem alle Überschriften auf niedrigerer Ebene und Blattzeilen, die zu der Kategorie gehören, aus der Tabellenansicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="68ead-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="68ead-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="68ead-106">Parameters</span></span>

 <span data-ttu-id="68ead-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="68ead-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="68ead-108">[in] Die Anzahl der Bytes in der PR_INSTANCE_KEY, auf die der  _pbInstanceKey-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="68ead-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="68ead-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="68ead-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="68ead-110">[in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, die die Überschriftenzeile für die Kategorie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="68ead-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="68ead-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="68ead-111">_ulFlags_</span></span>
  
> <span data-ttu-id="68ead-112">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="68ead-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="68ead-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="68ead-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="68ead-114">[out] Ein Zeiger auf die Gesamtanzahl der Zeilen, die aus der Tabellenansicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="68ead-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="68ead-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="68ead-115">Return value</span></span>

<span data-ttu-id="68ead-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="68ead-116">S_OK</span></span> 
  
> <span data-ttu-id="68ead-117">Der Collapse-Vorgang ist erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="68ead-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="68ead-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="68ead-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="68ead-119">Die vom  _pbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="68ead-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="68ead-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="68ead-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="68ead-121">Die vom  _pbInstanceKey-Parameter_ identifizierte Zeile ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="68ead-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="68ead-122">Dieser Fehler ist eine Alternative zu MAPI_E_NOT_FOUND. Dienstanbieter können eine der beiden Zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="68ead-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="68ead-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="68ead-123">Remarks</span></span>

<span data-ttu-id="68ead-124">Die **IMAPITable::CollapseRow-Methode** reduziert eine Tabellenkategorie und entfernt sie aus der Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="68ead-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="68ead-125">Die Zeilen werden beginnend mit der Zeile reduziert, die von der **PR_INSTANCE_KEY-Eigenschaft** identifiziert wird, auf die der  _pbInstanceKey-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="68ead-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="68ead-126">Die Anzahl der Zeilen, die aus der Ansicht entfernt werden, wird im Inhalt des  _lpulRowCount-Parameters_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="68ead-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="68ead-127">Benachrichtigungen werden niemals für Tabellenzeilen generiert, die als Ergebnis eines Reduzierens aus einer Ansicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="68ead-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="68ead-128">Wenn eine zeile, die durch eine Textmarke definiert ist, aus der Sicht reduziert wird, wird die Textmarke verschoben, um auf die nächste sichtbare Zeile zu zeigen.</span><span class="sxs-lookup"><span data-stu-id="68ead-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="68ead-129">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="68ead-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="68ead-130">MFCMAPI-Referenz</span><span class="sxs-lookup"><span data-stu-id="68ead-130">MFCMAPI reference</span></span>

<span data-ttu-id="68ead-131">Einen MFCMAP-Beispielcode finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="68ead-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="68ead-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="68ead-132">**File**</span></span>|<span data-ttu-id="68ead-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="68ead-133">**Function**</span></span>|<span data-ttu-id="68ead-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="68ead-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="68ead-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="68ead-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="68ead-136">CContentsTableListCtrl::D oExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="68ead-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="68ead-137">MFCMAPI verwendet die **IMAPITable::CollapseRow-Methode,** um eine Tabellenkategorie zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="68ead-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="68ead-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68ead-138">See also</span></span>



[<span data-ttu-id="68ead-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="68ead-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="68ead-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="68ead-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="68ead-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="68ead-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="68ead-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="68ead-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="68ead-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="68ead-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="68ead-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="68ead-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="68ead-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="68ead-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="68ead-146">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="68ead-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

