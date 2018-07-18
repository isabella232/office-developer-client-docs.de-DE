---
title: IMAPITableSeekRowApprox
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.SeekRowApprox
api_type:
- COM
ms.assetid: ce5e8c43-06af-4afc-9138-5cc51d8fc401
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 12b0c9b40c7ff06e9a3cf8e7929489f30434fa12
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792486"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="ca33d-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="ca33d-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="ca33d-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca33d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca33d-105">Verschiebt den Cursor an eine ungefähre Bruch Position in der Tabelle an.</span><span class="sxs-lookup"><span data-stu-id="ca33d-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="ca33d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ca33d-106">Parameters</span></span>

 <span data-ttu-id="ca33d-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="ca33d-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="ca33d-108">[in] Zeiger auf die Zähler des Bruchs, die die Position der Tabelle darstellen.</span><span class="sxs-lookup"><span data-stu-id="ca33d-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="ca33d-109">Wenn der Parameter _UlNumerator_ gleich NULL ist, wird der Cursor am Anfang der Tabelle ungeachtet des Werts Nenner positioniert.</span><span class="sxs-lookup"><span data-stu-id="ca33d-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="ca33d-110">Wenn _UlNumerator_ gleich dem _UlDenominator_ -Parameter ist, wird der Cursor nach der letzten Tabellenzeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="ca33d-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="ca33d-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="ca33d-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="ca33d-112">[in] Zeiger auf die als Nenner des Bruchs, die die Position der Tabelle darstellen.</span><span class="sxs-lookup"><span data-stu-id="ca33d-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="ca33d-113">Der Parameter _UlDenominator_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="ca33d-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="ca33d-114">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="ca33d-114">Return value</span></span>

<span data-ttu-id="ca33d-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="ca33d-115">S_OK</span></span> 
  
> <span data-ttu-id="ca33d-116">Der Suchvorgang erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="ca33d-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="ca33d-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="ca33d-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="ca33d-118">Ein anderer Vorgang wird ausgeführt, die verhindert, die Zeile Suchvorgänge Vorgang dass gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="ca33d-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="ca33d-119">Entweder dürfen der Vorgang in Arbeit abgeschlossen oder angehalten werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ca33d-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ca33d-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca33d-120">Remarks</span></span>

<span data-ttu-id="ca33d-121">Die Cursorposition in einer Tabelle nach dem Aufruf **der SeekRowApprox** ist heuristisch den Bruch und möglicherweise nicht genau.</span><span class="sxs-lookup"><span data-stu-id="ca33d-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="ca33d-122">Bestimmte Anbieter können beispielsweise eine Tabelle auf der Basis einer binären Struktur, implementieren, zeigen Sie in der Mitte der Tabelle als im oberen Bereich der Struktur aus Gründen der Systemleistung behandelt.</span><span class="sxs-lookup"><span data-stu-id="ca33d-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="ca33d-123">Wenn die Struktur nicht ausgeglichen ist, klicken Sie dann in der Mitte Punkts verwendet genau durch die Tabelle in der Mitte möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="ca33d-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="ca33d-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="ca33d-124">Notes to callers</span></span>

<span data-ttu-id="ca33d-125">Rufen Sie **SeekRowApprox** , um die Daten für die Implementierung eines Scroll-Leiste bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ca33d-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="ca33d-126">Wenn der Benutzer die Bildlaufleiste Feld 2/3 nach unten die Bildlaufleiste positioniert, können Sie beispielsweise diese Aktion modellieren, durch Aufrufen von **SeekRowApprox** und einen entsprechenden Bruch Wert mithilfe von _UlNumerator_ und _UlDenominator_übergeben.</span><span class="sxs-lookup"><span data-stu-id="ca33d-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="ca33d-127">Die **SeekRowApprox** Suche ist immer absolute vom Beginn der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="ca33d-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="ca33d-128">Um am Ende der Tabelle zu verschieben, müssen die Werte in _UlNumerator_ und _UlDenominator_ identisch sein.</span><span class="sxs-lookup"><span data-stu-id="ca33d-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="ca33d-129">Verwenden Sie aufbauen Nummerierungsschema geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="ca33d-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="ca33d-130">Um eine Position in der Mitte durch die Tabelle gesucht, können Sie d. h., 1/2, 10/20 oder 50/100 angeben.</span><span class="sxs-lookup"><span data-stu-id="ca33d-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ca33d-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ca33d-131">See also</span></span>



[<span data-ttu-id="ca33d-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ca33d-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

