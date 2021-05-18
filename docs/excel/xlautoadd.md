---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- xlautoadd-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9a38d5dafd30fda87dda5eadf8fa97ab6e6768a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413759"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Hinzugefügt von Microsoft Excel, wenn der Benutzer die XLL während einer Excel mit dem Add-In aktiviert. Diese Funktion wird nicht aufgerufen, Excel gestartet und ein vorinstalliertes Add-In geladen wird.
  
Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, in dem der Benutzer informiert wird, dass das Add-In aktiviert wurde, oder um aus der Registrierung zu lesen oder in die Registrierung zu schreiben oder z. B. Lizenzierungsinformationen zu überprüfen.
  
Excel erfordert keine XLL, um diese Funktion zu implementieren und zu exportieren.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Ihre Implementierung dieser Funktion sollte 1 zurückgeben. (**int**).
  
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, wenn Ihre XLL etwas tun muss, wenn sie vom Add-In hinzugefügt wird.
  
## <a name="example"></a>Beispiel

Sehen  `\SAMPLES\EXAMPLE\EXAMPLE.C` Sie sich beispielsweise  `\SAMPLES\GENERIC\GENERIC.C` Implementierungen dieser Funktion an. Der folgende Code stammt aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
```cs
int WINAPI xlAutoAdd(void)
{
    XCHAR szBuf[255];
    wsprintfW((LPWSTR)szBuf, L"Thank you for adding Example.XLL\n"
            L"build date %hs, time %hs",__DATE__, __TIME__);
/* Display a dialog indicating that the XLL was successfully added */
    Excel12f(xlcAlert, 0, 2, TempStr12(szBuf), TempInt12(2));
    return 1;
}
```

## <a name="see-also"></a>Siehe auch



[xlAutoRemove](xlautoremove.md)


[Add-In-Manager und XLL-Benutzeroberflächenfunktionen](add-in-manager-and-xll-interface-functions.md)

