---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- Funcfib-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 8d1c97ea57e968aaedffca6b37ded3d875e87413
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790501"
---
# <a name="funcfib"></a>FuncFib

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel Arbeitsblatt benutzerdefinierte Funktion, die die n-te Fibonacci-Zahl berechnet. Wenn GENERIC.xll geladen wird, registriert sie diese Funktion, damit sie aus dem Arbeitsblatt aufgerufen werden kann.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Parameter

 _pxN_ (**LPXLOPER12**)
  
Der Wert von N für die die n-te Fibonacci-Zahl erforderlich ist.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

(**XltypeNum LPXLOPER12** bei erfolgreicher oder **XltypeErr** andernfalls) 
  
Die n-te Fibonacci-Zahl.
  
## <a name="remarks"></a>Hinweise

Die Funktion verwendet eine statische Variable in der Funktionsblock als Rückgabewert **XLOPER12**definiert sind. Dies ist nicht threadsicheren und also diese Funktion und alle Arbeitsblattfunktion, die diese Strategie verwendet für die Rückgabe **XLOPER**s oder **XLOPER12**s, sollten nicht registriert werden als threadsicheren ab Excel 2007.
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

