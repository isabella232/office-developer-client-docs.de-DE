---
title: xlfEvaluate
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfEvaluate
keywords:
- xlfevaluate-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 527f7e932a41103c374e327a1bd0dd4c7d8e92a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439184"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Verwendet den Microsoft Excel parser und den Funktionsevaluator, um einen beliebigen Ausdruck auszuwerten, der in eine Arbeitsblattzelle eingegeben werden kann.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Parameter

 _pxFormulaText (xltypeStr)_
  
Die zu bewertende Zeichenfolge. Ein führendes Gleichheitszeichen (=) ist optional. Die Zeichenfolge kann ein beliebiger Text sein, der legal in eine Arbeitsblatt- oder Makroblattzelle eingegeben werden kann.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt das Ergebnis der Auswertung der Zeichenfolge zurück, die einen der Typen **xltypeNum**, **xltypeStr**, **xltypeBool**, **xltypeErr**, **xltypeNil**, **xltypeMulti** sein kann.
  
## <a name="remarks"></a>Hinweise

Die Zeichenfolge kann nur Funktionen und keine Befehlsäquivalente enthalten. Sie entspricht dem Drücken von **F9 aus** der Formelleiste. Wenn **xlfEvaluate** von einer XLL-Arbeitsblattfunktion aufgerufen wird, die als threadsicher registriert wurde, darf der Ausdruck nur threadsichere Funktionen enthalten. 
  
Die primäre Verwendung der **xlfEvaluate-Funktion** besteht in der Möglichkeit, DLLs das Aufschlüsseln des Werts zu ermöglichen, der einem definierten Namen zugewiesen ist, der sich entweder auf einem Blatt oder einem in der DLL definierten ausgeblendeten Namen befindet. Beachten Sie, dass einem Arbeitsblattnamen in einer DLL/XLL mindestens ein Ausrufezeichen (!) vorangestellt werden muss, um sicherzustellen, dass er als außerhalb der DLL interpretiert wird. Weitere Informationen finden Sie unter [Evaluating Names and Other Worksheet Formula Expressions](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **xlfEvaluate** kann nicht zum Auswerten von Verweisen auf ein externes Blatt verwendet werden, das nicht geöffnet ist. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel **wird xlfEvaluate** verwendet, um den Text "! B38" zum Inhalt der Zelle B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Diese Funktion ruft ein Befehlsmakro (**xlcAlert**) auf und funktioniert nur dann ordnungsgemäß, wenn sie von einem Makroblatt oder als Makrobefehl aufgerufen wird.
  
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

