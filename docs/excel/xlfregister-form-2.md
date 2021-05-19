---
title: xlfRegister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416041"
---
# <a name="xlfregister-form-2"></a>xlfRegister (Formular 2)

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von einem Microsoft Excel. Dies entspricht dem Aufrufen **von REGISTER** aus Excel XLM-Makroblatts. 
  
Die **xlfRegister-Funktion** kann in zwei Formen aufgerufen werden: 
  
- [xlfRegister (Form 1):](xlfregister-form-1.md)Registriert einen einzelnen Befehl oder eine einzelne Funktion.
    
- xlfRegister (Form 2): Lädt und aktiviert eine XLL.
    
In Form 2 aufgerufen, kann diese Funktion nur zum Laden und Aktivieren einer XLL verwendet werden, die eine [xlAutoOpen-Prozedur](xlautoopen.md) enthält. 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameter

 _pxModuleText_ (**xltypeStr**)
  
Der Name der DLL, die geladen und aktiviert werden soll.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn dies erfolgreich ist, wird der Name der DLL (**xltypeStr**) zurückgegeben. Andernfalls wird ein #VALUE! zurück.
  
## <a name="see-also"></a>Siehe auch



[Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

