---
title: IMAPITableQueryPosition
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPITable.QueryPosition
api_type:
- COM
ms.assetid: 510b2e21-ba27-47dd-87cb-2a549e31fa28
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 502bc24ece37c91e2cac23cf8486df96d5a71377
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584338"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="4696e-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="4696e-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="4696e-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4696e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4696e-105">Ruft die aktuelle Tabelle Zeilenposition des Cursors, basierend auf einem Bruch Wert.</span><span class="sxs-lookup"><span data-stu-id="4696e-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="4696e-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4696e-106">Parameters</span></span>

 <span data-ttu-id="4696e-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="4696e-107">_lpulRow_</span></span>
  
> <span data-ttu-id="4696e-108">[out] Zeiger auf die Anzahl der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="4696e-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="4696e-109">Die Zeilennummer ist nullbasiert. die erste Zeile in der Tabelle ist 0 (null).</span><span class="sxs-lookup"><span data-stu-id="4696e-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="4696e-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="4696e-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="4696e-111">[out] Zeiger auf die Zähler für den Bruch, die die Position der Tabelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4696e-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="4696e-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="4696e-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="4696e-113">[out] Zeiger auf die als Nenner für den Bruch, die die Position der Tabelle identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4696e-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="4696e-114">Der Parameter _LpulDenominator_ darf nicht NULL sein.</span><span class="sxs-lookup"><span data-stu-id="4696e-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4696e-115">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="4696e-115">Return value</span></span>

<span data-ttu-id="4696e-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="4696e-116">S_OK</span></span> 
  
> <span data-ttu-id="4696e-117">Die Methode, die gültige Werte in _LpulRow_, _LpulNumerator_und _LpulDenominator_zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4696e-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4696e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4696e-118">Remarks</span></span>

<span data-ttu-id="4696e-119">Die **IMAPITable::QueryPosition** -Methode die aktuelle Zeilenposition bestimmt und sowohl die Anzahl der aktuellen Zeile und eine anteilige Wert, der angibt, der der relativen Position am Ende der Tabelle zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4696e-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="4696e-120">MAPI definiert die aktuelle Zeile als die nächste Zeile gelesen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4696e-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="4696e-121">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="4696e-121">Notes to implementers</span></span>

<span data-ttu-id="4696e-122">Sie müssen nicht die genaue Anzahl der Zeilen in der Tabelle für den Parameter _LpulDenominator_ zurückgegeben. Es kann eine Annäherung sein.</span><span class="sxs-lookup"><span data-stu-id="4696e-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="4696e-123">Wenn Sie die aktuelle Zeile nicht ermitteln können, einen Wert 0xFFFFFFFF in _LpulRow_zurück.</span><span class="sxs-lookup"><span data-stu-id="4696e-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="4696e-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="4696e-124">Notes to callers</span></span>

<span data-ttu-id="4696e-125">**QueryPosition** können Sie um das Bildlauffeld in einer Bildlaufleiste zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="4696e-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="4696e-126">Beispielsweise in einer Tabelle mit 100 Zeilen **QueryPosition** in den _LpulNumerator_ -Parameter im Parameter _LpulDenominator_ 100 und 75 in den _LpulRow_ -Parameter einen Wert von 75 zurück können Sie die Scroll Feld 3/4 der positionieren die Möglichkeit, über die Bildlaufleiste.</span><span class="sxs-lookup"><span data-stu-id="4696e-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="4696e-127">Verlassen Sie sich nicht auf dem Wert im _LpulDenominator_ wird die Anzahl der Zeilen in der Tabelle.</span><span class="sxs-lookup"><span data-stu-id="4696e-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="4696e-128">**QueryPosition** kann nicht immer die genaue Zeile identifizieren, der auf dem sich der Cursor befindet.</span><span class="sxs-lookup"><span data-stu-id="4696e-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="4696e-129">Ein Aufruf von **QueryPosition** möglicherweise große Mengen von Arbeitsspeicher, besonders für große kategorisierten Tabellen umfassen.</span><span class="sxs-lookup"><span data-stu-id="4696e-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="4696e-130">Wenn der Parameter _LpulRow_ auf 0xFFFFFFFF festgelegt ist, wurde zu viel Speicher für **QueryPosition** zum Bestimmen der aktuellen Zeile erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4696e-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="4696e-131">Rufen Sie die [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) -Methode, um die position der Tabelle auf die Zeile, die durch die Parameter _LpulNumerator_ und _LpulDenominator_ identifiziert.</span><span class="sxs-lookup"><span data-stu-id="4696e-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="4696e-132">Jedoch immer erwarten Sie keine **SeekRowApprox** , wie die aktuelle Position die gleiche Zeile herzustellen, die Wenn Speicher keinen Faktor hätte **QueryPosition** hätten.</span><span class="sxs-lookup"><span data-stu-id="4696e-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4696e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4696e-133">See also</span></span>



[<span data-ttu-id="4696e-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="4696e-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="4696e-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="4696e-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

