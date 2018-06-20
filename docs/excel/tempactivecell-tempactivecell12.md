---
title: TempActiveCell/TempActiveCell12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempActiveCell
- TempActiveCell12
keywords:
- tempactivecell12-Funktion [excel 2007], TempActiveCell-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8ad409a76195d67fa61e7991ce6527c40e0a3265
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790564"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Funktionen der Framework-Bibliothek, die eine temporäre **XLOPER**erstellen/ **XLOPER12** , die einen externen Verweis auf eine Zelle im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Parameter

 _Zeile_
  
Die Zeile verwiesen werden. Zeile Argumente sind nullbasiert, damit diese Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, der Höchstwert ist 65.535 = 2 ^ 16-1 und gibt den Maximalwert, die durch eine ganze Zahl mit WORD entnommen werden kann. Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 1.048.575 = 2 ^ 20-1. Lese ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
 _Spalte_
  
Die Spalte verwiesen werden. Dies ist nullbasiert, sodass diese Spalte A als 0 übergeben wird. Der Höchstwert ist in Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, 255 = 2 ^ 8-1 und der maximale Wert ist, die durch eine BYTE-Ganzzahl entnommen werden kann. Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 16,383 = 2 ^ 14 1. Spalte ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
## <a name="return-value"></a>R�ckgabewert

Gibt einen **XltypeRef** externer Verweis auf die Zelle übergeben. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel verwendet die **TempActiveCell12** zum Anzeigen des Inhalts der B94 auf dem aktiven Blatt. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempActiveCellExample(void)
{
   Excel12f(xlcAlert, 0, 1, TempActiveCell12(93,1));
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

