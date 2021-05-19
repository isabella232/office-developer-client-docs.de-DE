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
- tempactivecolumn12-Funktion [excel 2007],TempActiveColumn-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 4b1f34c4-e7fa-4a0b-8fc5-c9d465ebb70c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d1399a407e3e269b78c7afbde8ff32c126b4b1bc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417875"
---
# <a name="tempactivecolumntempactivecolumn12"></a>TempActiveColumn/TempActiveColumn12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktionen, die eine temporäre **XLOPER** /  **XLOPER12** erstellen, die einen externen Verweis auf eine gesamte Spalte im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveColumn(BYTE col);
LPXLOPER12 TempActiveColumn12(COL col);
```

## <a name="parameters"></a>Parameter

 _col_ (**BYTE**)
  
Die Spalte, auf die verwiesen werden soll. Dies ist nullbasierte, sodass Spalte A als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der Maximalwert 255 = 2^8 - 1 und der Höchstwert, der von einer GANZZAHL von BYTE verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 16.383 = 2^14 - 1. COL ist in XLCALL.H als 32-Bit-ganzzahlige 32-Bit-Zahl definiert.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen **externen xltypeRef-Verweis** auf die übergebene Spalte zurück. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird **TempActiveColumn12 verwendet,** um die gesamte Spalte B auszuwählen. 
  
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

