---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- xlautoremove-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5d86d08d05070adb127282cd07a496498fff0567
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59557589"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel aufgerufen, wenn der Benutzer die XLL während einer Excel Sitzung mithilfe des Add-In-Managers deaktiviert. Diese Funktion wird nicht aufgerufen, wenn eine Excel-Sitzung mit dem installierten Add-In (ordnungsgemäß oder unerwartet) beendet wird.
  
Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, in dem der Benutzer informiert wird, dass das Add-In deaktiviert wurde, oder um beispielsweise aus der Registrierung zu lesen oder in die Registrierung zu schreiben.
  
Excel erfordert keine XLL, um diese Funktion zu implementieren und zu exportieren. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 zurückgeben (**Int**).
  
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, wenn Ihre XLL eine Aufgabe ausführen muss, wenn sie vom Add-In-Manager entfernt wird.
  
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

