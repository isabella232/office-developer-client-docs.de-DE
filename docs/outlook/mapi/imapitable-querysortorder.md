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
ms.openlocfilehash: 61991972fdf8674a9ffd2b790e26c7fa669df357
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407550"
---
# <a name="imapitablequerysortorder"></a><span data-ttu-id="00850-103">IMAPITable::QuerySortOrder</span><span class="sxs-lookup"><span data-stu-id="00850-103">IMAPITable::QuerySortOrder</span></span>

  
  
<span data-ttu-id="00850-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="00850-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="00850-105">Ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="00850-105">Retrieves the current sort order for a table.</span></span>
  
```cpp
HRESULT QuerySortOrder(
LPSSortOrderSet FAR * lppSortCriteria
);
```

## <a name="parameters"></a><span data-ttu-id="00850-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="00850-106">Parameters</span></span>

 <span data-ttu-id="00850-107">_lppSortCriteria_</span><span class="sxs-lookup"><span data-stu-id="00850-107">_lppSortCriteria_</span></span>
  
> <span data-ttu-id="00850-108">[out] Zeiger auf einen Zeiger auf die [SSortOrderSet-Struktur](ssortorderset.md) mit der aktuellen Sortierreihenfolge.</span><span class="sxs-lookup"><span data-stu-id="00850-108">[out] Pointer to a pointer to the [SSortOrderSet](ssortorderset.md) structure holding the current sort order.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="00850-109">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00850-109">Return value</span></span>

<span data-ttu-id="00850-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="00850-110">S_OK</span></span> 
  
> <span data-ttu-id="00850-111">Die aktuelle Sortierreihenfolge wurde erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="00850-111">The current sort order was successfully returned.</span></span>
    
<span data-ttu-id="00850-112">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="00850-112">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="00850-113">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Sortierreihenfolgenabrufvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="00850-113">Another operation is in progress that prevents the sort order retrieval operation from starting.</span></span> <span data-ttu-id="00850-114">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="00850-114">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="00850-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00850-115">Remarks</span></span>

<span data-ttu-id="00850-116">Die **IMAPITable::QuerySortOrder-Methode** ruft die aktuelle Sortierreihenfolge für eine Tabelle ab.</span><span class="sxs-lookup"><span data-stu-id="00850-116">The **IMAPITable::QuerySortOrder** method retrieves the current sort order for a table.</span></span> <span data-ttu-id="00850-117">Sortierreihenfolgen werden mit einer [SSortOrderSet-Struktur](ssortorderset.md) beschrieben.</span><span class="sxs-lookup"><span data-stu-id="00850-117">Sort orders are described with an [SSortOrderSet](ssortorderset.md) structure.</span></span> 
  
- <span data-ttu-id="00850-118">Das **cSorts-Element** der **SSortOrderSet-Struktur** kann auf Null festgelegt werden, wenn:</span><span class="sxs-lookup"><span data-stu-id="00850-118">The **cSorts** member of the **SSortOrderSet** structure can be set to zero if:</span></span> 
    
- <span data-ttu-id="00850-119">Die Tabelle ist unsortiert.</span><span class="sxs-lookup"><span data-stu-id="00850-119">The table is unsorted.</span></span>
    
- <span data-ttu-id="00850-120">Es gibt keine Informationen zur Sortierung der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="00850-120">There is no information about how the table is sorted.</span></span>
    
- <span data-ttu-id="00850-121">Die **SSortOrderSet-Struktur** ist nicht geeignet, um die Sortierreihenfolge zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="00850-121">The **SSortOrderSet** structure is not appropriate for describing the sort order.</span></span> 
    
## <a name="notes-to-implementers"></a><span data-ttu-id="00850-122">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="00850-122">Notes to implementers</span></span>

<span data-ttu-id="00850-123">Wenn sie ihre [IMAPITable::SortTable-Methode](imapitable-sorttable.md) mit einer **SSortOrderSet-Struktur** aufruft, die keine Spalten im Sortierschlüssel enthält, entfernen Sie die aktuelle Sortierreihenfolge, und wenden Sie die Standardreihenfolge an, falls eine solche besteht.</span><span class="sxs-lookup"><span data-stu-id="00850-123">If a call is made to your [IMAPITable::SortTable](imapitable-sorttable.md) method with an **SSortOrderSet** structure containing zero columns in the sort key, remove the current sort order and apply the default order, if there is one.</span></span> <span data-ttu-id="00850-124">Bei nachfolgenden Aufrufen von **QuerySortOrder** können Sie auswählen, ob null oder mehr Spalten für den Sortierschlüssel zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="00850-124">In subsequent calls to **QuerySortOrder**, you can choose whether to return zero or more columns for the sort key.</span></span> <span data-ttu-id="00850-125">Sie können mehr Spalten als in der aktuellen Ansicht zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="00850-125">You can return more columns than are in the present view.</span></span>
  
<span data-ttu-id="00850-126">Weitere Informationen zum Sortieren finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="00850-126">For more information about sorting, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="00850-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00850-127">See also</span></span>



[<span data-ttu-id="00850-128">IMAPITable::SortTable</span><span class="sxs-lookup"><span data-stu-id="00850-128">IMAPITable::SortTable</span></span>](imapitable-sorttable.md)
  
[<span data-ttu-id="00850-129">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="00850-129">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="00850-130">SSortOrderSet</span><span class="sxs-lookup"><span data-stu-id="00850-130">SSortOrderSet</span></span>](ssortorderset.md)
  
[<span data-ttu-id="00850-131">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="00850-131">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

