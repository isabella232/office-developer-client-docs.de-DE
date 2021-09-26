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
ms.localizationpriority: medium
ms.assetid: 7c69d15a-294b-4545-983b-720409001e0e
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 7faec0ba405c8bb774cf33fc01edb2247fdbea5b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611266"
---
# <a name="tempactivereftempactiveref12"></a>TempActiveRef/TempActiveRef12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktion, die einen temporären **XLOPER** /  **XLOPER12** erstellt, der einen externen Verweis auf rechteckige Zellenblocks auf dem aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveRef(WORD rwFirst, WORD rwLast, BYTE colFirst, BYTE colLast);
LPXLOPER12 TempActiveRef12(ROW rwFirst, ROW rwLast, COL colFirst, COL colLast);
```

## <a name="parameters"></a>Parameter

 _rwFirst_
  
Die Anfangszeile des Verweises.
  
 _rwLast_
  
Die letzte Zeile des Verweises.
  
Zeilenargumente sind nullbasiert, sodass Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, beträgt der Maximalwert 65.535 = 2^16 - 1 und ist der Maximalwert, der von einer ganzzahligen WORD-Zahl verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, beträgt der Maximalwert 1.048.575 = 2^20 - 1. RW ist in XLCALL.H als 32-Bit-Ganzzahl mit Vorzeichen definiert.
  
 _colFirst_
  
Die Nummer der Anfangsspalte des Verweises.
  
 _colLast_
  
Die Nummer der letzten Spalte des Verweises.
  
Spaltenargumente sind nullbasiert, sodass Spalte A als 0 übergeben wird. In Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, beträgt der Maximalwert 255 = 2^8 - 1 und ist der Maximalwert, der von einer ganzzahligen BYTE-Zahl verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, beträgt der Maximalwert 16.383 = 2^14 - 1. COL ist in XLCALL.H als 32-Bit-Ganzzahl mit Vorzeichen definiert.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen **xltypeRef-externen** Verweis auf einen rechteckigen Zellenblock zurück, der übergeben wird. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempActiveRef12-Funktion** verwendet, um die Zellen A105:C110 auszuwählen. 
  
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

