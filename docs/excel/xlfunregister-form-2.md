---
title: xlfUnregister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- xlfunregister [Excel 2007]
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
  
Kann von einem DLL-oder XLL-Befehl aufgerufen werden, der selbst von Microsoft Excel aufgerufen wurde. Dies entspricht dem Aufrufen der **AUFheben der Registrierung** aus einer Excel-XML-Makrovorlage. 
  
**xlfUnregister** kann in zwei Formen aufgerufen werden: 
  
- Form 1: hebt die Registrierung eines einzelnen Befehls oder einer Funktion auf.
    
- Form 2: entladen und Deaktivieren einer XLL.
    
In Form 2 aufgerufen, wird durch diese Funktion erzwungen, dass eine DLL oder Coderessource vollständig entladen wird. Sie hebt die Registrierung aller Funktionen in einer DLL auf, auch wenn Sie derzeit von einem anderen Makro verwendet werden, unabhängig davon, welche Verwendungsanzahl verwendet wird. Diese Funktion ruft **xlAutoClose**auf und hebt dann alle Funktionen in der dll auf.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**xltypeStr**)
  
Der Name der DLL.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Wenn der Wert erfolgreich ist, wird **true** (**xltypeBool**) zurückgegeben. Wenn nicht erfolgreich, gibt **false**zurück.
  
## <a name="remarks"></a>Bemerkungen

> [!NOTE] 
> Rufen Sie diese Form der Funktion nicht aus der Implementierung des [xlAutoClose](xlautoclose.md) auf, um die Registrierung aller Ressourcen der DLL mit einem einfachen Funktionsaufruf aufzuheben. Dies führt zu einem rekursiven Aufruf von **xlAutoClose** und einem Stapelüberlauf. 
  
### <a name="remember-to-delete-names"></a>Namen löschen

Wenn Sie das _pxFunctionText_ -Argument für **xlfRegister**angegeben haben, müssen Sie beim Registrieren der DLL-Funktionen und-Befehle die Namen explizit löschen, indem Sie **xlfSetName** für jeden einzelnen aufrufen, wobei das zweite Argument ausgelassen wird, sodass die die Funktion wird nicht mehr im Funktions-Assistenten angezeigt. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Excel-XLL-Entwicklung](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Siehe auch

- [xlfRegister (Formular 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [xlfUnregister (Formular 1)](xlfunregister-form-1.md)
- [Wichtige und nützliche C-API-XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

