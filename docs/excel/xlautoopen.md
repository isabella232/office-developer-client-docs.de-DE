---
title: xlAutoOpen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoOpen
keywords:
- xlAutoOpen-Funktion [Excel 2007]
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
  
Rückruffunktion, die von jeder gültigen XLL implementiert und exportiert werden muss. Die **xlAutoOpen** -Funktion wird empfohlen, um die XLL-Funktionen und-Befehle zu registrieren, Datenstrukturen zu initialisieren, die Benutzeroberfläche anzupassen usw. 
  
```cs
int WINAPI xlAutoOpen(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).
  
## <a name="remarks"></a>Hinweise

Microsoft Excel ruft **xlAutoOpen** auf, wenn die XLL aktiviert wird. Die XLL wird in den folgenden Situationen aktiviert: 
  
- Am Anfang einer Excel-Sitzung, wenn Sie in der letzten Excel-Sitzung aktiv war, die normal beendet wurde.
    
- Wenn es während einer Excel-Sitzung geladen wird.
    
- Eine XLL kann auf verschiedene Arten geladen werden:
    
- Durch Auswählen von **Öffnen** im Menü **Datei** (wobei die Version von Excel diese Methode zum Laden von XLLs unterstützt). 
    
- Verwenden des Add-In-Managers.
    
- Von einer anderen XLL, die [xlfRegister](xlfregister-form-1.md) mit dem Namen dieser DLL als das einzige Argument aufruft. 
    
- Aus einem XML-Makroblatt, das [Register](xlfregister-form-1.md) mit dem Namen dieser DLL als einziges Argument aufruft. 
    
- Wenn das Add-in während einer Excel-Sitzung deaktiviert und reaktiviert wird, wird diese Funktion bei der Reaktivierung aufgerufen.
    
### <a name="example"></a>Beispiel

Sehen Sie sich `SAMPLES\EXAMPLE\EXAMPLE.C` die `SAMPLES\GENERIC\GENERIC.C`Dateien und, und zum Beispielimplementierungen dieser Funktion an.
  
## <a name="see-also"></a>Siehe auch



[xlAutoClose](xlautoclose.md)
  
[xlAutoRegister/xlAutoRegister12](xlautoregister-xlautoregister12.md)


[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

