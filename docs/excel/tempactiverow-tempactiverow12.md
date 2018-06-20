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
- Tempactiverow-Funktion [excel 2007], TempActiveRow12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a406d6e5a8ffa91e103276cb39230058b4840614
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790565"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Funktionen der Framework-Bibliothek, die eine temporäre **XLOPER**erstellen/ **XLOPER12** , die einen externen Verweis auf eine gesamte Zeile im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Parameter

 _Zeile_
  
Die Zeile verwiesen werden. Zeile Argumente sind nullbasiert, damit diese Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, der Höchstwert ist 65.535 = 2 ^ 16-1 und gibt den Maximalwert, die durch eine ganze Zahl mit WORD entnommen werden kann. Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 1.048.575 = 2 ^ 20-1. Lese ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
## <a name="return-value"></a>R�ckgabewert

Gibt einen **XltypeRef** externer Verweis zu übergeben, die Zellen in der Zeile zurück. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempActiveRow12** -Funktion verwendet, um 113 Zeile auszuwählen. 
  
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

