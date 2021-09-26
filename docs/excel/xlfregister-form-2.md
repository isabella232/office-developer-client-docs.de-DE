---
title: xlfRegister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfregister-Funktion [Excel 2007]
ms.localizationpriority: medium
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: e6268339f9dddff6d61ec843bb7d498fc0710d38
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611168"
---
# <a name="xlfregister-form-2"></a>xlfRegister (Formular 2)

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde. Dies entspricht dem Aufrufen von **REGISTER** aus einer Excel XLM-Makrovorlage. 
  
Die **xlfRegister-Funktion** kann in zwei Formen aufgerufen werden: 
  
- [xlfRegister (Formular 1):](xlfregister-form-1.md)Registriert einen einzelnen Befehl oder eine einzelne Funktion.
    
- xlfRegister (Formular 2): Lädt und aktiviert eine XLL.
    
In Form 2 aufgerufen, kann diese Funktion nur zum Laden und Aktivieren einer XLL verwendet werden, die eine [xlAutoOpen-Prozedur](xlautoopen.md) enthält. 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameter

 _pxModuleText_ (**xltypeStr**)
  
Der Name der zu ladenden und zu aktivierenden DLL.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn dies erfolgreich ist, wird der Name der DLL (**xltypeStr**) zurückgegeben. Andernfalls wird ein #VALUE zurückgegeben! zurück.
  
## <a name="see-also"></a>Siehe auch



[Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

