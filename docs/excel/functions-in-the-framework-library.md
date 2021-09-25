---
title: Funktionen in der Frameworkbibliothek
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- framework library functions [excel 2007],functions [Excel 2007], Framework library
ms.localizationpriority: medium
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e828a8a9f8724ac9012955f885238b2ca1b3dd3d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617216"
---
# <a name="functions-in-the-framework-library"></a>Funktionen in der Frameworkbibliothek

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Die Framework-Bibliothek wurde erstellt, um das Schreiben von XLLs zu vereinfachen. Sie enthält einfache Funktionen zum Verwalten des **XLOPER** /  **XLOPER12-Speichers,** zum Erstellen temporärer **XLOPER** /  **XLOPER12,** zum robusten Aufrufen der Microsoft Excel Rückruffunktionen (**Excel4**, **Excel4v**, ** Excel12 **, ** Excel12v **) und zum Drucken von Debugzeichenfolgen in einem angefügten Terminal.
  
Die in dieser Bibliothek enthaltenen Funktionen vereinfachen einen Code, der wie folgt aussieht.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

Der vereinfachte Code sieht wie im folgenden Beispiel aus.
  
```cs
Excel12f(xlcDisplay, 0, 2, TempMissing12(), TempBool12(0));
```

Die folgenden Funktionen sind in der Framework-Bibliothek enthalten:
  
||
|:-----|
|[debugPrintf](debugprintf.md) <br/> |
|**GetTempMemory** <br/> |
|**FreeAllTempMemory** <br/> |
|[InitFramework](initframework.md) <br/> |
|[QuitFramework](quitframework.md) <br/> |
   
|**Mit XLOPERs verwendete Funktionen**|**Mit XLOPER12s verwendete Funktionen**|
|:-----|:-----|
|[Excel](excel-excel12f.md) <br/> |[Excel12f](excel-excel12f.md) <br/> |
|[TempNum](tempnum-tempnum12.md) <br/> |[TempNum12](tempnum-tempnum12.md) <br/> |
|[TempStr](tempstr.md) <br/> |[TempStr12](tempstrconst-tempstr12.md) <br/> |
|[TempStrConst](tempstrconst-tempstr12.md) <br/> |[TempStr12Const](tempstrconst-tempstr12.md) <br/> |
|[TempBool](tempbool-tempbool12.md) <br/> |[TempBool12](tempbool-tempbool12.md) <br/> |
|[TempInt](tempint-tempint12.md) <br/> |[TempInt12](tempint-tempint12.md) <br/> |
|[TempErr](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
Die Verwendung dieser Funktionen verkürzt den Zeitaufwand für das Schreiben einer DLL oder XLL. Ab der Entwicklung ab der Beispielanwendung GENERIC verkürzt sich auch die Entwicklungszeit. Verwenden Sie GENERIC. C als Vorlage zum Einrichten des Frameworks einer XLL, und ersetzen Sie dann den vorhandenen Code durch Ihren eigenen Code.
  
Die **temporären XLOPER** /  **XLOPER12-Funktionen** erstellen **XLOPER** /  **XLOPER12-Werte** mithilfe von Arbeitsspeicher aus einem lokalen Heap, der von der Framework-Bibliothek verwaltet wird. Die **XLOPER** /  **XLOPER12-Werte** bleiben gültig, bis Sie die **FreeAllTempMemory-Funktion** oder eine der **Excel-** oder **Excel12f-Funktionen** aufrufen. (Die **Funktionen Excel** und **Excel12f** geben vor der Rückgabe den gesamten temporären Speicher frei.) 
  
Um die Framework-Bibliotheksfunktionen zu verwenden, müssen Sie framewrk einschließen. H-Datei in Ihrem C-Code, und fügen Sie framewrk hinzu. C oder FRMWRK32. LIB-Dateien für Ihr Codeprojekt.
  
## <a name="see-also"></a>Siehe auch

- [Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

