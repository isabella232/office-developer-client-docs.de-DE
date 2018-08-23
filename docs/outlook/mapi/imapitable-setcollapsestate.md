---
title: IMAPITableSetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SetCollapseState
api_type:
- COM
ms.assetid: 31325e8f-1cf9-49b2-8118-953996b0037f
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 51c239897e5e225a0765f78404526e2836371f30
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567902"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="046ea-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="046ea-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="046ea-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="046ea-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="046ea-105">Erstellt den aktuellen erweiterten oder reduzierten den Status einer kategorisierten Tabelle mit Daten, die durch einen vorherigen Aufruf der [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) -Methode gespeichert wurde neu.</span><span class="sxs-lookup"><span data-stu-id="046ea-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="046ea-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="046ea-106">Parameters</span></span>

 <span data-ttu-id="046ea-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="046ea-107">_ulFlags_</span></span>
  
> <span data-ttu-id="046ea-108">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="046ea-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="046ea-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="046ea-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="046ea-110">[in] Die Anzahl der Bytes in der Struktur auf den durch den Parameter _PbCollapseState_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="046ea-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="046ea-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="046ea-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="046ea-112">[in] Zeiger auf die Strukturen, die mit den Daten, die Tabellenansicht neu erstellen.</span><span class="sxs-lookup"><span data-stu-id="046ea-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="046ea-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="046ea-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="046ea-114">[out] Zeiger auf eine Textmarke, identifiziert der Zeile in der Tabelle, an der der reduzierte oder erweiterte Zustand neu erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="046ea-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="046ea-115">Dieses Lesezeichen und im _LpbInstanceKey_ -Parameter im Aufruf [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) übergebenen Instanz Taste identifizieren die gleiche Zeile.</span><span class="sxs-lookup"><span data-stu-id="046ea-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="046ea-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="046ea-116">Return value</span></span>

<span data-ttu-id="046ea-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="046ea-117">S_OK</span></span> 
  
> <span data-ttu-id="046ea-118">Der Zustand der kategorisierten Tabelle wurden erfolgreich neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="046ea-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="046ea-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="046ea-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="046ea-120">Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang gestartet wird dass.</span><span class="sxs-lookup"><span data-stu-id="046ea-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="046ea-121">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="046ea-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="046ea-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="046ea-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="046ea-123">Die Tabelle konnte nicht fertig gestellt Neuerstellen der Ansicht reduzierten oder erweiterten.</span><span class="sxs-lookup"><span data-stu-id="046ea-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="046ea-124">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="046ea-124">Remarks</span></span>

<span data-ttu-id="046ea-125">Die **IMAPITable::SetCollapseState** -Methode wird den Zustand erweiterten oder reduzierten die Tabellenansicht.</span><span class="sxs-lookup"><span data-stu-id="046ea-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="046ea-126">**SetCollapseState** und **GetCollapseState** arbeiten wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="046ea-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="046ea-127">Wenn der Zustand einer kategorisierten Tabelle zu ändern, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) aufgerufen, um alle Daten für den Zustand vor der Änderung zu speichern.</span><span class="sxs-lookup"><span data-stu-id="046ea-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="046ea-128">**SetCollapseState** wird aufgerufen, um die Ansicht der Tabelle auf den gespeicherten Zustand wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="046ea-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="046ea-129">Die Daten, die **GetCollapseState** gespeichert werden an **SetCollapseState**übergeben.</span><span class="sxs-lookup"><span data-stu-id="046ea-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="046ea-130">**SetCollapseState** ist berechtigt, diese Daten verwenden, um den Zustand wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="046ea-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="046ea-131">**SetCollapseState** gibt als Ausgabeparameter eine Textmarke, die die gleiche Zeile als Instanzschlüssel übergeben als Eingabe in **GetCollapseState**identifiziert.</span><span class="sxs-lookup"><span data-stu-id="046ea-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="046ea-132">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="046ea-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="046ea-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="046ea-133">Notes to implementers</span></span>

<span data-ttu-id="046ea-134">Sie sind verantwortlich für das Überprüfen, dass die Sortierreihenfolge und Einschränkungen identisch sind, wie sie zum Zeitpunkt des Anrufs **GetCollapseState** waren.</span><span class="sxs-lookup"><span data-stu-id="046ea-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="046ea-135">Wenn eine Änderung vorgenommen wurde, sollte **SetCollapseState** nicht aufgerufen werden, da die Ergebnisse unvorhersehbar können.</span><span class="sxs-lookup"><span data-stu-id="046ea-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="046ea-136">Dies kann vorkommen, wenn beispielsweise ein Client **GetCollapseState** und dann **SortTable** , um den Sortierschlüssel zu ändern, vor dem Aufruf von **SetCollapseState**aufruft.</span><span class="sxs-lookup"><span data-stu-id="046ea-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="046ea-137">Aus Sicherheitsgründen sicher, dass die gespeicherten Daten noch gültig ist, bevor Sie mit der Wiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="046ea-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="046ea-138">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="046ea-138">Notes to callers</span></span>

<span data-ttu-id="046ea-139">Wenn **SetCollapseState**anrufen möchten, müssen Sie zuvor **GetCollapseState**aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="046ea-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="046ea-140">Die Sortierreihenfolge zur Festlegung der Kategorien sollten für beide Methoden identisch sein.</span><span class="sxs-lookup"><span data-stu-id="046ea-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="046ea-141">Wenn die Sortierreihenfolgen unterscheiden, sind die Ergebnisse des Vorgangs **SetCollapseState** unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="046ea-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="046ea-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="046ea-142">See also</span></span>



[<span data-ttu-id="046ea-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="046ea-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="046ea-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="046ea-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="046ea-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="046ea-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="046ea-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="046ea-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

