---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlAutoRemove-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: af8bd2d44883b1820be42b82d4fe4794fa29caab
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425477"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel aufgerufen, wenn der Benutzer die XLL während einer Excel-Sitzung mithilfe des Add-in-Managers deaktiviert. Diese Funktion wird nicht aufgerufen, wenn eine Excel-Sitzung mit dem installierten Add-In (ordnungsgemäß oder unerwartet) beendet wird.
  
Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer mitteilt, dass das Add-in deaktiviert wurde, oder beispielsweise in die Registrierung zu lesen oder zu schreiben.
  
Excel benötigt keine XLL, um diese Funktion zu implementieren und zu exportieren. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).
  
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, wenn Ihre XLL eine Aufgabe ausführen muss, wenn Sie vom Add-in-Manager entfernt wird.
  
## <a name="example"></a>Beispiel

Schauen Sie sich die Dateien `\SAMPLES\EXAMPLE\EXAMPLE.C` und `\SAMPLES\GENERIC\GENERIC.C` für Beispiel-Implementierungen dieser Funktion an. Der folgende Code stammt aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoRemove(void)
{
/* Display a dialog box indicating that the XLL was successfully removed */
   Excel12f(xlcAlert, 0, 2,
      TempStr12(L"Thank you for removing Example.XLL!"),
      TempInt12(2));
   return 1;
}
```

## <a name="see-also"></a>Siehe auch



[xlAutoAdd](xlautoadd.md)


[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

