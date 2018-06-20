---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- Funcsum-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790509"
---
# <a name="funcsum"></a>FuncSum

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel benutzerdefinierter Arbeitsblattfunktion, die von 1 bis 29 Argumente und berechnet die Summe. Jedes Argument kann es sich um eine einzelne Zahl, einem Bereich oder ein Array sein. Wenn GENERIC.xll geladen wird, registriert sie diese Funktion, damit sie aus dem Arbeitsblatt aufgerufen werden kann. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Parameter

 _px1 px29_ (**LPXLOPER12**)
  
Zeiger auf **XLOPER12** Argumente. Die Funktion akzeptiert jede Art von Eingabetyp jedoch nur, um auf Zahlen, Literale Arrays von Zahlen und Bereiche, die nur Zahlen oder leere Zellen enthält angewendet werden codiert wird. Wenn weniger als 29 Argumente angegeben werden, sind die übrigen Argumente als **XltypeMissing**bereitgestellt.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

(**LPXLOPER12 XltypeNum** oder **XltypeErr**)
  
Die Summe der Argumente oder #VALUE! Wenn nicht-numerische Werte in der angegebenen Argumentliste oder in einer Zelle in einem Bereich oder das Element in einem Array vorhanden sind.
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

