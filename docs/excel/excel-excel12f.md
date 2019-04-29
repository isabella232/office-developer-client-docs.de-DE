---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- Excel-Funktion [Excel 2007], Excel12f-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f7ff6afac1737ee869e69fffd3dbed36a908b376
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431673"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktionen. **Excel** ist ein Wrapper für die [Excel4](excel4-excel12.md) -Funktion. **Excel12f** ist ein Wrapper für die [Excel12](excel4-excel12.md) -Funktion. Jeder überprüft, ob keines der Argumente NULL ist, was darauf hinweist, dass die Erstellung eines temporären **XLOPER** oder **XLOPER12** fehlgeschlagen ist. Wenn ein Fehler auftritt, wird jeweils eine Debug-Meldung ausgegeben. Wenn der Vorgang abgeschlossen ist, werden alle temporären Speicher freigegeben, die für temporäre **XLOPER**s und **XLOPER12**s erstellt wurden.
  
 **Excel12f** kann nur von einer DLL aufgerufen werden, die mit der Excel 2007 C-API-Bibliothek beginnt. Außerdem funktioniert es nur, wenn es ab Excel 2007 ausgeführt wird, und schlägt mit **xlretFailed** andernfalls fehl. 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**int**)
  
Eine Zahl, die den anzurufenden Befehl oder die Funktion angibt. Weitere Informationen finden Sie unter [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Ein Zeiger auf das Ergebnis der ausgewertet-Funktion. Jeder Arbeitsspeicher, auf den im Ergebnis verwiesen wird, wird von Excel zugewiesen und sollte bei einem Aufruf von [xlFree](xlfree.md) freigegeben werden, wenn er nicht mehr benötigt wird, oder indem **xlbitXLFree** festgelegt wird, wenn es an Excel zurückgegeben wird. 
  
 _iCount_ (**int**)
  
Die Anzahl der Argumente, die an die Funktion übergeben werden. Ab Excel 2007 ist der Grenzwert 255 Argumente. In früheren Versionen beträgt die Grenze 30.
  
 _Argument1,..._
  
Die optionalen Argumente für die Funktion. Alle Argumente müssen Zeiger auf **XLOPER**s im Fall von **Excel**oder **XLOPER12**s im Fall von **Excel12f**sein.
  
## <a name="return-value"></a>Rückgabewert

Beide Funktionen geben dieselben Fehler-und Erfolgscodes zurück wie **Excel4**, **Excel4v**, **Excel12**und **Excel12v**. Eine vollständige Beschreibung dieser Codes finden Sie unter [Excel4/Excel12](excel4-excel12.md) . Darüber hinaus geben diese Frameworkfunktionen **xlretFailed** ohne Aufrufen der C-API zurück, wenn ein NULL-Zeiger auf einen Parameter erkannt wird. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird ein ungültiges Argument an die **Excel12f** -Funktion übergeben, die eine Nachricht an den Debugger sendet. 
  
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

