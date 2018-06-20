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
- Tempactiveref-Funktion [excel 2007], TempActiveRef12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5c2e82dcaf9bf562048b5d2582ece1bd262b47eb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790567"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** mit einer externen Referenz zu rechteckigen zellenblocks auf dem aktiven Blatt. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parameter

 _rwFirst_
  
Die Startzeile des Verweises.
  
 _rwLast_
  
Die letzte Zeile des Verweises.
  
Zeile Argumente sind nullbasiert, damit diese Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, der Höchstwert ist 65.535 = 2 ^ 16-1 und gibt den Maximalwert, die durch eine ganze Zahl mit WORD entnommen werden kann. Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 1.048.575 = 2 ^ 20-1. Lese ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
 _colFirst_
  
Die Anfangs-Spaltennummer des Verweises.
  
 _colLast_
  
Die Spaltennummer der letzten, des Verweises.
  
Spalte Argumente sind nullbasiert, damit diese Spalte A als 0 übergeben wird. Der Höchstwert ist in Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, 255 = 2 ^ 8-1 und der maximale Wert ist, die durch eine BYTE-Ganzzahl entnommen werden kann. Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 16,383 = 2 ^ 14 1. Spalte ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
## <a name="return-value"></a>R�ckgabewert

Gibt einen **XltypeRef** externer Verweis auf rechteckigen zellenblocks übergeben. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempActiveRef12** -Funktion verwendet, um Zellen A105:C110 auszuwählen. 
  
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

