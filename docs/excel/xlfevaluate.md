---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- Xlfevaluate-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 06526e4cf699cc24fd2cbc9d4cf54d6a018f9d99
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557596"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Verwendet den Microsoft Excel Parser und den Funktionsauswertungsmodul, um einen beliebigen Ausdruck auszuwerten, der in eine Arbeitsblattzelle eingegeben werden kann.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Parameter

 _pxFormulaText (xltypeStr)_
  
Die zu bewertende Zeichenfolge. Ein führendes Gleichheitszeichen (=) ist optional. Die Zeichenfolge kann ein beliebiger Text sein, der gesetzlich in ein Arbeitsblatt oder eine Makroblattzelle eingegeben werden kann.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt das Ergebnis der Auswertung der Zeichenfolge zurück, die einen der Typen **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti** sein kann.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Zeichenfolge darf nur Funktionen und keine Befehlsentsprechungen enthalten. Dies entspricht dem Drücken von **F9** aus der Bearbeitungsleiste. Wenn **xlfEvaluate** von einer XLL-Arbeitsblattfunktion aufgerufen wird, die als threadsicher registriert wurde, darf der Ausdruck nur threadsichere Funktionen enthalten. 
  
Die primäre Verwendung der **xlfEvaluate-Funktion** besteht darin, DLLs das Ermitteln des Werts zu ermöglichen, der einem definierten Namen zugewiesen ist, der sich entweder in einem Blatt befindet, oder einem ausgeblendeten Namen, der in der DLL definiert ist. Beachten Sie, dass einem Arbeitsblattnamen innerhalb einer DLL/XLL mindestens ein Ausrufezeichen (!) vorangestellt werden muss, um sicherzustellen, dass er als extern für die DLL interpretiert wird. Weitere Informationen finden Sie unter [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** kann nicht verwendet werden, um Verweise auf ein nicht geöffnetes externes Blatt auszuwerten. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird **xlfEvaluate** verwendet, um den Text "! B38" bis zum Inhalt der Zelle B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Diese Funktion ruft ein Befehlsmakro (**xlcAlert**) auf und funktioniert nur ordnungsgemäß, wenn es von einem Makroblatt oder als Makrobefehl aufgerufen wird.
  
```cs
short WINAPI EvaluateExample(void)
{
    XLOPER12 xFormulaText, xRes, xRes2, xInt;
    xFormulaText.xltype = xltypeStr;
    xFormulaText.val.str = L"\004!B38";
    Excel12(xlfEvaluate, &xRes, 1, (LPXLOPER12)&xFormulaText);
    xInt.xltype = xltypeInt;
    xInt.val.w = 2;
    Excel12(xlcAlert, &xRes2, 2, (LPXLOPER12)&xRes, (LPXLOPER12)&xInt);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
    Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes2);
    return 1;
}
```

## <a name="see-also"></a>Siehe auch

- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

