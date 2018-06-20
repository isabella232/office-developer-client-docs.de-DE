---
title: xlAutoAdd
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoAdd
keywords:
- Xlautoadd-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: c69299af-a28a-44d9-be10-9c9fb92e21f2
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: ae0b4ae2d5f5fc58c3e18ffa9d79ec4128cb4639
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790579"
---
# <a name="xlautoadd"></a>xlAutoAdd

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Von Microsoft Excel hinzugefügt, wenn der Benutzer die XLL während einer Sitzung Excel aktiviert, mit dem Add-In-Manager. Diese Funktion wird nicht aufgerufen, wenn Excel gestartet und ein vorinstallierte Add-In lädt.
  
Diese Funktion kann verwendet werden, um ein benutzerdefiniertes Dialogfeld anzuzeigen, das dem Benutzer teilt mit, dass das Add-In aktiviert wurde, oder zum Lesen oder Schreiben in die Registrierung Lizenzinformationen, beispielsweise überprüfen.
  
Excel erfordert eine XLL zu implementieren und exportieren Sie diese Funktion nicht.
  
```cs
int WINAPI xlAutoAdd(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

1 sollte die Implementierung von dieser Funktion zurückgegeben werden. (**Int**).
  
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, wenn vorhanden ist nichts, die Ihre XLL benötigt, wenn es vom Add-In-Manager hinzugefügt wird.
  
## <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\EXAMPLE\EXAMPLE.C` und `\SAMPLES\GENERIC\GENERIC.C` beispielsweise Implementierungen von dieser Funktion. Der folgende Code ist aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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


[Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)

