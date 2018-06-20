---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- Xlsheetnm-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790622"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Namen des ein Arbeitsblatt oder eine Makrovorlage aus der internen Blatt-ID, die ein externer Verweis oder den Namen des aktuellen Blatts enthaltenen, wenn einen internen Verweis übergeben zurück.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Parameter

_pxExtref_ (**XltypeRef** oder **XltypeSRef**)
  
Ein Verweis auf das Blatt, deren Namen Sie möchten.
  
Wenn Sie einen externen Verweis (**XltypeRef**) übergeben müssen sie nur die ID des Blatts enthalten. Die Datenstrukturen, die die Zellen im Arbeitsblatt beschreiben werden ignoriert und müssen nicht angegeben werden. Wenn die ID 0 (null) festgelegt ist, wird der Name des das aktuelle Blatt von **XlSheetNm** zurückgegeben. 
  
Wenn Sie einen internen Verweis (**XltypeSef**) übergeben, wird der Name des aktuellen Blatts von **XlSheetNm** zurückgegeben. 
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Gibt den Namen des Blatts (**XltypeStr**) in das Formular `[Book1]Sheet1`.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt den Namen des Blatts, von dem die Funktion aufgerufen wurde. Die Funktion funktioniert nur, wenn Sie von einem Makroblatt aufgerufen wird, während der Ausführung eines XLM-Makros Befehl. Dies ist, da es aufruft, **XlcAlert**, die nur Befehle führen können, und sie muss von einem Blatt statt ein Dialogfeld, im Menü oder Befehlsleiste in der Reihenfolge für **XlfCaller** zum Zurückgeben eines Verweises aufgerufen werden. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch

- [xlSheetId](xlsheetid.md)
- [C C-API-Funktionen, die nur aus einer DLL oder XLL aufgerufen werden k�nnen](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

