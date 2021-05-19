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
ms.openlocfilehash: 2e44d824bbb5cc96c51d7ca91eb639001bc52a71
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415663"
---
# <a name="imapitablequeryposition"></a><span data-ttu-id="e43f9-103">IMAPITable::QueryPosition</span><span class="sxs-lookup"><span data-stu-id="e43f9-103">IMAPITable::QueryPosition</span></span>

  
  
<span data-ttu-id="e43f9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e43f9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e43f9-105">Ruft die aktuelle Tabellenzeile des Cursors basierend auf einem Bruchwert ab.</span><span class="sxs-lookup"><span data-stu-id="e43f9-105">Retrieves the current table row position of the cursor, based on a fractional value.</span></span>
  
```cpp
HRESULT QueryPosition(
ULONG FAR * lpulRow,
ULONG FAR * lpulNumerator,
ULONG FAR * lpulDenominator
);
```

## <a name="parameters"></a><span data-ttu-id="e43f9-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="e43f9-106">Parameters</span></span>

 <span data-ttu-id="e43f9-107">_lpulRow_</span><span class="sxs-lookup"><span data-stu-id="e43f9-107">_lpulRow_</span></span>
  
> <span data-ttu-id="e43f9-108">[out] Zeiger auf die Nummer der aktuellen Zeile.</span><span class="sxs-lookup"><span data-stu-id="e43f9-108">[out] Pointer to the number of the current row.</span></span> <span data-ttu-id="e43f9-109">Die Zeilennummer ist nullbasierter Wert. Die erste Zeile in der Tabelle ist Null.</span><span class="sxs-lookup"><span data-stu-id="e43f9-109">The row number is zero-based; the first row in the table is zero.</span></span> 
    
 <span data-ttu-id="e43f9-110">_lpulNumerator_</span><span class="sxs-lookup"><span data-stu-id="e43f9-110">_lpulNumerator_</span></span>
  
> <span data-ttu-id="e43f9-111">[out] Zeiger auf den Zähler für den Bruch, der die Tabellenposition identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e43f9-111">[out] Pointer to the numerator for the fraction identifying the table position.</span></span>
    
 <span data-ttu-id="e43f9-112">_lpulDenominator_</span><span class="sxs-lookup"><span data-stu-id="e43f9-112">_lpulDenominator_</span></span>
  
> <span data-ttu-id="e43f9-113">[out] Zeiger auf den Nenner für den Bruch, der die Tabellenposition identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e43f9-113">[out] Pointer to the denominator for the fraction identifying the table position.</span></span> <span data-ttu-id="e43f9-114">Der  _lpulDenominator-Parameter_ darf nicht null sein.</span><span class="sxs-lookup"><span data-stu-id="e43f9-114">The  _lpulDenominator_ parameter cannot be zero.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="e43f9-115">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e43f9-115">Return value</span></span>

<span data-ttu-id="e43f9-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e43f9-116">S_OK</span></span> 
  
> <span data-ttu-id="e43f9-117">Die Methode hat gültige Werte in _lpulRow,_ _lpulNumerator_ und _lpulDenominator zurückgegeben._</span><span class="sxs-lookup"><span data-stu-id="e43f9-117">The method returned valid values in  _lpulRow_,  _lpulNumerator_, and  _lpulDenominator_.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e43f9-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e43f9-118">Remarks</span></span>

<span data-ttu-id="e43f9-119">Die **IMAPITable::QueryPosition-Methode** bestimmt die aktuelle Zeilenposition und gibt sowohl die Nummer der aktuellen Zeile als auch einen Bruchwert zurück, der die relative Position am Ende der Tabelle angibt.</span><span class="sxs-lookup"><span data-stu-id="e43f9-119">The **IMAPITable::QueryPosition** method determines the current row position and returns both the number of the current row and a fractional value indicating its relative position to the end of the table.</span></span> <span data-ttu-id="e43f9-120">MAPI definiert die aktuelle Zeile als die nächste zu lesende Zeile.</span><span class="sxs-lookup"><span data-stu-id="e43f9-120">MAPI defines the current row as the next row to be read.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="e43f9-121">Hinweise für Implementierer</span><span class="sxs-lookup"><span data-stu-id="e43f9-121">Notes to implementers</span></span>

<span data-ttu-id="e43f9-122">Sie müssen nicht die genaue Anzahl der Zeilen in der Tabelle für den  _lpulDenominator-Parameter zurückgeben._ Dies kann eine Näherung sein.</span><span class="sxs-lookup"><span data-stu-id="e43f9-122">You do not need to return the exact number of rows in the table for the  _lpulDenominator_ parameter; it can be an approximation.</span></span> 
  
