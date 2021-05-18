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
- tempactivecell12-Funktion [excel 2007],TempActiveCell-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: ac5a200d-32d5-4313-9a6d-d730032aaf10
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f9bdb4cd9919d0e52654a3996ede99c4d1b35cc6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413192"
---
# <a name="tempactivecelltempactivecell12"></a>TempActiveCell/TempActiveCell12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktionen, die eine temporäre **XLOPER** /  **XLOPER12** erstellen, die einen externen Verweis auf eine Zelle im aktiven Blatt enthält. 
  
```cs
LPXLOPER TempActiveCell(WORD row, BYTE col);
LPXLOPER12 TempActiveCell12(RW row, COL co);
```

## <a name="parameters"></a>Parameter

 _row_
  
Die Zeile, auf die verwiesen werden soll. Zeilenargumente sind nullbasierte, sodass Zeile 1 als 0 übergeben wird. In Microsoft Office Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der höchstwert 65.535 = 2^16 - 1 und der Höchstwert, der von einer ganzzahligen WORD-Zahl verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 1.048.575 = 2^20 - 1. RW ist in XLCALL.H als 32-Bit-ganze Zahl mit Vorzeichen definiert.
  
 _col_
  
Die Spalte, auf die verwiesen werden soll. Dies ist nullbasierte, sodass Spalte A als 0 übergeben wird. In Excel 2003 und früheren Versionen und ab Excel 2007, in dem eine Arbeitsmappe im Kompatibilitätsmodus ausgeführt wird, ist der Maximalwert 255 = 2^8 – 1 und der Höchstwert, der von einer ganzzahligen BYTE verwendet werden kann. Ab Excel 2007, in dem eine Arbeitsmappe ausgeführt wird, ist der maximale Wert 16.383 = 2^14 - 1. COL ist in XLCALL.H als 32-Bit-ganzzahlige 32-Bit-Zahl definiert.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen **externen xltypeRef-Verweis** auf die übergebene Zelle zurück. 
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird **TempActiveCell12 verwendet,** um den Inhalt von B94 auf dem aktiven Blatt anzuzeigen. 
  
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

