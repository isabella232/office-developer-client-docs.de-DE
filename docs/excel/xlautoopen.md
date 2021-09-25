---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- xlautoopen-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 443b6511e0935737187994bf0224bd80b84ada21
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59621353"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Rückruffunktion, die von jeder gültigen XLL implementiert und exportiert werden muss. Die **xlAutoOpen-Funktion** ist die empfohlene Stelle, um XLL-Funktionen und -Befehle zu registrieren, Datenstrukturen zu initialisieren, die Benutzeroberfläche anzupassen usw. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).
  
## <a name="remarks"></a>Hinweise

Microsoft Excel ruft **xlAutoOpen** immer dann auf, wenn die XLL aktiviert wird. Die XLL wird in den folgenden Situationen aktiviert: 
  
- Zu Beginn einer Excel Sitzung, wenn sie in der letzten Excel Sitzung aktiv war, die normal endete.
    
- Wenn während einer Excel Sitzung geladen.
    
- Eine XLL kann auf verschiedene Arten geladen werden:
    
- Indem Sie im Menü **"Datei"** die Option **"Öffnen"** auswählen (wobei die Version von Excel diese Methode zum Laden von XLLs unterstützt). 
    
- Verwenden des Add-In-Managers.
    
- Aus einer anderen XLL, die [xlfRegister](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument aufruft. 
    
- Aus einem XLM-Makroblatt, das [REGISTER](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument aufruft. 
    
- Wenn das Add-In während einer Excel Sitzung deaktiviert und reaktiviert wird, wird diese Funktion bei der Reaktivierung aufgerufen.
    
### <a name="example"></a>Beispiel

Sehen Sie sich die Dateien  `SAMPLES\EXAMPLE\EXAMPLE.C` und , und beispielsweise  `SAMPLES\GENERIC\GENERIC.C` Implementierungen dieser Funktion.
  
## <a name="see-also"></a>Siehe auch



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

