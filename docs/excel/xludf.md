---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- xlUDF-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303815"
---
# <a name="xludf"></a>xlUDF

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine benutzerdefinierte Funktion (UDF) auf. Diese Funktion ermöglicht es einer DLL, benutzerdefinierte VBA-Funktionen (Visual Basic für Applikationen), XML-Sprachfunktionen und in anderen Add-ins enthaltene registrierte Funktionen aufzurufen.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parameter

_pxFnRef_ (**externen xltypeRef**, **xltypeSRef**, **xltypeStr** oder **xltypeNum**)
  
Der Verweis der Funktion, die Sie aufrufen möchten. Dies kann ein Makroblatt-Zellbezug, der registrierte Name der Funktion als Zeichenfolge oder die Register-ID der Funktion sein. Für XLL-Add-in-Funktionen, die mit **xlfRegister** registriert sind, oder **registrieren** Sie sich mit dem angegebenen Argument _pxFunctionText_ , kann die ID mithilfe von **xlfEvaluate** abgerufen werden, um den Namen zu suchen. 
  
_pxArg1,..._
  
NULL oder mehr Argumente für die benutzerdefinierte Funktion. Wenn Sie diese Funktion in früheren Versionen als Excel 2007 aufrufen, ist die maximale Anzahl von zusätzlichen Argumenten, die übergeben werden können, 29, was 30 ist, einschließlich _pxFnRef_. Ab Excel 2007 wird dieser Grenzwert auf 254 erhöht, was 255 einschließlich _pxFnRef_ist.
  
## <a name="return-value"></a>Rückgabewert

Gibt den Wert zurück, der von der benutzerdefinierten Funktion zurückgegeben wird.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird **TestMacro** auf Blatt MACRO1 in book1 ausgeführt. XLS. Stellen Sie sicher, dass sich das Makro in einem Arbeitsblatt mit dem Namen Macro1 befindet. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlUDFExample(void)
{       
   XLOPER12 xMacroName, xMacroRef, xRes;
   xMacroName.xltype = xltypeStr;
   xMacroName.val.str = L"\044[BOOK1.XLSX]Macro1!TestMacro";
   Excel12(xlfEvaluate, &xMacroRef, 1, (LPXLOPER12)&xMacroName);
   Excel12(xlUDF, &xRes, 1, (LPXLOPER12)&xMacroRef);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch

- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

