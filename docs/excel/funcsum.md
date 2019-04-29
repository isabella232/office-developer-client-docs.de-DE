---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- funcsum-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406941"
---
# <a name="funcsum"></a>FuncSum

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für eine benutzerdefinierte Arbeitsblattfunktion, die 1 bis 29 Argumente verwendet und deren Summe berechnet. Jedes Argument kann eine einzelne Zahl, ein Bereich oder ein Array sein. Wenn generische. XLL geladen wird, wird diese Funktion registriert, sodass Sie vom Arbeitsblatt aufgerufen werden kann. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Parameter

 _PX1-px29_ (**LPXLOPER12**)
  
Zeiger auf **XLOPER12** -Argumente. Die Funktion akzeptiert jede Art von Eingabetyp, ist jedoch nur codiert, um Zahlen, Literale Arrays von Zahlen und Bereichen zu verwenden, die nur Zahlen oder leere Zellen enthalten. Wenn weniger als 29 Argumente angegeben werden, werden die restlichen Argumente als **xltypeMissing**angegeben.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

(**LPXLOPER12 xltypeNum** oder **xltypeErr**)
  
Die Summe der Argumente oder #VALUE! Wenn es sich nicht um numerische Werte in der angegebenen Argumentliste oder in einer Zelle in einem Bereich oder Element in einem Array handelt.
  
### <a name="example"></a>Beispiel

Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

