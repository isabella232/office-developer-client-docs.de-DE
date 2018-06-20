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
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 26439f1fb05aae2077844ce19935d9ff99e4f701
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790503"
---
# <a name="func1"></a>Func1

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Benutzerdefinierte Tabellenfunktion Beispiel veranschaulicht die Rückgabe von einen statischen String-Wert. Wenn GENERIC.xll geladen wird, registriert sie diese Funktion, damit sie aus dem Arbeitsblatt aufgerufen werden kann.
  
```cs
LPXLOPER12 WINAPI Func1(LPXLOPER12 px);
```

## <a name="parameters"></a>Parameter

 _px_ (**LPXLOPER**)
  
Dieses Argument wird ignoriert, und nur für Microsoft Excel die Funktion Trigger dient.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

 **LPXLOPER12**: immer die Zeichenfolge "Func1"
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

