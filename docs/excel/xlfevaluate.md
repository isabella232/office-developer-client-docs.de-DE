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
localization_priority: Normal
ms.assetid: deea3ee6-2a32-47ef-bfa4-914891538633
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e468dc18b8f78f56acaa67c2f23dd53254088ad0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790593"
---
# <a name="xlfevaluate"></a>xlfEvaluate

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Verwendet Microsoft Excel-Parser und der Funktion Auswertung für ein beliebiger Ausdruck ausgewertet werden soll, die in einer Arbeitsblattzelle eingegeben werden konnte.
  
```cs
Excel12(xlfEvaluate, LPXLOPER12 pxRes, 1, LPXLOPER12 pxFormulaText);
```

## <a name="parameters"></a>Parameter

 _PxFormulaText (XltypeStr)_
  
Die Zeichenfolge ausgewertet werden soll. Ein führendes Gleichheitszeichen (=) ist optional. Die Zeichenfolge kann Text sein, der in ein Arbeitsblatt oder Makroblatt Blatt Zelle gesetzlich eingegeben werden können.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Gibt das Ergebnis der Überprüfung der Zeichenfolge, die Typen **XltypeNum**, **XltypeStr**, **XltypeBool**, **XltypeErr**, **XltypeNil**, **XltypeMulti**angegeben werden kann.
  
## <a name="remarks"></a>Hinweise

Die Zeichenfolge kann nur Funktionen, nicht Befehl Entsprechungen enthalten. Es ist gleichbedeutend mit dem Drücken von **F9** aus der Bearbeitungsleiste angezeigt. Wenn **XlfEvaluate** eine XLL-Arbeitsblattfunktion aufgerufen wird, die als threadsicheren registriert wurde, muss der Ausdruck nur threadsicheren Funktionen enthalten. 
  
Die primäre Verwendung der **XlfEvaluate** -Funktion ist mit ermöglichen DLLs erhalten Sie Informationen zu einem definierten Namen, die entweder in einem Blatt zugewiesene Wert oder einen ausgeblendeten Namen in der DLL-Datei definiert sind. Beachten Sie, dass innerhalb einer DLL/XLL, ein Arbeitsblatt mit dem Präfix werden muss mindestens ein Ausrufezeichen (!), um sicherzustellen, dass er auf die DLL als extern interpretiert wird. Weitere Informationen finden Sie unter [Namen bewerten und andere Arbeitsblatt Formel Ausdrücke](evaluating-names-and-other-worksheet-formula-expressions.md).
  
 **XlfEvaluate** kann nicht verwendet werden, um Verweise auf einem externen Blatt ausgewertet werden soll, die nicht geöffnet ist. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **XlfEvaluate** umzuwandelnde den Text "! B38 "auf den Inhalt der Zelle B38. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Diese Funktion ruft ein Makro mit Befehlen (**XlcAlert**) und funktionieren ordnungsgemäß nur, wenn von einem Makroblatt oder als Makrobefehl aufgerufen.
  
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

- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

