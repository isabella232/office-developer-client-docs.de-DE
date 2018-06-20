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
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um das Ergebnis einer asynchronen benutzerdefinierte Funktion (UDF) zurückzugeben.
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parameter

_pxAsyncHandle_ (**XltypeBigData**)
  
Die asynchrone Handle der UDF-Datei an die das Ergebnis zurückgegeben wird.
  
_pxFunctionResult_
  
Der Rückgabewert der UDF-Datei.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Wenn erfolgreich ist, gibt **"true"** (**XltypeBool**). Wenn nicht erfolgreich ist, gibt **FALSE**zurück.
  
## <a name="remarks"></a>Hinweise

**XlAsyncReturn** ist der einzige Rückruf Excel auf nicht-Berechnungsthreads während einer neuberechnung ermöglicht. Der asynchrone Teil einer asynchrones UDF muss keine Rückrufe als **XlAsyncReturn**ausführen. XLL muss, um den Rückgabewert halten belegten Arbeitsspeicher freizugeben.
  
Der Typ **XltypeMulti** Wenn verwendet, um ein Array von Handles und die entsprechenden Werte in einem einzigen Rückruf zurückgegeben können auch die Parameter _PxAsyncHandle_ und _PxFunctionResult_ sein. Wenn Sie einen einzelnen Rückruf verwenden, übergeben Sie eine LPXLOPER12, die auf XLOPER12 Strukturen verweist, die eine dimensionale Arrays enthalten, die Rückgabewerte und enthalten die asynchronen werden. Diese Arrays muss in der gleichen Reihenfolge für Excel ordnungsgemäß ein asynchrones Handle mit den entsprechenden Wert übereinstimmen. 
  
Das folgende Beispiel zeigt, wie Sie einen Batch Anrufen über **XlAsyncReturn**machen können.
  
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

## <a name="see-also"></a>Siehe auch

- [Asynchrone benutzerdefinierte Funktionen](asynchronous-user-defined-functions.md)

