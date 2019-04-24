---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- tempnum12-Funktion [Excel 2007], TempNum-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310360"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, mit der ein temporäres **XLOPER**/ -**XLOPER12** mit einer Microsoft Excel-Arbeitsblatt Nummer (ein IEEE 8-Byte-Double) erstellt wird. 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Parameter

 _d_ (**Double**)
  
Der vorgesehene Wert. Beachten Sie, dass IEEE-Sub-normal zahlen derzeit nicht unterstützt werden und auf NULL gerundet werden. Negative Unendlichkeit wird unterstützt.
  
## <a name="return-value"></a>Rückgabewert

Gibt eine numerische **XltypeNum** zurück, die den übergebenen Wert enthält, oder NULL, wenn der übergebene Wert unter normal ist. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempNum12** -Funktion verwendet, um ein Argument an **xlfGetWorkspace**zu übergeben.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

