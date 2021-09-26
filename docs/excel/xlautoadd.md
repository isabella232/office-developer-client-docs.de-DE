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
ms.localizationpriority: medium
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 574d5f446ec4114cfbf94bea984fb0df92f072f0
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59611216"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel hinzugefügt, wenn der Benutzer die XLL während einer Excel Sitzung mithilfe des Add-In-Managers aktiviert. Diese Funktion wird nicht aufgerufen, wenn Excel gestartet wird und ein vorinstalliertes Add-In lädt.
  
Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer mitteilt, dass das Add-In aktiviert wurde, oder zum Lesen aus der Registrierung oder zum Schreiben in die Registrierung oder zum Überprüfen von Lizenzierungsinformationen, z. B.
  
Excel erfordert keine XLL, um diese Funktion zu implementieren und zu exportieren.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion sollte 1 zurückgeben. (**int**).
  
## <a name="remarks"></a>Bemerkungen

Verwenden Sie diese Funktion, wenn ihre XLL etwas tun muss, wenn sie vom Add-In-Manager hinzugefügt wird.
  
## <a name="example"></a>Beispiel

Sehen Sie sich  `\SAMPLES\EXAMPLE\EXAMPLE.C`  `\SAMPLES\GENERIC\GENERIC.C` implementierungsbeispiele dieser Funktion an. Der folgende Code stammt aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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

