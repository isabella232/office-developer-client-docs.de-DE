---
title: IMAPITableGetCollapseState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.GetCollapseState
api_type:
- COM
ms.assetid: fd4ea496-4c83-49cd-854e-f373cc1ed2af
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 97575a65cd6825e07d6f11c813beec539f99f53a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436076"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="1a697-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="1a697-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="1a697-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1a697-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1a697-105">Gibt die Daten zurück, die zum Neuerstellen des aktuellen reduzierten oder erweiterten Zustands einer kategorisierten Tabelle erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1a697-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="1a697-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="1a697-106">Parameters</span></span>

 <span data-ttu-id="1a697-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1a697-107">_ulFlags_</span></span>
  
> <span data-ttu-id="1a697-108">Reserviert; muss null sein.</span><span class="sxs-lookup"><span data-stu-id="1a697-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="1a697-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="1a697-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="1a697-110">[in] Die Anzahl der Bytes im Instanzschlüssel, auf die der  _lpbInstanceKey-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="1a697-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="1a697-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="1a697-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="1a697-112">[in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) -Eigenschaft der Zeile, in der der aktuelle reduzierte oder erweiterte Zustand neu erstellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="1a697-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="1a697-113">Der  _lpbInstanceKey-Parameter_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="1a697-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="1a697-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="1a697-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="1a697-115">[out] Ein Zeiger auf die Anzahl der Strukturen, auf die der  _lppbCollapseState-Parameter_ verweist.</span><span class="sxs-lookup"><span data-stu-id="1a697-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="1a697-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="1a697-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="1a697-117">[out] Ein Zeiger auf einen Zeiger auf Strukturen, die Daten enthalten, die die aktuelle Tabellenansicht beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1a697-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1a697-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="1a697-118">Return value</span></span>

<span data-ttu-id="1a697-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="1a697-119">S_OK</span></span> 
  
> <span data-ttu-id="1a697-120">Der Status für die kategorisierte Tabelle wurde erfolgreich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="1a697-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="1a697-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="1a697-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="1a697-122">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Vorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="1a697-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="1a697-123">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="1a697-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="1a697-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="1a697-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="1a697-125">Die Tabelle unterstützt keine Kategorisierung und erweiterte und reduzierte Ansichten.</span><span class="sxs-lookup"><span data-stu-id="1a697-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1a697-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a697-126">Remarks</span></span>

<span data-ttu-id="1a697-127">Die **IMAPITable::GetCollapseState-Methode** arbeitet mit der [IMAPITable::SetCollapseState-Methode,](imapitable-setcollapsestate.md) um die Benutzeransicht einer kategorisierten Tabelle zu ändern.</span><span class="sxs-lookup"><span data-stu-id="1a697-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="1a697-128">**GetCollapseState** speichert die Daten, die **setCollapseState** zum Neuerstellen der entsprechenden Ansichten der Kategorien einer kategorisierten Tabelle benötigt.</span><span class="sxs-lookup"><span data-stu-id="1a697-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="1a697-129">Dienstanbieter bestimmen die zu speichernde Daten.</span><span class="sxs-lookup"><span data-stu-id="1a697-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="1a697-130">Die meisten Dienstanbieter, die **GetCollapseState** implementieren, speichern jedoch Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1a697-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="1a697-131">Die Sortiertasten (Standardspalten und Kategoriespalten).</span><span class="sxs-lookup"><span data-stu-id="1a697-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="1a697-132">Informationen zur Zeile, die der Instanzschlüssel darstellt.</span><span class="sxs-lookup"><span data-stu-id="1a697-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="1a697-133">Informationen zum Wiederherstellen der reduzierten und erweiterten Kategorien der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="1a697-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="1a697-134">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sorting and Categorization](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="1a697-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1a697-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="1a697-135">Notes to implementers</span></span>

<span data-ttu-id="1a697-136">Store den aktuellen Status aller Knoten einer Tabelle im _lppbCollapseState-Parameter._</span><span class="sxs-lookup"><span data-stu-id="1a697-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1a697-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="1a697-137">Notes to callers</span></span>

<span data-ttu-id="1a697-138">Rufen Sie **immer GetCollapseState auf,** bevor Sie **SetCollapseState aufrufen.**</span><span class="sxs-lookup"><span data-stu-id="1a697-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1a697-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a697-139">See also</span></span>



[<span data-ttu-id="1a697-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="1a697-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="1a697-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1a697-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

