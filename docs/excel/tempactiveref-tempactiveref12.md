---
title: TempActiveRef/TempActiveRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveRef
- TempActiveRef12
keywords:
- tempactiveref-Funktion [Excel 2007], TempActiveRef12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32301568"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, mit der ein temporäres **XLOPER**/ -**XLOPER12** erstellt wird, das eine externe Referenz auf rechteckigen Zellenblock im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parameter

 _rwFirst_
  
Die Startzeile des Verweises.
  
 _rwLast_
  
Die Endzeile des Verweises.
  
Zeilenargumente sind nullbasiert, sodass Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und beginnend mit Excel 2007, die eine Arbeitsmappe im Kompatibilitätsmodus ausführt, ist der Höchstwert 65.535 = 2 ^ 16-1 und ist der Höchstwert, der von einem Wort Integer verwendet werden kann. Ab Excel 2007 mit einer Arbeitsmappe ist der Höchstwert 1.048.575 = 2 ^ 20-1. RW ist als eine 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
 _colFirst_
  
Die Nummer der ersten Spalte des Verweises.
  
 _colLa_
  
Die Nummer der letzten Spalte des Verweises.
  
Spalten Argumente sind nullbasiert, sodass Spalte A als 0 übergeben wird. In Excel 2003 und früheren Versionen und beginnend mit Excel 2007, die eine Arbeitsmappe im Kompatibilitätsmodus ausführt, ist der Höchstwert 255 = 2 ^ 8-1 und ist der Maximalwert, der von einer BYTE-Ganzzahl verwendet werden kann. Ab Excel 2007 mit einer Arbeitsmappe ist der Höchstwert 16.383 = 2 ^ 14-1. COL ist als eine 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen **externen xltypeRef** -externen Verweis auf den rechteckigen Block der übergebenen Zellen zurück. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempActiveRef12** -Funktion verwendet, um Zellen A105: C110 auszuwählen. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveRefExample(void)
{
    Excel12f(xlcSelect, 0, 1, TempActiveRef12(104, 109, 0, 2));
    return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

