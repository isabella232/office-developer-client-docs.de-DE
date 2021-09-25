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
- tempactivecolumn12 function [excel 2007],TempActiveColumn function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0ab26134edca76e026f2fe46c3b111e917a7dad1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59614591"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktionen, die einen temporären **XLOPER** /  **XLOPER12** erstellen, der einen externen Verweis auf eine gesamte Spalte im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parameter

 _col_ (**BYTE**)
  
Die Spalte, auf die verwiesen werden soll. Dies ist nullbasiert, sodass Spalte A als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, beträgt der Maximalwert 255 = 2^8 - 1 und ist der Maximalwert, der von einer ganzzahligen BYTE-Zahl verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, beträgt der Maximalwert 16.383 = 2^14 - 1. COL ist in XLCALL.H als 32-Bit-Ganzzahl mit Vorzeichen definiert.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen externen **XltypeRef-Verweis** auf die übergebene Spalte zurück. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel **wird TempActiveColumn12** verwendet, um die gesamte Spalte B auszuwählen. 
  
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

