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
ms.openlocfilehash: 7351457dc5b72cfc4a7ef9f91e9d33a80ca98c39
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414067"
---
# <a name="imapitablesetcollapsestate"></a><span data-ttu-id="f153f-103">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="f153f-103">IMAPITable::SetCollapseState</span></span>

  
  
<span data-ttu-id="f153f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f153f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f153f-105">Erstellt den aktuellen erweiterten oder reduzierten Zustand einer kategorisierten Tabelle mithilfe von Daten, die durch einen vorherigen Aufruf der [IMAPITable::GetCollapseState-Methode gespeichert](imapitable-getcollapsestate.md) wurden.</span><span class="sxs-lookup"><span data-stu-id="f153f-105">Rebuilds the current expanded or collapsed state of a categorized table using data that was saved by a prior call to the [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) method.</span></span> 
  
```cpp
HRESULT SetCollapseState(
ULONG ulFlags,
ULONG cbCollapseState,
LPBYTE pbCollapseState,
BOOKMARK FAR * lpbkLocation
);
```

## <a name="parameters"></a><span data-ttu-id="f153f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="f153f-106">Parameters</span></span>

 <span data-ttu-id="f153f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f153f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="f153f-108">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="f153f-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="f153f-109">_cbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="f153f-109">_cbCollapseState_</span></span>
  
> <span data-ttu-id="f153f-110">[in] Anzahl der Bytes in der Struktur, auf die der  _pbCollapseState-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="f153f-110">[in] Count of bytes in the structure pointed to by the  _pbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="f153f-111">_pbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="f153f-111">_pbCollapseState_</span></span>
  
> <span data-ttu-id="f153f-112">[in] Zeiger auf die Strukturen, die die Daten enthalten, die zum Neuerstellen der Tabellenansicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f153f-112">[in] Pointer to the structures containing the data needed to rebuild the table view.</span></span>
    
 <span data-ttu-id="f153f-113">_lpbkLocation_</span><span class="sxs-lookup"><span data-stu-id="f153f-113">_lpbkLocation_</span></span>
  
> <span data-ttu-id="f153f-114">[out] Zeiger auf eine Textmarke, die die Zeile in der Tabelle identifiziert, in der der reduzierte oder erweiterte Zustand neu erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="f153f-114">[out] Pointer to a bookmark identifying the row in the table at which the collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="f153f-115">Diese Textmarke und der Instanzschlüssel, der im  _lpbInstanceKey-Parameter_ im Aufruf von [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) übergeben wurde, identifizieren dieselbe Zeile.</span><span class="sxs-lookup"><span data-stu-id="f153f-115">This bookmark and the instance key passed in the  _lpbInstanceKey_ parameter in the call to [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) identify the same row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f153f-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f153f-116">Return value</span></span>

<span data-ttu-id="f153f-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="f153f-117">S_OK</span></span> 
  
> <span data-ttu-id="f153f-118">Der Status der kategorisierten Tabelle wurde erfolgreich neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="f153f-118">The state of the categorized table was successfully rebuilt.</span></span>
    
<span data-ttu-id="f153f-119">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="f153f-119">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="f153f-120">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="f153f-120">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="f153f-121">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="f153f-121">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="f153f-122">MAPI_E_UNABLE_TO_COMPLETE</span><span class="sxs-lookup"><span data-stu-id="f153f-122">MAPI_E_UNABLE_TO_COMPLETE</span></span> 
  
> <span data-ttu-id="f153f-123">Die Tabelle konnte die Neuerstellung der reduzierten oder erweiterten Ansicht nicht beenden.</span><span class="sxs-lookup"><span data-stu-id="f153f-123">The table could not finish rebuilding the collapsed or expanded view.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f153f-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f153f-124">Remarks</span></span>

<span data-ttu-id="f153f-125">Die **IMAPITable::SetCollapseState-Methode** stellt den erweiterten oder reduzierten Zustand der Tabellenansicht wieder ein.</span><span class="sxs-lookup"><span data-stu-id="f153f-125">The **IMAPITable::SetCollapseState** method reestablishes the expanded or collapsed state of the table view.</span></span> <span data-ttu-id="f153f-126">**SetCollapseState und** **GetCollapseState** arbeiten wie folgt zusammen:</span><span class="sxs-lookup"><span data-stu-id="f153f-126">**SetCollapseState** and **GetCollapseState** work together as follows:</span></span> 
  
1. <span data-ttu-id="f153f-127">Wenn sich der Status einer kategorisierten Tabelle ändern soll, wird [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) aufgerufen, um alle Daten zu speichern, die sich auf den Status vor der Änderung bezieht.</span><span class="sxs-lookup"><span data-stu-id="f153f-127">When the state of a categorized table is about to change, [IMAPITable::GetCollapseState](imapitable-getcollapsestate.md) is called to save all of the data pertaining to the state prior to the change.</span></span> 
    
