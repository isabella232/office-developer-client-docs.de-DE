---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- xludf-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a68794f61b791e911a6899922311973c5d747ab3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631391"
---
# <a name="xludf"></a>xlUDF

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine benutzerdefinierte Funktion (UDF) auf. Diese Funktion ermöglicht einer DLL das Aufrufen Visual Basic for Applications (VBA) benutzerdefinierter Funktionen, XLM-Makrosprachenfunktionen und registrierter Funktionen, die in anderen Add-Ins enthalten sind.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parameter

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** oder **xltypeNum**)
  
Der Verweis auf die Funktion, die Sie aufrufen möchten. Dabei kann es sich um einen Makroblatt-Zellbezug, den registrierten Namen der Funktion als Zeichenfolge oder die Register-ID der Funktion handeln. Für XLL-Add-In-Funktionen, die mit **xlfRegister** oder **REGISTER** mit dem angegebenen Argument  _pxFunctionText_ registriert wurden, kann die ID mithilfe von **xlfEvaluate** abgerufen werden, um den Namen nachzuschlagen. 
  
_pxArg1, ..._
  
Null oder mehr Argumente für die benutzerdefinierte Funktion. Wenn Sie diese Funktion in Versionen vor Excel 2007 aufrufen, beträgt die maximale Anzahl von zusätzlichen Argumenten, die übergeben werden können, 29, was 30 einschließlich _pxFnRef_ ist. Ab Excel 2007 wird dieser Grenzwert auf 254 erhöht, was 255 einschließlich _pxFnRef_ ist.
  
## <a name="return-value"></a>Rückgabewert

Gibt den Wert zurück, den die benutzerdefinierte Funktion zurückgegeben hat.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird **TestMacro** auf dem Blatt Macro1 in BOOK1.XLS ausgeführt. Stellen Sie sicher, dass sich das Makro auf einem Blatt mit dem Namen Macro1 befindet. 
  
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

- [C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden können](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

