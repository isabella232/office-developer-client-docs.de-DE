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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 1fd711683ff476ef5d381bca2f9db6bc25b07c68
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792456"
---
# <a name="imapitablecollapserow"></a><span data-ttu-id="09c8e-103">IMAPITable::CollapseRow</span><span class="sxs-lookup"><span data-stu-id="09c8e-103">IMAPITable::CollapseRow</span></span>

  
  
<span data-ttu-id="09c8e-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="09c8e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="09c8e-105">Blendet eine Tabellenkategorie für erweiterte, entfernen Sie die untergeordnete Überschriften und Endknoten Zeilen aus der Tabellenansicht für die Kategorie gehören.</span><span class="sxs-lookup"><span data-stu-id="09c8e-105">Collapses an expanded table category, removing any lower-level headings and leaf rows belonging to the category from the table view.</span></span>
  
```cpp
HRESULT CollapseRow(
ULONG cbInstanceKey,
LPBYTE pbInstanceKey,
ULONG ulFlags,
ULONG FAR * lpulRowCount
);
```

## <a name="parameters"></a><span data-ttu-id="09c8e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="09c8e-106">Parameters</span></span>

 <span data-ttu-id="09c8e-107">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="09c8e-107">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="09c8e-108">[in] Die Anzahl der Bytes in der PR_INSTANCE_KEY-Eigenschaft auf den durch den Parameter _PbInstanceKey_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="09c8e-108">[in] The count of bytes in the PR_INSTANCE_KEY property pointed to by the  _pbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="09c8e-109">_pbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="09c8e-109">_pbInstanceKey_</span></span>
  
