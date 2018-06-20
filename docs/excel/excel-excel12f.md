---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- Excel-Funktion [excel 2007], Excel12f-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 56034984852713496465c3d1f79a9989fc47df1c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790432"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Funktionen von Framework-Bibliothek. **Excel** ist ein Wrapper für die [Excel4](excel4-excel12.md) -Funktion. **Excel12f** ist ein Wrapper für die [Excel12](excel4-excel12.md) -Funktion. Jede überprüft, um anzuzeigen, dass keines der Argumente 0 (null) ist, bedeuten würde, dass die Erstellung einer temporären **XLOPER** oder **XLOPER12** ist fehlgeschlagen. Wenn ein Fehler auftritt, wird jeweils eine Debug-Meldung gedruckt. Abschließend frei jeweils alle temporären Speicher, der für die temporäre **XLOPER**s und **XLOPER12**s erstellt wurden.
  
 **Excel12f** kann nur aus einer DLL, beginnend mit der C-API für Excel 2007-Bibliothek aufgerufen werden. Darüber hinaus nur bei der Ausführung, beginnend mit Excel 2007 und Funktionsweise andernfalls schlägt mit **xlretFailed zurück** . 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**Int**)
  
Eine Zahl, die den Befehl oder die Funktion angibt, die Sie anrufen möchten. Weitere Informationen finden Sie unter [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Ein Zeiger auf Ergebnis der Funktion ausgewertet. Alle Speicher im das Ergebnis gezeigt wird von Excel zugeordnet worden sein und sollte im Gespräch zu [XlFree](xlfree.md) , sobald diese nicht mehr erforderlich ist, oder durch **XlbitXLFree** festlegen, wenn nach Excel zurückgegeben freigegeben werden. 
  
 _iCount_ (**Int**)
  
Die Anzahl von Argumenten, die an die Funktion übergeben werden. Ab Excel 2007 ist die Grenze 255 Argumente. In früheren Versionen ist die Grenze 30.
  
 _argument1..._
  
Die optionalen Argumente an die Funktion. Alle Argumente müssen Zeiger auf **XLOPER**s im Fall von **Excel**oder **XLOPER12**s im Fall von **Excel12f**sein.
  
## <a name="return-value"></a>R�ckgabewert

Beide Funktionen zurückgegeben derselbe Fehler und Erfolgscodes als **Excel4**, **Excel4v**, **Excel12**und **Excel12v**. Eine vollständige Beschreibung dieser Codes finden Sie unter [Excel4/Excel12](excel4-excel12.md) . Darüber hinaus Rückgabewerte diese Funktionen Framework **xlretFailed zurück** , ohne einen Aufruf der C-API, wenn ein NULL-Zeiger auf einen Parameter erkannt wird. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel werden ein ungültiges Argument an die Funktion **Excel12f** , sendet eine Meldung an den Debugger übergibt. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI Excel12fExample(void)
{
    Excel12f(xlcDisplay, 0, 1, 0);
    return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Excel4/Excel12](excel4-excel12.md)


[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

