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
- tempactivecell12 function [excel 2007],TempActiveCell function [Excel 2007]
ms.localizationpriority: medium
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 70222ff1e057427d6964ea6cae166f1ad08481ef
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611273"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktionen, die einen temporären **XLOPER** /  **XLOPER12** erstellen, der einen externen Verweis auf eine Zelle im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Parameter

 _Zeile_
  
Die Zeile, auf die verwiesen werden soll. Zeilenargumente sind nullbasiert, sodass Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, beträgt der Maximalwert 65.535 = 2^16 - 1 und ist der Maximalwert, der von einer ganzzahligen WORD-Zahl verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, beträgt der Maximalwert 1.048.575 = 2^20 - 1. RW ist in XLCALL.H als 32-Bit-Ganzzahl mit Vorzeichen definiert.
  
 _Col_
  
Die Spalte, auf die verwiesen werden soll. Dies ist nullbasiert, sodass Spalte A als 0 übergeben wird. In Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, beträgt der Maximalwert 255 = 2^8 - 1 und ist der Maximalwert, der von einer ganzzahligen BYTE-Zahl verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, beträgt der Maximalwert 16.383 = 2^14 - 1. COL ist in XLCALL.H als 32-Bit-Ganzzahl mit Vorzeichen definiert.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen externen **XltypeRef-Verweis** auf die übergebene Zelle zurück. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel **wird TempActiveCell12** verwendet, um den Inhalt von B94 im aktiven Blatt anzuzeigen. 
  
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

