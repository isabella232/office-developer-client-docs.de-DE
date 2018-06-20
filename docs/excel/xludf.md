---
title: xlUDF
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlUDF
keywords:
- XlUDF-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: b608b356-ca5c-47bb-9de8-9b7e2b3924dd
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8f45f800ca50d2a46792e7cf5e00ac25bd099e8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790623"
---
# <a name="xludf"></a>xlUDF

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Ruft eine benutzerdefinierte Funktion (UDF). Diese Funktion ermöglicht eine DLL zu Visual Basic für Applikationen (VBA) von benutzerdefinierten Funktionen, XLM-Makros-Sprache-Funktionen und registrierten in anderen add-ins enthaltenen Funktionen aufrufen.
  
```cs
Excel12(xlUDF, LPXLOPER12 pxRes, int iCount, LPXLOPER12 pxFnRef,
LPXLOPER12 pxArg1, ...);
```

## <a name="parameters"></a>Parameter

_pxFnRef_ (**XltypeRef**, **XltypeSRef**, **XltypeStr** oder **XltypeNum**)
  
Der Verweis von der Funktion, die Sie anrufen möchten. Dies kann ein Makro Blatt Zellbezug aufweisen, der registrierten Name der Funktion als String oder die Register-ID der Funktion sein. Für XLL-add-in-Funktionen mit **XlfRegister** , oder **Registrieren Sie** mit der bereitgestellten Argument _PxFunctionText_ registriert kann die ID mit **XlfEvaluate** zum Nachschlagen von den Namen abgerufen werden. 
  
_pxArg1..._
  
NULL oder mehr Argumente an die benutzerdefinierte Funktion. Wenn Sie diese Funktion in Versionen vor Excel 2007 aufrufen, die maximale Anzahl von zusätzlichen Argumenten, die übergeben werden kann, ist 29, 30 einschließlich _PxFnRef_. Ab Excel 2007 dieser Grenze ausgelöst wird in 254, 255 einschließlich _PxFnRef_.
  
## <a name="return-value"></a>R�ckgabewert

Gibt den Wert der benutzerdefinierten Funktion zurückgegeben wird.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel führt die **Kategorie** auf Blatt Macro1 in Mappe1. XLS. Stellen Sie sicher, dass das Makro in einem Blatt Makro1 ist. 
  
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

