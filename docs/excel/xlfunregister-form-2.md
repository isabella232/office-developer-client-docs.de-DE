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
ms.localizationpriority: medium
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: ae5188743e4aff9f187e0daff86fc9c78ec32a67
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605560"
---
# <a name="xlfunregister-form-2"></a>xlfUnregister (Formular 2)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann über einen DLL- oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde. Dies entspricht dem Aufrufen von **UNREGISTER** aus einer Excel XLM-Makrovorlage. 
  
**xlfUnregister** kann in zwei Formen aufgerufen werden: 
  
- Formular 1: Hebt die Registrierung eines einzelnen Befehls oder einer einzelnen Funktion auf.
    
- Formular 2: Entlädt und deaktiviert eine XLL.
    
In Form 2 aufgerufen, erzwingt diese Funktion, dass eine DLL- oder Coderessource vollständig entladen wird. Es hebt die Registrierung aller Funktionen in einer DLL auf, auch wenn sie derzeit von einem anderen Makro verwendet werden, unabhängig von der Anzahl der Verwendungen. Diese Funktion ruft **xlAutoClose** auf und hebt dann die Registrierung aller Funktionen in der DLL auf.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**xltypeStr**)
  
Der Name der DLL.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn erfolgreich, **gibt TRUE** (**xltypeBool**). Wenn dies nicht erfolgreich ist, wird **FALSE zurückgegeben.**
  
## <a name="remarks"></a>HinwBemerkungeneise

> [!NOTE] 
> Rufen Sie diese Form der Funktion nicht aus der Implementierung von [xlAutoClose](xlautoclose.md) auf, um die Registrierung aller DLL-Ressourcen mit einem einfachen Funktionsaufruf aufzuheben. Dies führt zu rekursivem Aufruf von **xlAutoClose** und einem Stapelüberlauf. 
  
### <a name="remember-to-delete-names"></a>Denken Sie daran, Namen zu löschen

Wenn Sie das  _Argument pxFunctionText_ für **xlfRegister** angegeben haben, müssen Sie beim Registrieren der Funktionen und Befehle der DLL die Namen explizit löschen, indem Sie **xlfSetName** für jedes Argument aufrufen und das zweite Argument weglassen, sodass die Funktion nicht mehr im Funktions-Assistenten angezeigt wird. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Siehe auch

- [xlfRegister (Formular 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formular 1)](xlfunregister-form-1.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

