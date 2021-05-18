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
- tempactiverow-Funktion [excel 2007],TempActiveRow12-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: cbb9181c-59b0-4133-a085-94a94ac3f229
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 1f89c458a521b41e4f172f8a6c53526440bb472b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413108"
---
# <a name="tempactiverowtempactiverow12"></a>TempActiveRow/TempActiveRow12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktionen, die eine temporäre **XLOPER** /  **XLOPER12** erstellen, die einen externen Verweis auf eine gesamte Zeile im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveRow(WORD row);
LPXLOPER12 TempActiveRow12(ROW row);
```

## <a name="parameters"></a>Parameter

 _row_
  
Die Zeile, auf die verwiesen werden soll. Zeilenargumente sind nullbasierte, sodass Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der höchstwert 65.535 = 2^16 - 1 und der Höchstwert, der von einer ganzzahligen WORD-Zahl verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 1.048.575 = 2^20 - 1. RW ist in XLCALL.H als 32-Bit-ganze Zahl mit Vorzeichen definiert.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen **externen xltypeRef-Verweis** auf die übergebenen Zeilenzellen zurück. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempActiveRow12-Funktion** verwendet, um Zeile 113 auszuwählen. 
  
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

