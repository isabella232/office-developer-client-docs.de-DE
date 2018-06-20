---
title: XlfUnregister (Formular 2)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfUnregister (Form 2)
keywords:
- Xlfunregister [excel 2007]
localization_priority: Normal
ms.assetid: 39c6eba7-ba41-4e7b-9a28-2b662378ff5a
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0154e380b65b8c57e7e96a98ef131e26b49e203
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790619"
---
# <a name="xlfunregister-form-2"></a>XlfUnregister (Formular 2)

**Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Kann aus einem Befehl DLL oder XLL aufgerufen werden, die selbst von Microsoft Excel aufgerufen wurde. Dies ist gleichbedeutend mit dem **UNREGISTER** aus einer Excel-XLM-Makrovorlage. 
  
**XlfUnregister** kann in zwei Formen aufgerufen werden: 
  
- Formular 1: Hebt die Registrierung einen einzelnen Befehl oder eine Funktion.
    
- Formular 2: Entlädt und eine XLL deaktiviert.
    
In Form 2 aufgerufen, erzwingt diese Funktion eine DLL oder Code-Ressource vollständig entfernt werden. Es hebt die Registrierung aller die Funktionen in einer DLL, auch wenn sie gerade von einem anderen Makro, unabhängig davon, welche die Verwendungszähler verwendet werden. Diese Funktion ruft **XlAutoClose**und hebt die Registrierung klicken Sie dann auf alle Funktionen in der DLL.
  
```cs
Excel12(xlfUnregister, LPXLOPER12 pxRes, 1, LPXLOPER12 pxModuleText);
```

## <a name="parameters"></a>Parameter

_pxModuleText_ (**XltypeStr**)
  
Der Name der DLL.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Wenn erfolgreich ist, gibt **"true"** (**XltypeBool**). Wenn nicht erfolgreich ist, gibt **FALSE**zurück.
  
## <a name="remarks"></a>Hinweise

> [!NOTE] 
> Rufen Sie diese Form der Funktion nicht die Implementierung von der [XlAutoClose](xlautoclose.md) versucht, alle Ressourcen mit einem einfachen Funktionsaufruf die DLL Aufheben der Registrierung auf. Dies führt zu rekursiven Aufruf der **XlAutoClose** und einen Stapelüberlauf. 
  
### <a name="remember-to-delete-names"></a>Denken Sie daran, Namen löschen

Wenn Sie das Argument _PxFunctionText_ **XlfRegister**, bei der Registrierung der DLL Funktionen und Befehle angegeben, Sie müssen explizit löschen die Namen durch Aufrufen von **XlfSetName** für jede Datei das zweite Argument auslassen, damit die Funktion im Funktions-Assistenten wird nicht mehr angezeigt. Weitere Informationen finden Sie unter [Bekannte Probleme bei der Entwicklung von Excel XLL](known-issues-in-excel-xll-development.md).
  
## <a name="see-also"></a>Siehe auch

- [XlfRegister (Formular 1)](xlfregister-form-1.md)
- [xlfRegisterId](xlfregisterid.md)
- [XlfUnregister (Formular 1)](xlfunregister-form-1.md)
- [Wichtige und n�tzliche C-API XLM-Funktionen](essential-and-useful-c-api-xlm-functions.md)

