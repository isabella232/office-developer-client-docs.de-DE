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
- tempnum12-Funktion [excel 2007], TempNum-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790572"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliothek-Funktion, die eine temporäre **XLOPER**erstellt/ **XLOPER12** mit einer Microsoft Excel-Arbeitsblatt-Zahl (einer IEEE-8-Byte-Double). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Parameter

 _d_ (**double**)
  
Der vorgesehene Wert. Beachten Sie, dass IEEE Unterseite normale Zahlen derzeit nicht unterstützt werden und sind auf 0 (null) gerundet. Negativ unendlich wird unterstützt.
  
## <a name="return-value"></a>R�ckgabewert

Gibt einen numerischen **XltypeNum** mit dem Wert übergeben, oder NULL, wenn der übergebene Wert Unterseite normalen wurde. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempNum12** -Funktion verwendet, um **XlfGetWorkspace**ein Argument übergeben.
  
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

