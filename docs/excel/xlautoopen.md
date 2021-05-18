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
localization_priority: Normal
ms.assetid: 748cecb6-61d0-496b-a1a4-a73d22eb29e2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: bf02f71458f2f4d8514f69a6b6f0921b5318303a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406647"
---
# <a name="xlautoopen"></a>xlAutoOpen

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Rückruffunktion, die von jeder gültigen XLL implementiert und exportiert werden muss. Die **xlAutoOpen-Funktion** ist der empfohlene Ort zum Registrieren von XLL-Funktionen und -Befehlen, Initialisieren von Datenstrukturen, Anpassen der Benutzeroberfläche und so weiter. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).
  
## <a name="remarks"></a>Hinweise

Microsoft Excel **aufruft xlAutoOpen,** wenn die XLL aktiviert wird. Die XLL wird in den folgenden Situationen aktiviert: 
  
- Zu Beginn einer Excel sitzung, wenn sie in der letzten Sitzung aktiv Excel, die normal beendet wurde.
    
- Wird während einer Sitzung Excel geladen.
    
- Eine XLL kann auf verschiedene Weise geladen werden:
    
- Durch Auswählen **von Öffnen** im Menü **Datei** (wobei die Version von Excel diese Methode zum Laden von XLLs unterstützt). 
    
- Verwenden des Add-In-Managers.
    
- Von einer anderen XLL, die [xlfRegister mit](xlfregister-form-1.md) dem Namen dieser DLL als einziges Argument aufruft. 
    
- Aus einem XLM-Makroblatt, das [REGISTER](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument aufruft. 
    
- Wenn das Add-In während einer Excel deaktiviert und reaktiviert wird, wird diese Funktion zur Reaktivierung aufgerufen.
    
### <a name="example"></a>Beispiel

Sehen Sie sich  `SAMPLES\EXAMPLE\EXAMPLE.C` die Dateien und , und beispielsweise  `SAMPLES\GENERIC\GENERIC.C` Implementierungen dieser Funktion an.
  
## <a name="see-also"></a>Siehe auch



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

