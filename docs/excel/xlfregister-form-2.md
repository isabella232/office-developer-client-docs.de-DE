---
title: XlfRegister (Form 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfRegister
keywords:
- XlfRegister-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 3ebbd775-f3d2-4ba7-8835-a5b38ad2267a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a535018e2b644966d183ba9ae862ce83670c9231
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790596"
---
# <a name="xlfregister-form-2"></a>XlfRegister (Form 2)

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann aus einem Befehl DLL oder XLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde. Dies ist gleichbedeutend mit dem **Registrieren** aus einer Excel-XLM-Makrovorlage. 
  
Die Funktion **XlfRegister** kann in zwei Formen aufgerufen werden: 
  
- [XlfRegister (Formular 1)](xlfregister-form-1.md): registriert einen einzelnen Befehl oder eine Funktion.
    
- XlfRegister (Form 2): Lasten und aktiviert eine XLL.
    
In Form 2 aufgerufen wird, kann diese Funktion nur verwendet werden zum Laden und aktivieren eine XLL, eine Prozedur [XlAutoOpen](xlautoopen.md) enthält. 
  
```cs
Excel12(xlfRegister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameter

 _pxModuleText_ (**XltypeStr**)
  
Der Name der DLL geladen und aktiviert werden.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Bei erfolgreicher zurückgegeben dies der Name der DLL (**XltypeStr**). Andernfalls gibt es eine #VALUE! Fehler.
  
## <a name="see-also"></a>Siehe auch



[Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

