---
title: xlAsyncReturn
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 159bc9bf-8dd5-4cd2-8384-474c74a3f112
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 36560fc0362654a209f87feb74e548cd5b68f809
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59596806"
---
# <a name="xlasyncreturn"></a>xlAsyncReturn

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird verwendet, um das Ergebnis einer asynchronen benutzerdefinierten Funktion (UDF) zurückzugeben.
  
```cpp
Excel12(xlAsyncReturn, LPXLOPER12 pxRes, 2, LPXLOPER12 pxAsyncHandle, LPXLOPER12 pxFunctionResult);
```

## <a name="parameters"></a>Parameter

_pxAsyncHandle_ (**xltypeDigData**)
  
Das asynchrone Handle der UDF, an die das Ergebnis zurückgegeben wird.
  
_pxFunctionResult_
  
Der Rückgabewert der UDF.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn erfolgreich, **gibt TRUE** (**xltypeBool**). Wenn dies nicht erfolgreich ist, wird **FALSE zurückgegeben.**
  
## <a name="remarks"></a>HinwBemerkungeneise

**xlAsyncReturn** ist der einzige Rückruf Excel der nicht berechnungsbezogene Threads während der Neuberechnung zulässt. Der asynchrone Teil einer asynchronen UDF darf keine anderen Rückrufe als **xlAsyncReturn** ausführen. Die XLL muss Speicher freigeben, der für den Rückgabewert reserviert ist.
  
Die Parameter _pxAsyncHandle_ und  _pxFunctionResult_ können auch vom Typ **xltypeMulti** sein, wenn sie verwendet werden, um ein Array von Handles und entsprechenden Werten in einem einzelnen Rückruf zurückzugeben. Übergeben Sie bei Verwendung eines einzelnen Rückrufs einen LPXLOPER12-Wert, der auf XLOPER12-Strukturen zeigt, die eindimensionale Arrays enthalten, die die asynchronen Handles und Rückgabewerte enthalten. Diese Arrays müssen in derselben Reihenfolge angeordnet sein, damit Excel ein asynchrones Handle korrekt mit dem entsprechenden Wert abgleichen können. 
  
Das folgende Beispiel zeigt, wie Sie einen Batchaufruf mit **xlAsyncReturn** ausführen können.
  
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

