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
- tempint12-Funktion [excel 2007], TempInt-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790575"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** , die eine ganze Zahl enthält. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Parameter

 _Ich_
  
Die vorgesehene Integer-Wert. Beachten Sie, dass die **XLOPER** ganze Zahl, eine 16-Bit-Ganzzahl mit Vorzeichen (short Int) ist die **XLOPER12** ganze Zahl ist eine 32-Bit-Ganzzahl ([lange] Int). 
  
## <a name="return-value"></a>R�ckgabewert

Gibt einen Integer **vom Typ XltypeInt** mit dem übergebenen Wert zurück. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempInt12** -Funktion verwendet, um **XlfGetWorkspace**ein Argument übergeben.
  
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

