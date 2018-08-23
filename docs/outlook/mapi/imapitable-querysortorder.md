---
title: IMAPITableQuerySortOrder
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QuerySortOrder
api_type:
- COM
ms.assetid: 7b4ca523-0703-417c-8586-c4324c200020
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48ca692779fb53cab386d8a18b5f0a50e11d531c
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22569435"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="e6e3e-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="e6e3e-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="e6e3e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e6e3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e6e3e-105">Ruft die aktuelle Sortierreihenfolge für eine Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="e6e3e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e6e3e-106">Parameters</span></span>

 <span data-ttu-id="e6e3e-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="e6e3e-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="e6e3e-108">[out] Zeiger auf einen Zeiger auf die [SSortOrderSet](ssortorderset.md) -Struktur, die die aktuelle Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e6e3e-109">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="e6e3e-109">Return value</span></span>

<span data-ttu-id="e6e3e-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="e6e3e-110">S_OK</span></span> 
  
> <span data-ttu-id="e6e3e-111">Die aktuelle Sortierreihenfolge wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="e6e3e-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="e6e3e-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="e6e3e-113">Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang Reihenfolge sortieren nicht gestartet dass.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="e6e3e-114">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e6e3e-115">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="e6e3e-115">Remarks</span></span>

<span data-ttu-id="e6e3e-116">Die **IMAPITable::QuerySortOrder** -Methode ruft die aktuelle Sortierreihenfolge für eine Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="e6e3e-117">Sortierreihenfolgen werden mit einer [SSortOrderSet](ssortorderset.md) Struktur beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="e6e3e-118">Der **cSorts** Member der Struktur **SSortOrderSet** kann wenn auf 0 (null) festgelegt werden:</span><span class="sxs-lookup"><span data-stu-id="e6e3e-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="e6e3e-119">Die Tabelle ist nicht sortiert.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="e6e3e-120">Es gibt keine Informationen darüber, wie die Tabelle sortiert ist.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="e6e3e-121">Die Struktur **SSortOrderSet** eignet sich nicht für die Beschreibung der Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="e6e3e-122">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e6e3e-122">Notes to implementers</span></span>

<span data-ttu-id="e6e3e-123">Wenn Ihre [SortTable](imapitable-sorttable.md) -Methode mit einer **SSortOrderSet** Struktur, enthält keine Spalten in der Sortierschlüssel aufgerufen wird, entfernen Sie die aktuelle Sortierreihenfolge und wenden Sie die Standardreihenfolge an, sofern vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="e6e3e-124">Bei nachfolgenden Aufrufen von **QuerySortOrder**können Sie auswählen, ob NULL oder mehr Spalten für den Sortierschlüssel zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="e6e3e-125">Sie können weitere Spalten als in der Ansicht vorhanden sind zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="e6e3e-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="e6e3e-126">Weitere Informationen zum Sortieren finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="e6e3e-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e6e3e-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e6e3e-127">See also</span></span>



[<span data-ttu-id="e6e3e-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="e6e3e-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="e6e3e-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="e6e3e-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="e6e3e-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="e6e3e-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="e6e3e-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e6e3e-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

