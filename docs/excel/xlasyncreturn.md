---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e7ba37629ff2198339394448410ffd16477d4766
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790586"
---
# <a name="xlasyncreturn"></a><span data-ttu-id="56464-103">xlAsyncReturn</span><span class="sxs-lookup"><span data-stu-id="56464-103">xlAsyncReturn</span></span>

<span data-ttu-id="56464-104">**Gilt für**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="56464-104">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="56464-105">Wird verwendet, um das Ergebnis einer asynchronen benutzerdefinierte Funktion (UDF) zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="56464-105">Used to return the result of an asynchronous user-defined function (UDF).</span></span>
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a><span data-ttu-id="56464-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="56464-106">Parameters</span></span>

<span data-ttu-id="56464-107">_pxAsyncHandle_ (**XltypeBigData**)</span><span class="sxs-lookup"><span data-stu-id="56464-107">_pxAsyncHandle_ (**xltypeBigData**)</span></span>
  
<span data-ttu-id="56464-108">Die asynchrone Handle der UDF-Datei an die das Ergebnis zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="56464-108">The asynchronous handle of the UDF to which the result is returned.</span></span>
  
<span data-ttu-id="56464-109">_pxFunctionResult_</span><span class="sxs-lookup"><span data-stu-id="56464-109">_pxFunctionResult_</span></span>
  
<span data-ttu-id="56464-110">Der Rückgabewert der UDF-Datei.</span><span class="sxs-lookup"><span data-stu-id="56464-110">The return value of the UDF.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="56464-111">Eigenschaft Eigenschaftswert/Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="56464-111">Property value/Return value</span></span>

<span data-ttu-id="56464-112">Wenn erfolgreich ist, gibt **"true"** (**XltypeBool**).</span><span class="sxs-lookup"><span data-stu-id="56464-112">If successful, returns **TRUE** (**xltypeBool**).</span></span> <span data-ttu-id="56464-113">Wenn nicht erfolgreich ist, gibt **FALSE**zurück.</span><span class="sxs-lookup"><span data-stu-id="56464-113">If unsuccessful, returns **FALSE**.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="56464-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="56464-114">Remarks</span></span>

<span data-ttu-id="56464-115">**XlAsyncReturn** ist der einzige Rückruf Excel auf nicht-Berechnungsthreads während einer neuberechnung ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="56464-115">**xlAsyncReturn** is the only callback Excel allows on non-calculation threads during recalculation.</span></span> <span data-ttu-id="56464-116">Der asynchrone Teil einer asynchrones UDF muss keine Rückrufe als **XlAsyncReturn**ausführen.</span><span class="sxs-lookup"><span data-stu-id="56464-116">The asynchronous portion of an asynchronous UDF must not perform any callbacks other than **xlAsyncReturn**.</span></span> <span data-ttu-id="56464-117">XLL muss, um den Rückgabewert halten belegten Arbeitsspeicher freizugeben.</span><span class="sxs-lookup"><span data-stu-id="56464-117">The XLL must free memory allocated to hold the return value.</span></span>
  
<span data-ttu-id="56464-118">Der Typ **XltypeMulti** Wenn verwendet, um ein Array von Handles und die entsprechenden Werte in einem einzigen Rückruf zurückgegeben können auch die Parameter _PxAsyncHandle_ und _PxFunctionResult_ sein.</span><span class="sxs-lookup"><span data-stu-id="56464-118">The _pxAsyncHandle_ and  _pxFunctionResult_ parameters can also be of type **xltypeMulti** when used to return an array of handles and corresponding values in a single callback.</span></span> <span data-ttu-id="56464-119">Wenn Sie einen einzelnen Rückruf verwenden, übergeben Sie eine LPXLOPER12, die auf XLOPER12 Strukturen verweist, die eine dimensionale Arrays enthalten, die Rückgabewerte und enthalten die asynchronen werden.</span><span class="sxs-lookup"><span data-stu-id="56464-119">When using a single callback, pass an LPXLOPER12 that points to XLOPER12 structures that contain one dimensional arrays that contain the asynchronous handles and return values.</span></span> <span data-ttu-id="56464-120">Diese Arrays muss in der gleichen Reihenfolge für Excel ordnungsgemäß ein asynchrones Handle mit den entsprechenden Wert übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="56464-120">These arrays must be in the same order for Excel to correctly match an asynchronous handle with its corresponding value.</span></span> 
  
<span data-ttu-id="56464-121">Das folgende Beispiel zeigt, wie Sie einen Batch Anrufen über **XlAsyncReturn**machen können.</span><span class="sxs-lookup"><span data-stu-id="56464-121">The following example shows how you can make a batch call using **xlAsyncReturn**.</span></span>
  
```cpp
int batchSize = 10;
    LPXLOPER12 pHandles = new XLOPER12[batchSize];
    LPXLOPER12 pValues = new XLOPER12[batchSize];
    /*Add code to fill in LPXLOPER12 arrays (pHandles and pValues)
    with the XOPER12 structures that contain the asynchronous handles
    and values, in respective order*/
    //Create an XLOPER12 of type xltypeMulti, and fill the Handle array
    XLOPER12 handleArray;
    handleArray.xltype = xltypeMulti;
    handleArray.val.array.rows = 1;
    handleArray.val.array.columns = (COL)batchSize;
    handleArray.val.array.lparray = pHandles;
    
    //Create an XLOPER12 if type xltypeMulti, and fill the Values array
    XLOPER12 valueArray;
    valueArray.xltype = xltypeMulti;
    valueArray.val.array.rows = 1;
    valueArray.val.array.columns = (COL)batchSize;
    valueArray.val.array.lparray = pValues;
    //Make the callback with the return value
    int ret = Excel12(xlAsyncReturn, 0, 2, &amp;handleArray, &amp;valueArray);
    //Add code to free the allocated memory here (pHandles, pValues, valueArray, handleArray)
    return ret;

```

## <a name="see-also"></a><span data-ttu-id="56464-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56464-122">See also</span></span>

- [<span data-ttu-id="56464-123">Asynchrone benutzerdefinierte Funktionen</span><span class="sxs-lookup"><span data-stu-id="56464-123">Asynchronous User-Defined Functions</span></span>](asynchronous-user-defined-functions.md)
