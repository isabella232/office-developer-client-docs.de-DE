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
ms.localizationpriority: medium
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 449886c9f0be9adad6af5dc6c6163eb8f0f64a4f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557680"
---
# <a name="funcsum"></a>FuncSum

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für eine benutzerdefinierte Arbeitsblattfunktion, die 1 bis 29 Argumente akzeptiert und deren Summe berechnet. Jedes Argument kann eine einzelne Zahl, ein Bereich oder ein Array sein. Wenn GENERIC.xll geladen wird, wird diese Funktion registriert, sodass sie aus dem Arbeitsblatt aufgerufen werden kann. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Parameter

 _px1-px29_ (**LPXLOPER12**)
  
Zeiger auf **XLOPER12-Argumente.** Die Funktion akzeptiert jede Art von Eingabetyp, ist jedoch nur für den Betrieb mit Zahlen, Literalarrays von Zahlen und Bereichen codiert, die nur Zahlen oder leere Zellen enthalten. Wenn weniger als 29 Argumente angegeben werden, werden die verbleibenden Argumente als **xltypeMissing** angegeben.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

(**LPXLOPER12 xltypeNum** oder **xltypeErr**)
  
Die Summe der Argumente oder #VALUE! wenn die angegebene Argumentliste oder eine Zelle in einem Bereich oder Element in einem Array nicht numerisch ist.
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

