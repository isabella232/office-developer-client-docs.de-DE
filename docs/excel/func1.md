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
ms.localizationpriority: medium
ms.assetid: 801b14ef-0be8-4b97-919d-a9d413705d1c
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ec4d0646cb1525f517a57ace5cee52325548cec0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59552227"
---
# <a name="func1"></a>Func1

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für eine benutzerdefinierte Arbeitsblattfunktion veranschaulicht die Rückgabe eines statischen Zeichenfolgenwerts. Wenn GENERIC.xll geladen wird, wird diese Funktion registriert, sodass sie aus dem Arbeitsblatt aufgerufen werden kann.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Parameter

 _px_ (**LPXLOPER**)
  
Dieses Argument wird ignoriert und dient nur dazu, Microsoft Excel zum Aufrufen der Funktion auszulösen.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

 **LPXLOPER12**: Immer die Zeichenfolge "Func1"
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

