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
- tempactivecolumn12-Funktion [excel 2007], TempActiveColumn-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ac3dbb0bb43527f790e6934d73bee30a33f8555f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790570"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Funktionen der Framework-Bibliothek, die eine temporäre **XLOPER**erstellen/ **XLOPER12** , die einen externen Verweis auf eine ganze Spalte im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parameter

 _Spalte_ (**BYTE**)
  
Die Spalte verwiesen werden. Dies ist nullbasiert, sodass diese Spalte A als 0 übergeben wird. Der Höchstwert ist in Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007 eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt, 255 = 2 ^ 8-1 und der maximale Wert ist, die durch eine BYTE-Ganzzahl entnommen werden kann. Ab Excel 2007 mit einer Arbeitsmappe, der Höchstwert ist 16,383 = 2 ^ 14 1. Spalte ist als 32-Bit-Ganzzahl mit Vorzeichen in XLCALL definiert. H.
  
## <a name="return-value"></a>R�ckgabewert

Gibt einen **XltypeRef** externer Verweis auf die Spalte übergebenen zurück. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel verwendet die **TempActiveColumn12** , wählen Sie die gesamte Spalte B. 
  
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

