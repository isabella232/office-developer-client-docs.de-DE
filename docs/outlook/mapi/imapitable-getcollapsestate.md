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
ms.openlocfilehash: 2c1246c46e9723cd3f6d92f0a44fc1419eef4a2e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792452"
---
# <a name="imapitablegetcollapsestate"></a><span data-ttu-id="9102c-103">IMAPITable::GetCollapseState</span><span class="sxs-lookup"><span data-stu-id="9102c-103">IMAPITable::GetCollapseState</span></span>

  
  
<span data-ttu-id="9102c-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="9102c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="9102c-105">Gibt die Daten, die benötigt werden, um die aktuelle neu erstellen erweitert oder reduziert Zustand einer kategorisierten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9102c-105">Returns the data that is needed to rebuild the current collapsed or expanded state of a categorized table.</span></span>
  
```cpp
HRESULT GetCollapseState(
ULONG ulFlags,
ULONG cbInstanceKey,
LPBYTE lpbInstanceKey,
ULONG FAR * lpcbCollapseState,
LPBYTE FAR * lppbCollapseState
);
```

## <a name="parameters"></a><span data-ttu-id="9102c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9102c-106">Parameters</span></span>

 <span data-ttu-id="9102c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9102c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="9102c-108">Reserviert. NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="9102c-108">Reserved; must be zero.</span></span>
    
 <span data-ttu-id="9102c-109">_cbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="9102c-109">_cbInstanceKey_</span></span>
  
> <span data-ttu-id="9102c-110">[in] Durch den Parameter _LpbInstanceKey_ auf zeigt die Anzahl der Bytes im Instanzschlüssel.</span><span class="sxs-lookup"><span data-stu-id="9102c-110">[in] The count of bytes in the instance key pointed to by the  _lpbInstanceKey_ parameter.</span></span> 
    
 <span data-ttu-id="9102c-111">_lpbInstanceKey_</span><span class="sxs-lookup"><span data-stu-id="9102c-111">_lpbInstanceKey_</span></span>
  
> <span data-ttu-id="9102c-112">[in] Ein Zeiger auf die **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))-Eigenschaft der Zeile mit der aktuellen reduziert oder erweitert Zustand sollte neu erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9102c-112">[in] A pointer to the **PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) property of the row at which the current collapsed or expanded state should be rebuilt.</span></span> <span data-ttu-id="9102c-113">Der Parameter _LpbInstanceKey_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="9102c-113">The  _lpbInstanceKey_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="9102c-114">_lpcbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="9102c-114">_lpcbCollapseState_</span></span>
  
> <span data-ttu-id="9102c-115">[out] Ein Zeiger auf die Anzahl der Strukturen auf den durch den Parameter _LppbCollapseState_ verwiesen.</span><span class="sxs-lookup"><span data-stu-id="9102c-115">[out] A pointer to the count of structures pointed to by the  _lppbCollapseState_ parameter.</span></span> 
    
 <span data-ttu-id="9102c-116">_lppbCollapseState_</span><span class="sxs-lookup"><span data-stu-id="9102c-116">_lppbCollapseState_</span></span>
  
> <span data-ttu-id="9102c-117">[out] Ein Zeiger auf einen Zeiger auf Strukturen, die Daten enthalten, die die aktuelle Tabellenansicht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="9102c-117">[out] A pointer to a pointer to structures that contain data that describes the current table view.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9102c-118">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9102c-118">Return value</span></span>

<span data-ttu-id="9102c-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="9102c-119">S_OK</span></span> 
  
> <span data-ttu-id="9102c-120">Der Status für die kategorisierten Tabelle wurde erfolgreich gespeichert.</span><span class="sxs-lookup"><span data-stu-id="9102c-120">The state for the categorized table was successfully saved.</span></span>
    
