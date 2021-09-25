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
ms.localizationpriority: medium
ms.assetid: 4e6a9ccc-988d-42a9-8874-01f2ee29b835
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bae0e56648392469dd532259c941e71674f67fd0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601366"
---
# <a name="excelexcel12f"></a>Excel/Excel12f

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktionen. **Excel** ist ein Wrapper für die [Excel4-Funktion.](excel4-excel12.md) **Excel12f** ist ein Wrapper für die [Excel12-Funktion.](excel4-excel12.md) Bei jeder Überprüfung wird überprüft, ob keines der Argumente Null ist, was darauf hinweist, dass die Erstellung eines temporären **XLOPER-** oder **XLOPER12-Vorgangs** fehlgeschlagen ist. Wenn ein Fehler auftritt, wird jeweils eine Debugmeldung ausgegeben. Nach Abschluss des Vorgangs gibt jeder Temporäre Speicher frei, der möglicherweise für temporäre **XLOPER-Elemente** und **XLOPER12-Elemente** erstellt wurde.
  
 **Excel12f** kann nur von einer DLL aufgerufen werden, die mit der C-API-Bibliothek Excel 2007 beginnt. Darüber hinaus funktioniert sie nur, wenn sie ab Excel 2007 ausgeführt wird, und schlägt andernfalls mit **xlretFailed fehl.** 
  
```cs
int Excel(int iFunction, LPXLOPER pxRes, int iCount, 
LPXLOPER argument1, ...);
int Excel12f(int iFunction, LPXLOPER12 pxRes, int iCount, 
LPXLOPER12 argument1, ...);
```

## <a name="parameters"></a>Parameter

 _iFunction_ (**int**)
  
Eine Zahl, die den Befehl oder die Funktion angibt, den Sie aufrufen möchten. Weitere Informationen finden Sie unter [Excel4/Excel12.](excel4-excel12.md)
  
 _pxRes_
  
Ein Zeiger auf das Ergebnis der ausgewerteten Funktion. Jeder Speicher, auf den im Ergebnis verwiesen wird, wurde von Excel zugewiesen und sollte in einem [XlFree-Aufruf](xlfree.md) freigegeben werden, sobald er nicht mehr benötigt wird, oder durch Festlegen von **xlbitXLFree,** wenn er auf Excel zurückgegeben wird. 
  
 _iCount_ (**int**)
  
Die Anzahl der Argumente, die an die Funktion übergeben werden. Ab Excel 2007 beträgt der Grenzwert 255 Argumente. In früheren Versionen beträgt der Grenzwert 30.
  
 _argument1, ..._
  
Die optionalen Argumente für die Funktion. Bei **allen** Argumenten muss es sich bei Excel um **XLOPER-Elemente** oder bei **Excel12f** um XLOPER12-Argumente handeln. 
  
## <a name="return-value"></a>Rückgabewert

Beide Funktionen geben die gleichen Fehler- und Erfolgscodes wie **Excel4**, **Excel4v**, **Excel12** und **Excel12v** zurück. Eine vollständige Beschreibung dieser Codes finden Sie unter [Excel4/Excel12.](excel4-excel12.md) Darüber hinaus geben diese Framework-Funktionen **xlretFailed** zurück, ohne die C-API aufzurufen, wenn ein NULL-Zeiger auf einen Parameter erkannt wird. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird ein ungültiges Argument an die **Excel12f-Funktion** übergeben, die eine Nachricht an den Debugger sendet. 
  
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

