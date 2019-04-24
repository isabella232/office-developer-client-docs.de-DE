---
title: Funktionen in der Framework-Bibliothek
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Framework-Bibliotheksfunktionen [Excel 2007], Funktionen [Excel 2007], Framework-Bibliothek
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 4eeb9e5db09592e98e9afb763efaa6be18eb2f7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304053"
---
# <a name="functions-in-the-framework-library"></a>Funktionen in der Framework-Bibliothek

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Die Framework-Bibliothek wurde erstellt, um das Schreiben von XLLs zu vereinfachen. Sie enthält einfache Funktionen zum Verwalten des **XLOPER**/ -**XLOPER12** -Speichers, zum Erstellen temporärer **XLOPER**/ -**XLOPER12**und zum robusten Aufrufen der Microsoft Excel-Rückruffunktionen (**Excel4**, **Excel4v** , * * Excel12 * *, * * Excel12v * *) und Drucken von Debug-Zeichenfolgen auf einem angefügten Terminal.
  
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
|[TempErierung](temperr-temperr12.md) <br/> |[TempErr12](temperr-temperr12.md) <br/> |
|[TempActiveRef](tempactiveref-tempactiveref12.md) <br/> |[TempActiveRef12](tempactiveref-tempactiveref12.md) <br/> |
|[TempActiveCell](tempactivecell-tempactivecell12.md) <br/> |[TempActiveCell12](tempactivecell-tempactivecell12.md) <br/> |
|[TempActiveRow](tempactiverow-tempactiverow12.md) <br/> |[TempActiveRow12](tempactiverow-tempactiverow12.md) <br/> |
|[TempActiveColumn](tempactivecolumn-tempactivecolumn12.md) <br/> |[TempActiveColumn12](tempactivecolumn-tempactivecolumn12.md) <br/> |
|[TempMissing](tempmissing-tempmissing12.md) <br/> |[TempMissing12](tempmissing-tempmissing12.md) <br/> |
   
Die Verwendung dieser Funktionen verkürzt die Zeitdauer, die zum Schreiben einer DLL oder XLL benötigt wird. Das Starten der Entwicklung aus der Beispielanwendung GENERIC verkürzt auch die Entwicklungszeit. Verwenden Sie GENERIC. C als Vorlage zum Einrichten des Frameworks einer XLL und ersetzen Sie dann den vorhandenen Code durch eigene.
  
Die temporären **XLOPER**/ **-XLOPER12** -Funktionen erstellen **XLOPER**/ -**XLOPER12** Werte, indem Sie Arbeitsspeicher aus einem lokalen Heap verwenden, der von der Framework-Bibliothek verwaltet wird. Die **XLOPER**/ **XLOPER12** -Werte bleiben gültig, bis Sie die **FreeAllTempMemory** -Funktion oder eine der **Excel** -oder **Excel12f** -Funktionen aufrufen. (Der **Excel** -und der **Excel12f** -Funktion werden alle temporären Arbeitsspeicher freigegeben, bevor Sie zurückkehren.) 
  
Um die Framework-Bibliotheksfunktionen verwenden zu können, müssen Sie die GERIPPE. H-Datei in Ihrem C-Code, und fügen Sie die GERIPPE. C oder FRMWRK32. LIB-Dateien für Ihr Codeprojekt.
  
## <a name="see-also"></a>Siehe auch

- [Excel XLL SDK – API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