<span data-ttu-id="9102c-121">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="9102c-121">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="9102c-122">Ein anderer Vorgang wird ausgeführt, die verhindert, den Vorgang gestartet wird dass.</span><span class="sxs-lookup"><span data-stu-id="9102c-122">Another operation is in progress that prevents the operation from starting.</span></span> <span data-ttu-id="9102c-123">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9102c-123">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
<span data-ttu-id="9102c-124">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="9102c-124">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="9102c-125">Die Tabelle unterstützt keine Kategorisierung und erweiterte und reduzierte Ansichten.</span><span class="sxs-lookup"><span data-stu-id="9102c-125">The table does not support categorization and expanded and collapsed views.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="9102c-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9102c-126">Remarks</span></span>

<span data-ttu-id="9102c-127">Die **IMAPITable::GetCollapseState** -Methode funktioniert mit der [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) -Methode zum Ändern des Benutzers Ansicht einer kategorisierten Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9102c-127">The **IMAPITable::GetCollapseState** method works with the [IMAPITable::SetCollapseState](imapitable-setcollapsestate.md) method to change the user's view of a categorized table.</span></span> <span data-ttu-id="9102c-128">**GetCollapseState** speichert die Daten, die für **SetCollapseState** zu verwenden, um die entsprechenden Ansichten der Kategorien von einer kategorisierten Tabelle neu erstellen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9102c-128">**GetCollapseState** saves the data that is needed for **SetCollapseState** to use to rebuild the appropriate views of the categories of a categorized table.</span></span> <span data-ttu-id="9102c-129">Dienstanbieter bestimmen die Daten gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="9102c-129">Service providers determine the data to be saved.</span></span> <span data-ttu-id="9102c-130">Die meisten Dienstanbieter implementieren **GetCollapseState** speichern jedoch die folgenden:</span><span class="sxs-lookup"><span data-stu-id="9102c-130">However, most service providers implementing **GetCollapseState** save the following:</span></span> 
  
- <span data-ttu-id="9102c-131">Die Sortierschlüssel (standard und Spalten Kategorie).</span><span class="sxs-lookup"><span data-stu-id="9102c-131">The sort keys (standard columns and category columns).</span></span>
    
- <span data-ttu-id="9102c-132">Informationen über die Zeile, die den Instanzschlüssel darstellt.</span><span class="sxs-lookup"><span data-stu-id="9102c-132">Information about the row that the instance key represents.</span></span>
    
- <span data-ttu-id="9102c-133">Informationen zum Wiederherstellen der reduzierten und erweiterten Kategorien der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9102c-133">Information to restore the collapsed and expanded categories of the table.</span></span>
    
<span data-ttu-id="9102c-134">Weitere Informationen zu kategorisierten Tabellen finden Sie unter [Sortieren und Kategorisierung](sorting-and-categorization.md).</span><span class="sxs-lookup"><span data-stu-id="9102c-134">For more information about categorized tables, see [Sorting and Categorization](sorting-and-categorization.md).</span></span>
  
## <a name="notes-to-implementers"></a><span data-ttu-id="9102c-135">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="9102c-135">Notes to implementers</span></span>

<span data-ttu-id="9102c-136">Speichern Sie den aktuellen Status aller Knoten in einer Tabelle in der _LppbCollapseState_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="9102c-136">Store the current state of all nodes of a table in the  _lppbCollapseState_ parameter.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9102c-137">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="9102c-137">Notes to callers</span></span>

<span data-ttu-id="9102c-138">Rufen Sie immer **GetCollapseState** , bevor Sie **SetCollapseState**aufrufen.</span><span class="sxs-lookup"><span data-stu-id="9102c-138">Always call **GetCollapseState** before you call **SetCollapseState**.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9102c-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9102c-139">See also</span></span>



[<span data-ttu-id="9102c-140">IMAPITable::SetCollapseState</span><span class="sxs-lookup"><span data-stu-id="9102c-140">IMAPITable::SetCollapseState</span></span>](imapitable-setcollapsestate.md)
  
[<span data-ttu-id="9102c-141">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9102c-141">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

