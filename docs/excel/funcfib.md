---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- Funcfib-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 4f1fceedaf7e152fbbfd5e708d9da55e161f43ba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552220"
---
# <a name="funcfib"></a>FuncFib

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für eine benutzerdefinierte Arbeitsblattfunktion, die die Nth Fibonacci-Zahl berechnet. Wenn GENERIC.xll geladen wird, wird diese Funktion registriert, sodass sie aus dem Arbeitsblatt aufgerufen werden kann.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Parameter

 _pxN_ (**LPXLOPER12**)
  
Der Wert von N, für den die N-te Fibonacci-Nummer erforderlich ist.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

(**xltypeNum LPXLOPER12** if successful or **xltypeErr** otherwise) 
  
Die N-te Fibonacci-Nummer.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Funktion verwendet eine statische Variable, die innerhalb des Funktionsblocks als Rückgabewert **XLOPER12** definiert ist. Dies ist nicht threadsicher, und daher sollten diese Funktion und alle Arbeitsblattfunktionen, die diese Strategie zum Zurückgeben von **XLOPER** s oder **XLOPER12** verwenden, ab Excel 2007 nicht als threadsicher registriert werden.
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