> <span data-ttu-id="09c8e-110">[in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft, die Zeile mit der Spaltenüberschrift für die Kategorie identifiziert.</span><span class="sxs-lookup"><span data-stu-id="09c8e-110">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property that identifies the heading row for the category.</span></span> 
    
 <span data-ttu-id="09c8e-111">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="09c8e-111">_ulFlags_</span></span>
  
> <span data-ttu-id="09c8e-112">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="09c8e-112">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="09c8e-113">_lpulRowCount_</span><span class="sxs-lookup"><span data-stu-id="09c8e-113">_lpulRowCount_</span></span>
  
> <span data-ttu-id="09c8e-114">[out] Ein Zeiger auf die Gesamtzahl der Zeilen, die aus der Tabellenansicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="09c8e-114">[out] A pointer to the total number of rows that are being removed from the table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="09c8e-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="09c8e-115">Return value</span></span>

<span data-ttu-id="09c8e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="09c8e-116">S_OK</span></span> 
  
> <span data-ttu-id="09c8e-117">Der Collapse-Vorgang wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="09c8e-117">The collapse operation has succeeded.</span></span>
    
<span data-ttu-id="09c8e-118">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="09c8e-118">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="09c8e-119">Die Zeile, die vom _PbInstanceKey_ -Parameter ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="09c8e-119">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> 
    
<span data-ttu-id="09c8e-120">MAPI_E_INVALID_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="09c8e-120">MAPI_E_INVALID_ENTRYID</span></span> 
  
> <span data-ttu-id="09c8e-121">Die Zeile, die vom _PbInstanceKey_ -Parameter ist nicht vorhanden.</span><span class="sxs-lookup"><span data-stu-id="09c8e-121">The row identified by the  _pbInstanceKey_ parameter does not exist.</span></span> <span data-ttu-id="09c8e-122">Dieser Fehler ist eine Alternative zur MAPI_E_NOT_FOUND. Dienstanbieter können entweder 1 zurück.</span><span class="sxs-lookup"><span data-stu-id="09c8e-122">This error is an alternative to MAPI_E_NOT_FOUND; service providers can return either one.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="09c8e-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09c8e-123">Remarks</span></span>

<span data-ttu-id="09c8e-124">Die **IMAPITable::CollapseRow** -Methode wird eine Tabellenkategorie reduziert und entfernt ihn aus der Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="09c8e-124">The **IMAPITable::CollapseRow** method collapses a table category and removes it from the table view.</span></span> <span data-ttu-id="09c8e-125">Die Zeilen werden regelmäßig beginnend in der Zeile, die von der **PR_INSTANCE_KEY** -Eigenschaft auf das durch den Parameter _PbInstanceKey_ identifiziert.</span><span class="sxs-lookup"><span data-stu-id="09c8e-125">The rows are collapsed starting at the row identified by the **PR_INSTANCE_KEY** property pointed to by the  _pbInstanceKey_ parameter.</span></span> <span data-ttu-id="09c8e-126">Die Anzahl der Zeilen, die aus der Ansicht entfernt wurden, wird in den Inhalt des Parameters _LpulRowCount_ zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="09c8e-126">The number of rows that are removed from the view is returned in the contents of the  _lpulRowCount_ parameter.</span></span> 
  
<span data-ttu-id="09c8e-127">Benachrichtigungen werden nie für Tabellenzeilen generiert, die als Ergebnis eines Vorgangs reduzieren aus einer Ansicht entfernt werden.</span><span class="sxs-lookup"><span data-stu-id="09c8e-127">Notifications are never generated for table rows that are removed from a view as the result of a collapse operation.</span></span> 
  
<span data-ttu-id="09c8e-128">Wenn eine Zeile, die durch eine Textmarke definiert wird aus der Ansicht reduziert ist, wird die Textmarke So zeigen Sie auf die nächste sichtbare Zeile verschoben.</span><span class="sxs-lookup"><span data-stu-id="09c8e-128">When a row that is defined by a bookmark is collapsed out of view, the bookmark is moved to point to the next visible row.</span></span> 
  
<span data-ttu-id="09c8e-129">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="09c8e-129">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="09c8e-130">MFCMAPI (engl.) (engl.)</span><span class="sxs-lookup"><span data-stu-id="09c8e-130">MFCMAPI reference</span></span>

<span data-ttu-id="09c8e-131">Beispielcode MFCMAPI (engl.) finden Sie in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="09c8e-131">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="09c8e-132">**Datei**</span><span class="sxs-lookup"><span data-stu-id="09c8e-132">**File**</span></span>|<span data-ttu-id="09c8e-133">**Funktion**</span><span class="sxs-lookup"><span data-stu-id="09c8e-133">**Function**</span></span>|<span data-ttu-id="09c8e-134">**Comment**</span><span class="sxs-lookup"><span data-stu-id="09c8e-134">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="09c8e-135">ContentsTableListCtrl.cpp</span><span class="sxs-lookup"><span data-stu-id="09c8e-135">ContentsTableListCtrl.cpp</span></span>  <br/> |<span data-ttu-id="09c8e-136">CContentsTableListCtrl::DoExpandCollapse</span><span class="sxs-lookup"><span data-stu-id="09c8e-136">CContentsTableListCtrl::DoExpandCollapse</span></span>  <br/> |<span data-ttu-id="09c8e-137">MFCMAPI (engl.) verwendet die **IMAPITable::CollapseRow** -Methode, um eine Tabellenkategorie reduzieren.</span><span class="sxs-lookup"><span data-stu-id="09c8e-137">MFCMAPI uses the **IMAPITable::CollapseRow** method to collapse a table category.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09c8e-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09c8e-138">See also</span></span>



[<span data-ttu-id="09c8e-139">IMAPITable::ExpandRow</span><span class="sxs-lookup"><span data-stu-id="09c8e-139">IMAPITable::ExpandRow</span></span>](imapitable-expandrow.md)
  
[<span data-ttu-id="09c8e-140">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="09c8e-140">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="09c8e-141">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="09c8e-141">IMAPITable::QuerySortOrder</span></span>](imapitable-querysortorder.md)
  
[<span data-ttu-id="09c8e-142">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="09c8e-142">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="09c8e-143">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="09c8e-143">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="09c8e-144">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="09c8e-144">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="09c8e-145">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="09c8e-145">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)


[<span data-ttu-id="09c8e-146">MFCMAPI (engl.) als ein Codebeispiel</span><span class="sxs-lookup"><span data-stu-id="09c8e-146">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

