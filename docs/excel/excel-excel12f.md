---
title: Excel/Excel12f
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Excel12f
keywords:
- excel-Funktion [excel 2007],Excel12f-Funktion [Excel 2007]
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
  
Funktionen der Frameworkbibliothek. **Excel** ist ein Wrapper für die [Excel4-Funktion.](excel4-excel12.md) **Excel12f** ist ein Wrapper für die [Excel12-Funktion.](excel4-excel12.md) Jeder überprüft, ob keines der Argumente null ist, was darauf hindelangt, dass die Erstellung eines temporären **XLOPER-** oder **XLOPER12-Werts fehlgeschlagen** ist. Wenn ein Fehler auftritt, wird jeweils eine Debugmeldung ausgegeben. Nach Abschluss gibt jeder den temporären Speicher frei, der möglicherweise für temporäre **XLOPER** s und **XLOPER12** s erstellt wurde.
  
 **Excel12f** kann nur von einer DLL aus aufgerufen werden, die mit der Excel 2007 C-API-Bibliothek beginnt. Darüber hinaus funktioniert sie nur, wenn sie ab Excel 2007 ausgeführt wird und andernfalls **mit xlretFailed fehlschlägt.** 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**int**)
  
Eine Zahl, die den Befehl oder die Funktion angibt, den Sie aufrufen möchten. Weitere Informationen finden Sie unter [Excel4/Excel12](excel4-excel12.md).
  
 _pxRes_
  
Ein Zeiger auf das Ergebnis der ausgewerteten Funktion. Jeder Speicher, auf den im Ergebnis verwiesen wird, wurde von Excel zugewiesen und sollte in einem Aufruf von [xlFree](xlfree.md) frei werden, sobald er nicht mehr benötigt wird, oder durch Festlegen **von xlbitXLFree,** wenn er an Excel. 
  
 _iCount_ (**int**)
  
Die Anzahl der Argumente, die an die Funktion übergeben werden. Ab Excel 2007 beträgt der Grenzwert 255 Argumente. In früheren Versionen beträgt der Grenzwert 30.
  
 _argument1, ..._
  
Die optionalen Argumente für die Funktion. Alle Argumente müssen Zeiger auf **XLOPER** s im Fall von **Excel** oder **XLOPER12** s im Fall von **Excel12f sein.**
  
## <a name="return-value"></a>Rückgabewert

Beide Funktionen geben dieselben Fehler- und Erfolgscodes wie **Excel4,** **Excel4v,** **Excel12** und **Excel12v zurück.** Eine vollständige Beschreibung dieser Codes finden Sie unter [Excel4/Excel12.](excel4-excel12.md) Darüber hinaus geben diese Framework-Funktionen **xlretFailed** ohne Aufruf der C-API zurück, wenn ein #A0 auf einen Parameter erkannt wird. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird ein ungültiges Argument an die **Excel12f-Funktion** übermittelt, die eine Nachricht an den Debugger sendet. 
  
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

