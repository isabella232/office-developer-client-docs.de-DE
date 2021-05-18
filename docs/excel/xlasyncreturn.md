---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 32d5075af34cda9753c5d082bd4ab00afab1ecff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414109"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um das Ergebnis einer asynchronen benutzerdefinierten Funktion (User-Defined Function, UDF) zurück zu geben.
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parameter

_pxAsyncHandle_ (**xltypeBigData**)
  
Das asynchrone Handle der UDF, an die das Ergebnis zurückgegeben wird.
  
_pxFunctionResult_
  
Der Rückgabewert der UDF.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn dies erfolgreich ist, wird **TRUE** (**xltypeBool**) zurückgegeben. Wenn der Wert nicht erfolgreich ist, wird **FALSE zurückgegeben.**
  
## <a name="remarks"></a>Hinweise

**xlAsyncReturn** ist der einzige Rückruf, Excel nicht berechnungsfreie Threads während der Neuberechnung zulässt. Der asynchrone Teil einer asynchronen UDF darf keine anderen Rückrufe als **xlAsyncReturn ausführen.** Die XLL muss speicherplatz frei, der für den Rückgabewert reserviert ist.
  
Die _Parameter pxAsyncHandle_ und  _pxFunctionResult_ können auch vom Typ **xltypeMulti** sein, wenn sie zum Zurückgeben eines Arrays von Handles und entsprechenden Werten in einem einzelnen Rückruf verwendet werden. Übergeben Sie bei Verwendung eines einzelnen Rückrufs eine LPXLOPER12, die auf XLOPER12-Strukturen verweist, die eindimensionale Arrays enthalten, die die asynchronen Ziehpunkte und Rückgabewerte enthalten. Diese Arrays müssen sich in derselben Reihenfolge befinden, Excel einem asynchronen Handle mit dem entsprechenden Wert korrekt entspricht. 
  
Das folgende Beispiel zeigt, wie Sie einen Batchaufruf mit **xlAsyncReturn erstellen können.**
  
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