2. <span data-ttu-id="f153f-128">Um die Ansicht der Tabelle in ihrem gespeicherten Zustand wiederherzustellen, **wird SetCollapseState** aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="f153f-128">To restore the view of the table to its saved state, **SetCollapseState** is called.</span></span> <span data-ttu-id="f153f-129">Die von **GetCollapseState gespeicherten** Daten werden an **SetCollapseState übergeben.**</span><span class="sxs-lookup"><span data-stu-id="f153f-129">The data saved by **GetCollapseState** is passed to **SetCollapseState**.</span></span> <span data-ttu-id="f153f-130">**SetCollapseState** kann diese Daten verwenden, um den Zustand wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="f153f-130">**SetCollapseState** is able to use that data to restore the state.</span></span> 
    
3. <span data-ttu-id="f153f-131">**SetCollapseState** gibt als Ausgabeparameter eine Textmarke zurück, die dieselbe Zeile identifiziert wie die Instanztaste, die als Eingabe an **GetCollapseState übergeben wird.**</span><span class="sxs-lookup"><span data-stu-id="f153f-131">**SetCollapseState** returns as an output parameter a bookmark that identifies the same row as the instance key passed as input to **GetCollapseState**.</span></span>
    
<span data-ttu-id="f153f-132">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="f153f-132">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="f153f-133">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="f153f-133">Notes to implementers</span></span>

<span data-ttu-id="f153f-134">Sie sind für die Überprüfung verantwortlich, ob die Sortierreihenfolge und die Einschränkungen exakt mit der zum Zeitpunkt des **GetCollapseState-Aufrufs identisch** sind.</span><span class="sxs-lookup"><span data-stu-id="f153f-134">You are responsible for verifying that the sort order and restrictions are exactly the same as they were at the time of the **GetCollapseState** call.</span></span> <span data-ttu-id="f153f-135">Wenn eine Änderung vorgenommen wurde, **sollte SetCollapseState** nicht aufgerufen werden, da die Ergebnisse unvorhersehbar sein können.</span><span class="sxs-lookup"><span data-stu-id="f153f-135">If a change has been made, **SetCollapseState** should not be called because the results can be unpredictable.</span></span> <span data-ttu-id="f153f-136">Dies kann passieren, wenn ein Client z. B. **GetCollapseState** aufruft und **anschließend SortTable** zum Ändern des Sortierschlüssels vor dem Aufrufen von **SetCollapseState .**</span><span class="sxs-lookup"><span data-stu-id="f153f-136">This can happen if, for example, a client calls **GetCollapseState** and then **SortTable** to change the sort key before calling **SetCollapseState**.</span></span> <span data-ttu-id="f153f-137">Um sicher zu sein, überprüfen Sie, ob die gespeicherten Daten noch gültig sind, bevor Sie mit der Wiederherstellung fortfahren.</span><span class="sxs-lookup"><span data-stu-id="f153f-137">To be safe, check that the saved data is still valid before proceeding with the restoration.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f153f-138">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="f153f-138">Notes to callers</span></span>

<span data-ttu-id="f153f-139">Zum Aufrufen **von SetCollapseState** müssen Sie zuvor **GetCollapseState aufgerufen haben.**</span><span class="sxs-lookup"><span data-stu-id="f153f-139">To call **SetCollapseState**, you must have previously called **GetCollapseState**.</span></span> <span data-ttu-id="f153f-140">Die Sortierreihenfolge zum Festlegen der Kategorien sollte für beide Methoden identisch sein.</span><span class="sxs-lookup"><span data-stu-id="f153f-140">The sort order establishing the categories should be the same for both methods.</span></span> <span data-ttu-id="f153f-141">Wenn sich die Sortierreihenfolgen unterscheiden, sind die Ergebnisse des **SetCollapseState-Vorgangs** unvorhersehbar.</span><span class="sxs-lookup"><span data-stu-id="f153f-141">If the sort orders differ, the results of the **SetCollapseState** operation are unpredictable.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f153f-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f153f-142">See also</span></span>



[<span data-ttu-id="f153f-143">IMAPITable::CreateBookmark</span><span class="sxs-lookup"><span data-stu-id="f153f-143">IMAPITable::CreateBookmark</span></span>](imapitable-createbookmark.md)
  
[<span data-ttu-id="f153f-144">IMAPITable::FreeBookmark</span><span class="sxs-lookup"><span data-stu-id="f153f-144">IMAPITable::FreeBookmark</span></span>](imapitable-freebookmark.md)
  
[<span data-ttu-id="f153f-145">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="f153f-145">IMAPITable::GetCollapseState</span></span>](imapitable-getcollapsestate.md)
  
[<span data-ttu-id="f153f-146">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f153f-146">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