<span data-ttu-id="e43f9-123">Wenn Sie die aktuelle Zeile nicht ermitteln können, geben Sie den Wert 0xFFFFFFFF in _lpulRow zurück._</span><span class="sxs-lookup"><span data-stu-id="e43f9-123">If you cannot determine the current row, return a value of 0xFFFFFFFF in  _lpulRow_.</span></span>
  
## <a name="notes-to-callers"></a><span data-ttu-id="e43f9-124">Hinweise für Aufrufer</span><span class="sxs-lookup"><span data-stu-id="e43f9-124">Notes to callers</span></span>

<span data-ttu-id="e43f9-125">Sie können **QueryPosition verwenden,** um ein Bildlauffeld in einer Bildlaufleiste zu positionieren.</span><span class="sxs-lookup"><span data-stu-id="e43f9-125">You can use **QueryPosition** to position a scroll box in a scroll bar.</span></span> <span data-ttu-id="e43f9-126">Wenn **QueryPosition** beispielsweise in einer Tabelle mit 100 Zeilen den Wert 75 im  _lpulNumerator-Parameter,_ 100 im  _lpulDenominator-Parameter_ und 75 im  _lpulRow-Parameter_ zurückgibt, können Sie das Bildlauffeld 3/4 des Wegs über die Bildlaufleiste positionieren.</span><span class="sxs-lookup"><span data-stu-id="e43f9-126">For example, in a table containing 100 rows, if **QueryPosition** returns a value of 75 in the  _lpulNumerator_ parameter, 100 in the  _lpulDenominator_ parameter, and 75 in the  _lpulRow_ parameter, you can position the scroll box 3/4 of the way across the scroll bar.</span></span> 
  
<span data-ttu-id="e43f9-127">Verlassen Sie sich nicht darauf, dass der Wert in  _lpulDenominator_ die Anzahl der Zeilen in der Tabelle ist.</span><span class="sxs-lookup"><span data-stu-id="e43f9-127">Do not rely on the value in  _lpulDenominator_ being the number of rows in the table.</span></span> <span data-ttu-id="e43f9-128">**QueryPosition** kann nicht immer die genaue Zeile identifizieren, in der der Cursor positioniert ist.</span><span class="sxs-lookup"><span data-stu-id="e43f9-128">**QueryPosition** cannot always identify the exact row that the cursor is positioned on.</span></span> 
  
<span data-ttu-id="e43f9-129">Ein Aufruf von **QueryPosition** kann große Mengen an Arbeitsspeicher umfassen, insbesondere für große kategorisierte Tabellen.</span><span class="sxs-lookup"><span data-stu-id="e43f9-129">A call to **QueryPosition** might involve large amounts of memory, particularly for large categorized tables.</span></span> <span data-ttu-id="e43f9-130">Wenn der  _lpulRow-Parameter_ auf 0xFFFFFFFF festgelegt ist, war zu viel Arbeitsspeicher für **QueryPosition** erforderlich, um die aktuelle Zeile zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="e43f9-130">If the  _lpulRow_ parameter is set to 0xFFFFFFFF, too much memory was required for **QueryPosition** to determine the current row.</span></span> <span data-ttu-id="e43f9-131">Rufen Sie [die IMAPITable::SeekRowApprox-Methode](imapitable-seekrowapprox.md) auf, um die Tabelle in der Zeile zu positionieren, die durch die  _Parameter lpulNumerator_ und  _lpulDenominator identifiziert_ wird.</span><span class="sxs-lookup"><span data-stu-id="e43f9-131">Call the [IMAPITable::SeekRowApprox](imapitable-seekrowapprox.md) method to position the table to the row identified by the  _lpulNumerator_ and  _lpulDenominator_ parameters.</span></span> <span data-ttu-id="e43f9-132">Gehen Sie jedoch nicht immer davon aus, dass **SeekRowApprox** als aktuelle Position dieselbe Zeile wie **QueryPosition** festlegen würde, wenn der Arbeitsspeicher kein Faktor gewesen wäre.</span><span class="sxs-lookup"><span data-stu-id="e43f9-132">However, do not always expect **SeekRowApprox** to establish as the current position the same row **QueryPosition** would have if memory had not been a factor.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e43f9-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e43f9-133">See also</span></span>



[<span data-ttu-id="e43f9-134">IMAPITable::SeekRowApprox</span><span class="sxs-lookup"><span data-stu-id="e43f9-134">IMAPITable::SeekRowApprox</span></span>](imapitable-seekrowapprox.md)
  
[<span data-ttu-id="e43f9-135">IMAPITable : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e43f9-135">IMAPITable : IUnknown</span></span>](imapitableiunknown.md)

