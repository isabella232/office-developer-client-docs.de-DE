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
- tempactiveref-Funktion [excel 2007],TempActiveRef12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 58feee8f43e0f90f710c9e4387684dcb6d173a7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415544"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework library function that creates a temporary **XLOPER** /  **XLOPER12** containing an external reference to rechteckige block of cells on the active sheet. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parameter

 _rwFirst_
  
Die Anfangszeile des Verweises.
  
 _rwLast_
  
Die endende Zeile des Verweises.
  
Zeilenargumente sind nullbasierte, sodass Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der höchstwert 65.535 = 2^16 - 1 und der Höchstwert, der von einer ganzzahligen WORD-Zahl verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 1.048.575 = 2^20 - 1. RW ist in XLCALL.H als 32-Bit-ganze Zahl mit Vorzeichen definiert.
  
 _colFirst_
  
Die Nummer der Anfangsspalte des Verweises.
  
 _colLast_
  
Die Nummer der Endspalte des Verweises.
  
Spaltenargumente sind nullbasierte, sodass Spalte A als 0 übergeben wird. In Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der Maximalwert 255 = 2^8 – 1 und der Höchstwert, der von einer ganzzahligen BYTE verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 16.383 = 2^14 - 1. COL ist in XLCALL.H als 32-Bit-ganzzahlige 32-Bit-Zahl definiert.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen **externen xltypeRef-Verweis** auf einen rechteckigen Zellenblock zurück, der übergeben wird. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempActiveRef12-Funktion** zum Auswählen der Zellen A105:C110 verwendet. 
  
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

