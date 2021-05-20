---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- xludf-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 569334847c7612b86f6ddc967f159e2ef425cbbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430644"
---
# <a name="xludf"></a>xlUDF

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine benutzerdefinierte Funktion (USERF) auf. Mit dieser Funktion kann eine DLL Visual Basic for Applications (VBA) benutzerdefinierte Funktionen, XLM-Makrosprachenfunktionen und registrierte Funktionen aufrufen, die in anderen Add-Ins enthalten sind.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parameter

_pxFnRef_ (**xltypeRef**, **xltypeSRef**, **xltypeStr** oder **xltypeNum**)
  
Der Verweis auf die Funktion, die Sie aufrufen möchten. Dies kann ein Makroblattzellenverweis, der registrierte Name der Funktion als Zeichenfolge oder die Register-ID der Funktion sein. Für XLL-Add-In-Funktionen, die mithilfe von **xlfRegister** oder **REGISTER** mit dem angegebenen Argument  _pxFunctionText_ registriert wurden, kann die ID mithilfe von **xlfEvaluate** zum Suchen nach dem Namen erhalten werden. 
  
_pxArg1, ..._
  
Null oder mehr Argumente für die benutzerdefinierte Funktion. Wenn Sie diese Funktion in Versionen vor Excel 2007 aufrufen, ist die maximale Anzahl zusätzlicher Argumente, die übergeben werden können, 29, d. h. 30 einschließlich _pxFnRef_. Ab Excel 2007 wird dieser Grenzwert auf 254 angehoben, d. h. 255 einschließlich _pxFnRef_.
  
## <a name="return-value"></a>Rückgabewert

Gibt den von der benutzerdefinierten Funktion zurückgegebenen Wert zurück.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird **TestMacro auf** Blatt Macro1 in BOOK1.XLS. Stellen Sie sicher, dass sich das Makro auf einem Blatt mit dem Namen "Macro1" befindet. 
  
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

