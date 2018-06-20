---
title: Funktionen in der Framework-Klassenbibliothek
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- Funktionen der Framework-Bibliothek [excel 2007], Funktionen [Excel 2007], Framework-Klassenbibliothek
localization_priority: Normal
ms.assetid: 7d9a13fd-9a4c-423e-bb08-4a5be57c7905
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1d3878e376f95be3b277f1bb1a59545eb0a631ac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790516"
---
# <a name="functions-in-the-framework-library"></a>Funktionen in der Framework-Klassenbibliothek

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Der Framework-Klassenbibliothek erstellt wurde, um das Schreiben von XLLs leichter machen. Sie enthält einfache Funktionen für die Verwaltung von **XLOPER**/ **XLOPER12** Arbeitsspeicher, zum Erstellen der temporären **XLOPER**/ **XLOPER12**, die Microsoft Excel-Rückruffunktionen (**Excel4**, **Excel4v** robust aufrufen ** Excel12 **, ** Excel12v **) und Debuggen von Zeichenfolgen auf eine angefügte Terminal drucken.
  
Die in dieser Bibliothek enthaltenen Funktionen vereinfachen Codeabschnitte, die wie folgt aussieht.
  
```cs
XLOPER12 xMissing, xBool;
xMissing.xltype = xltypeMissing;
xBool.xltype = xltypeBool;
xBool.val.xbool = 0;
Excel12(xlcDisplay, 0, 2, (LPXLOPER12) &xMissing, (LPXLOPER12) &xBool);
```

Der vereinfachte Code sieht wie im folgenden Beispiel wird.
  
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
   
|**Funktionen, die mit XLOPERs verwendet werden.**|**Funktionen, die mit XLOPER12s verwendet werden.**|
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
   
Verwendung dieser Funktionen verkürzt die Zeitdauer, die erforderlich sind, einer DLL oder XLL zu schreiben. Beginn der Entwicklung von der beispielanwendung verkürzt generische Entwicklungszeit. Verwenden Sie Allgemeines. C als Vorlage, die im Rahmen der eine XLL eingerichtet, und Ersetzen Sie den vorhandenen Code durch Ihren eigenen unterstützen.
  
Die temporäre **XLOPER**/ **XLOPER12** Funktionen erstellen **XLOPER**/ **XLOPER12** Werte mithilfe der Speicher von einem lokalen Heap Framework-Klassenbibliothek verwaltet. Die **XLOPER**/ **XLOPER12** Werte bleiben gültig, bis Sie die **FreeAllTempMemory** -Funktion oder eine **Excel-** oder **Excel12f** -Funktionen aufrufen. (Die Funktionen von **Excel** und **Excel12f** frei alle temporären Speicher vor der Rückgabe). 
  
Um die Funktionen der Framework-Bibliothek verwenden, müssen Sie die FRAMEWRK einbeziehen. H-Datei in Ihrem C#-Code, und fügen Sie die FRAMEWRK. C oder FRMWRK32. LIB-Dateien auf Ihr Codeprojekt.
  
## <a name="see-also"></a>Siehe auch

- [Excel XLL-SDK-API-Funktionsreferenz](excel-xll-sdk-api-function-reference.md)

