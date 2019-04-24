---
title: xlfRegister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- xlfRegister-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 66af741456ab763ef346a8777429f0ae1be77c11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310122"
---
# <a name="xlfregister-form-2"></a>xlfRegister (Formular 2)

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann von einem DLL-oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde. Dies entspricht dem Aufrufen von **Register** aus einer Excel-XML-Makrovorlage. 
  
Die **xlfRegister** -Funktion kann in zwei Formen aufgerufen werden: 
  
- [xlfRegister (Formular 1)](xlfregister-form-1.md): registriert einen einzelnen Befehl oder eine Funktion.
    
- xlfRegister (Formular 2): lädt und aktiviert eine XLL.
    
Diese Funktion kann nur zum Laden und Aktivieren einer XLL mit einer [xlAutoOpen](xlautoopen.md) -Prozedur verwendet werden. 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameter

 _pxModuleText_ (**xltypeStr**)
  
Der Name der DLL, die geladen und aktiviert werden soll.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Bei erfolgreicher Ausführung gibt dieser Wert den Namen der DLL (**xltypeStr**) zurück. Andernfalls wird ein #VALUE zurückgegeben. zurück.
  
## <a name="see-also"></a>Siehe auch



[Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

