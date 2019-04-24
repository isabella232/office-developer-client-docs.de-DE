---
title: TempActiveRow/TempActiveRow12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRow
- TempActiveRow12
keywords:
- tempactiverow-Funktion [Excel 2007], TempActiveRow12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310416"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktionen, mit denen ein temporäres **XLOPER**/ -**XLOPER12** erstellt wird, das einen externen Verweis auf eine ganze Zeile im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Parameter

 _Zeile_
  
Die Zeile, auf die verwiesen werden soll. Zeilenargumente sind nullbasiert, sodass Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und beginnend mit Excel 2007, die eine Arbeitsmappe im Kompatibilitätsmodus ausführt, ist der Höchstwert 65.535 = 2 ^ 16-1 und ist der Höchstwert, der von einem Wort Integer verwendet werden kann. Ab Excel 2007 mit einer Arbeitsmappe ist der Höchstwert 1.048.575 = 2 ^ 20-1. RW ist als eine 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen externen **externen xltypeRef** -Verweis auf Zeilen Zellen zurück, die übergeben werden. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempActiveRow12** -Funktion verwendet, um Zeile 113 zu markieren. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRowExample(void)
{
   Excel12f(xlcSelect, 0, 1, TempActiveRow12(112));
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

