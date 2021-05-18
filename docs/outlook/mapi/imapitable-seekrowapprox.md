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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: bbb79097d03a8ea09cb4aff374231ee780e15395
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412149"
---
# <a name="imapitableseekrowapprox"></a><span data-ttu-id="b0133-103">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="b0133-103">IMAPITable::SeekRowApprox</span></span>

  
  
<span data-ttu-id="b0133-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0133-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0133-105">Verschiebt den Cursor an eine ungefähre Bruchposition in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b0133-105">Moves the cursor to an approximate fractional position in the table.</span></span> 
  
```cpp
HRESULT SeekRowApprox(
ULONG ulNumerator,
ULONG ulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="b0133-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b0133-106">Parameters</span></span>

 <span data-ttu-id="b0133-107">_ulNumerator_</span><span class="sxs-lookup"><span data-stu-id="b0133-107">_ulNumerator_</span></span>
  
> <span data-ttu-id="b0133-108">[in] Zeiger auf den Zähler der Bruchzahl, die die Tabellenposition darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0133-108">[in] Pointer to the numerator of the fraction representing the table position.</span></span> <span data-ttu-id="b0133-109">Wenn der  _ulNumerator-Parameter_ null ist, wird der Cursor unabhängig vom Nennwert am Anfang der Tabelle positioniert.</span><span class="sxs-lookup"><span data-stu-id="b0133-109">If the  _ulNumerator_ parameter is zero, the cursor is positioned at the beginning of the table regardless of the denominator value.</span></span> <span data-ttu-id="b0133-110">Wenn  _ulNumerator_ gleich dem  _ulDenominator-Parameter_ ist, wird der Cursor hinter der letzten Tabellenzeile positioniert.</span><span class="sxs-lookup"><span data-stu-id="b0133-110">If  _ulNumerator_ is equal to the  _ulDenominator_ parameter, the cursor is positioned after the last table row.</span></span> 
    
 <span data-ttu-id="b0133-111">_ulDenominator_</span><span class="sxs-lookup"><span data-stu-id="b0133-111">_ulDenominator_</span></span>
  
> <span data-ttu-id="b0133-112">[in] Zeiger auf den Nenner der Bruchzahl, die die Tabellenposition darstellt.</span><span class="sxs-lookup"><span data-stu-id="b0133-112">[in] Pointer to the denominator of the fraction representing the table position.</span></span> <span data-ttu-id="b0133-113">Der  _ulDenominator-Parameter_ darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="b0133-113">The  _ulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b0133-114">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="b0133-114">Return value</span></span>

<span data-ttu-id="b0133-115">S_OK</span><span class="sxs-lookup"><span data-stu-id="b0133-115">S_OK</span></span> 
  
> <span data-ttu-id="b0133-116">Der Suchvorgang war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="b0133-116">The seek operation was successful.</span></span>
    
<span data-ttu-id="b0133-117">MAPI_E_BUSY</span><span class="sxs-lookup"><span data-stu-id="b0133-117">MAPI_E_BUSY</span></span> 
  
> <span data-ttu-id="b0133-118">Ein weiterer Vorgang wird ausgeführt, der verhindert, dass der Zeilensuchenvorgang gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="b0133-118">Another operation is in progress that prevents the row seeking operation from starting.</span></span> <span data-ttu-id="b0133-119">Der ausgeführte Vorgang sollte entweder abgeschlossen oder beendet werden.</span><span class="sxs-lookup"><span data-stu-id="b0133-119">Either the operation in progress should be allowed to complete or it should be stopped.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b0133-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b0133-120">Remarks</span></span>

<span data-ttu-id="b0133-121">Die Cursorposition in einer Tabelle nach einem Aufruf der **IMAPITable::SeekRowApprox-Methode** ist heuristisch der Bruch und möglicherweise nicht exakt.</span><span class="sxs-lookup"><span data-stu-id="b0133-121">The cursor position in a table after a call to the **IMAPITable::SeekRowApprox** method is heuristically the fraction and might not be exact.</span></span> <span data-ttu-id="b0133-122">Beispielsweise können bestimmte Anbieter eine Tabelle über einer binären Struktur implementieren und den Tabellenhalbpunkt aus Leistungsgründen als oberster Punkt der Struktur behandeln.</span><span class="sxs-lookup"><span data-stu-id="b0133-122">For example, certain providers might implement a table on top of a binary tree, treating the table's halfway point as the top of the tree for performance reasons.</span></span> <span data-ttu-id="b0133-123">Wenn die Struktur nicht ausgeglichen ist, ist der verwendete Halbzeitpunkt möglicherweise nicht genau in der Mitte der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b0133-123">If the tree is not balanced, then the halfway point used might not be exactly halfway through the table.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b0133-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="b0133-124">Notes to callers</span></span>

<span data-ttu-id="b0133-125">Rufen **Sie SeekRowApprox** auf, um die Daten für eine Bildlaufleistenimplementierung zur Verfügung zu stellen.</span><span class="sxs-lookup"><span data-stu-id="b0133-125">Call **SeekRowApprox** to provide the data for a scroll bar implementation.</span></span> <span data-ttu-id="b0133-126">Wenn der Benutzer beispielsweise das Bildlauffeld 2/3 unten auf der Bildlaufleiste positioniert, können Sie diese Aktion modellieren, indem Sie **SeekRowApprox** aufrufen und einen entsprechenden Bruchwert mithilfe von _ulNumerator_ und _ulDenominator übergeben._</span><span class="sxs-lookup"><span data-stu-id="b0133-126">For example, if the user positions the scroll box 2/3 down the scroll bar, you can model that action by calling **SeekRowApprox** and passing in an equivalent fractional value using  _ulNumerator_ and  _ulDenominator_.</span></span> <span data-ttu-id="b0133-127">Die **SeekRowApprox-Suche** ist immer vom Anfang der Tabelle aus absolut.</span><span class="sxs-lookup"><span data-stu-id="b0133-127">The **SeekRowApprox** search is always absolute from the beginning of the table.</span></span> <span data-ttu-id="b0133-128">Um an das Ende der Tabelle zu wechseln, müssen die Werte in  _ulNumerator_ und  _ulDenominator_ identisch sein.</span><span class="sxs-lookup"><span data-stu-id="b0133-128">To move to the end of the table, the values in  _ulNumerator_ and  _ulDenominator_ must be the same.</span></span> 
  
<span data-ttu-id="b0133-129">Verwenden Sie das entsprechende Nummernschema.</span><span class="sxs-lookup"><span data-stu-id="b0133-129">Use whatever number scheme is appropriate.</span></span> <span data-ttu-id="b0133-130">Das heißt, sie können 1/2, 10/20 oder 50/100 angeben, um eine Position in der Mitte der Tabelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="b0133-130">That is, to seek to a position halfway through the table, you can specify 1/2, 10/20, or 50/100.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b0133-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b0133-131">See also</span></span>



[<span data-ttu-id="b0133-132">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b0133-132">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

