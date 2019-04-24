---
title: TempActiveColumn/TempActiveColumn12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveColumn
- TempActiveColumn12
keywords:
- tempactivecolumn12-Funktion [Excel 2007], TempActiveColumn-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310472"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktionen, mit denen ein temporäres **XLOPER**/ -**XLOPER12** erstellt wird, das einen externen Verweis auf eine ganze Spalte im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parameter

 _Col_ (**Byte**)
  
Die Spalte, auf die verwiesen werden soll. Dies ist nullbasiert, sodass Spalte A als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und beginnend mit Excel 2007, die eine Arbeitsmappe im Kompatibilitätsmodus ausführt, ist der Höchstwert 255 = 2 ^ 8-1 und ist der Maximalwert, der von einer BYTE-Ganzzahl verwendet werden kann. Ab Excel 2007 mit einer Arbeitsmappe ist der Höchstwert 16.383 = 2 ^ 14-1. COL ist als eine 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen externen **externen xltypeRef** -Verweis auf die übergebene Spalte zurück. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird **TempActiveColumn12** verwendet, um die gesamte Spalte B auszuwählen. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveColumnExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveColumn12(1));
    return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

