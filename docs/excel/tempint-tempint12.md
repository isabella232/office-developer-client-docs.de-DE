---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- tempint12-Funktion [Excel 2007], TempInt-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310479"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, die eine temporäre **XLOPER**/ -**XLOPER12** erstellt, die eine ganze Zahl enthält. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Parameter

 _i_
  
Der vorgesehene ganzzahlige Wert. Beachten Sie, dass die **XLOPER** -Ganzzahl eine signierte 16-Bit-Ganzzahl (short int) ist, wohingegen die **XLOPER12** -ganzzahl eine signierte 32-Bit-Ganzzahl ([Long] int) ist. 
  
## <a name="return-value"></a>Rückgabewert

Gibt eine **xltypeInt** -Ganzzahl zurück, die den übergebenen Wert enthält. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempInt12** -Funktion verwendet, um ein Argument an **xlfGetWorkspace**zu übergeben.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>Siehe auch



[Funktionen in der Framework-Klassenbibliothek](functions-in-the-framework-library.md)

