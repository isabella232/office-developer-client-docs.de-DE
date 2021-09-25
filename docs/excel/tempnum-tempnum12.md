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
- tempnum12-Funktion [excel 2007],TempNum-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 2aad64b2058456eb3e0908387091dcfbc11d284e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605603"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Framework-Bibliotheksfunktion, die einen temporären **XLOPER** /  **XLOPER12** erstellt, der eine Microsoft Excel Arbeitsblattnummer (ein IEEE 8-Byte-Double) enthält. 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Parameter

 _d_ (**double**)
  
Der beabsichtigte Wert. Beachten Sie, dass IEEE-Subnormale Zahlen derzeit nicht unterstützt werden und auf Null gerundet werden. Negative Unendlichkeit wird unterstützt.
  
## <a name="return-value"></a>Rückgabewert

Gibt einen numerischen **XltypeNum-Wert** zurück, der den übergebenen Wert enthält, oder null, wenn der übergebene Wert unternormal war. 
  
## <a name="example"></a>Beispiel

In diesem Beispiel wird die **TempNum12** -Funktion verwendet, um ein Argument an **xlfGetWorkspace** zu übergeben.
  
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

