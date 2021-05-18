---
title: Func1
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Func1
keywords:
- func1-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a3d3c6bbd529f43bd75b31b9348498928390a8f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408915"
---
# <a name="func1"></a>Func1

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für eine benutzerdefinierte Arbeitsblattfunktion veranschaulicht die Rückgabe eines statischen Zeichenfolgenwerts. Wenn GENERIC.xll geladen wird, registriert es diese Funktion, sodass sie aus dem Arbeitsblatt aufgerufen werden kann.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Parameter

 _px_ (**LPXLOPER**)
  
Dieses Argument wird ignoriert und dient nur zum Auslösen von Microsoft Excel zum Aufrufen der Funktion.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 **LPXLOPER12**: Immer die Zeichenfolge "Func1"
  
### <a name="example"></a>Beispiel

Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

