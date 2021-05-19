---
title: xlfUnregister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8bf1151e1ba4c165e784b88dce80096a2eaa62de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419905"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (Formular 2)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von einem Microsoft Excel. Dies entspricht dem Aufrufen von **UNREGISTER** aus Excel XLM-Makroblatts. 
  
**xlfUnregister** kann in zwei Formen aufgerufen werden: 
  
- Formular 1: Aufheben der Registrierung eines einzelnen Befehls oder einer Einzelnen Funktion.
    
- Formular 2: Entladen und Deaktivieren einer XLL.
    
In Form 2 aufgerufen, erzwingt diese Funktion, dass eine DLL- oder Coderessource vollständig entladen wird. Es wird die Registrierung aller Funktionen in einer DLL aufgehoben, auch wenn sie derzeit von einem anderen Makro verwendet werden, unabhängig von der Anzahl der Verwendungen. Diese Funktion ruft **xlAutoClose** auf und macht dann die Registrierung aller Funktionen in der DLL aufgehoben.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**xltypeStr**)
  
Der Name der DLL.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn dies erfolgreich ist, wird **TRUE** (**xltypeBool**) zurückgegeben. Wenn der Wert nicht erfolgreich ist, wird **FALSE zurückgegeben.**
  
## <a name="remarks"></a>Hinweise

> [!NOTE] 
> Rufen Sie diese Form der Funktion nicht aus Ihrer Implementierung von [xlAutoClose](xlautoclose.md) auf, um die Registrierung aller Ressourcen der DLL mit einem einfachen Funktionsaufruf auf zu aufheben. Dies führt zu rekursiven Aufrufen von **xlAutoClose** und einem Stapelüberlauf. 
  
### <a name="remember-to-delete-names"></a>Vergessen Sie nicht, Namen zu löschen

Wenn Sie das  _Argument pxFunctionText_ für **xlfRegister** angegeben haben, müssen Sie beim Registrieren der Funktionen und Befehle der DLL die Namen explizit löschen, indem Sie **xlfSetName** für jedes Argument aufrufen und das zweite Argument auslassen, sodass die Funktion nicht mehr im Funktions-Assistenten angezeigt wird. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Siehe auch

- [xlfRegister (Formular 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formular 1)](xlfunregister-form-1.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

