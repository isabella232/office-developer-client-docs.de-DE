---
title: FuncFib
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncFib
keywords:
- funcfib-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 6a719f04-b2d1-4f87-a227-be561cbd3e49
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb8f0c12c27fb2c95007eb5006c1d8b90970f3ad
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423671"
---
# <a name="funcfib"></a>FuncFib

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für eine benutzerdefinierte Arbeitsblattfunktion, die die n-te Fibonacci-Zahl berechnet. Wenn generische. XLL geladen wird, wird diese Funktion registriert, sodass Sie vom Arbeitsblatt aufgerufen werden kann.
  
```cs
LPXLOPER12 WINAPI FuncFib (LPXLOPER12 pxN);
```

## <a name="parameters"></a>Parameter

 _pxN_ (**LPXLOPER12**)
  
Der Wert von N, für den die te Fibonacci-Zahl erforderlich ist.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

(**XLTYPENUM LPXLOPER12** wenn erfolgreich oder **xltypeErr** andernfalls) 
  
Die n-te Fibonacci-Zahl.
  
## <a name="remarks"></a>Bemerkungen

Die Funktion verwendet eine statische Variable, die innerhalb des Funktionsblocks als Rückgabewert **XLOPER12**definiert ist. Dies ist nicht threadsicher, und diese Funktion und jede Arbeitsblattfunktion, die diese Strategie zum Zurückgeben von **XLOPER**s oder **XLOPER12**s verwendet, sollten ab Excel 2007 nicht als threadsicher registriert werden.
  
### <a name="example"></a>Beispiel

Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

