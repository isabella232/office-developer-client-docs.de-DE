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
- tempint12-Funktion [excel 2007],TempInt-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 390de41b38b10d3ab794c615824bd8b32cbdbb32
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59572361"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Frameworkbibliotheksfunktion, die eine temporäre **XLOPER** /  **XLOPER12** erstellt, die eine ganze Zahl enthält. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Parameter

 _Ich_
  
Der beabsichtigte ganzzahlige Wert. Beachten Sie, dass die **XLOPER-Ganzzahl** eine 16-Bit-Ganzzahl mit Vorzeichen (short int) ist, während die **xloper12-Ganzzahl** eine 32-Bit-Ganzzahl mit Vorzeichen ([long] int) ist. 
  
## <a name="return-value"></a>Rückgabewert

Gibt eine **xltypeInt-Ganzzahl** zurück, die den übergebenen Wert enthält. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempInt12** -Funktion verwendet, um ein Argument an **xlfGetWorkspace** zu übergeben.
  
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

