---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310248"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um das Ergebnis einer asynchronen benutzerdefinierten Funktion (UDF) zurückzugeben.
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parameter

_pxAsyncHandle_ (**xltypeBigData**)
  
Der asynchrone Handle des UDF, an das das Ergebnis zurückgegeben wird.
  
_pxFunctionResult_
  
Der Rückgabewert des UDF.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn der Wert erfolgreich ist, wird **true** (**xltypeBool**) zurückgegeben. Wenn nicht erfolgreich, gibt **false**zurück.
  
## <a name="remarks"></a>Bemerkungen

**xlAsyncReturn** ist der einzige Rückruf, den Excel für nicht-Berechnungs-Threads während der Neuberechnung ermöglicht. Der asynchrone Teil einer asynchronen UDF darf keine Rückrufe außer **xlAsyncReturn**durchführen. Die XLL muss Arbeitsspeicher freigeben, der für den Rückgabewert reserviert ist.
  
Die Parameter _pxAsyncHandle_ und _pxFunctionResult_ können auch vom Typ **xltypeMulti** sein, wenn Sie verwendet werden, um ein Array von Handles und entsprechenden Werten in einem einzelnen Rückruf zurückzugeben. Wenn Sie einen einzelnen Rückruf verwenden, übergeben Sie ein LPXLOPER12, das auf XLOPER12-Strukturen verweist, die eindimensionale Arrays enthalten, die die asynchronen Handles und Rückgabewerte enthalten. Diese Arrays müssen in der gleichen Reihenfolge für Excel ordnungsgemäß mit einem asynchronen Handle mit dem entsprechenden Wert übereinstimmen. 
  
Das folgende Beispiel zeigt, wie Sie einen Batch Aufruf mit **xlAsyncReturn**durchführen können.
  
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

