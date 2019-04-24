---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- xlsheetnm-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5d62be7ebef71547de3a903db4c1a030984b8640
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303871"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Gibt den Namen eines Arbeitsblatts oder einer Makrovorlage aus der internen Blatt-ID zurück, die in einem externen Verweis enthalten ist, oder den Namen des aktuellen Blatts, wenn ein interner Verweis übergeben wird.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Parameter

_pxExtref_ (**externen xltypeRef** oder **xltypeSRef**)
  
Ein Verweis auf das Blatt, dessen Name Sie wünschen.
  
Wenn Sie einen externen Verweis (**externen xltypeRef**) übergeben, muss er nur die ID des Blatts enthalten. Die Datenstrukturen, die die Zellen im Arbeitsblatt beschreiben, werden ignoriert und müssen nicht bereitgestellt werden. Wenn die ID auf NULL festgelegt ist, gibt **xlSheetNm** den Namen des aktuellen Blatts zurück. 
  
Wenn Sie einen internen Verweis (**xltypeSef**) übergeben, gibt **xlSheetNm** den Namen des aktuellen Blatts zurück. 
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Gibt den Namen des Blatts (**xltypeStr**) im Formular `[Book1]Sheet1`zurück.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird der Name des Blatts angezeigt, aus dem die Funktion aufgerufen wurde. Die Funktion funktioniert nur dann ordnungsgemäß, wenn Sie beim Ausführen eines XML-Befehlsmakros aus einer Makrovorlage aufgerufen wird. Der Grund ist, dass **xlcAlert**aufgerufen wird, die nur von Befehlen ausgeführt werden können und die von einem Arbeitsblatt und nicht von einem Dialogfeld, einem Menü oder einer Befehlsleiste abgerufen werden müssen, damit **xlfCaller** einen Verweis zurückgibt. 
  
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

