---
title: xlAutoRemove
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAutoRemove
keywords:
- Xlautoremove-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: fff0de4d-605d-49e6-a5be-a000410c09d8
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 6e5daac21a6d89472a7d84a25e9aeaea56db1ae1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790597"
---
# <a name="xlautoremove"></a>xlAutoRemove

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Wird von Microsoft Excel aufgerufen, wenn der Benutzer mit dem Add-In-Manager die XLL während einer Sitzung Excel deaktiviert. Diese Funktion ist nicht aufgerufen, wenn eine Excel-Sitzung, ordnungsgemäß oder nicht ordnungsgemäß, mit der Add-in installiert wird geschlossen.
  
Diese Funktion kann zum Anzeigen eines benutzerdefinierten Dialogfelds, die den Anwender darüber, dass das Add-in deaktiviert wurde, oder zum Lesen oder Schreiben in die Registrierung, zum Beispiel verwendet werden.
  
Excel erfordert eine XLL zu implementieren und exportieren Sie diese Funktion nicht. 
  
```cs
int WINAPI xlAutoRemove(void);
```

## <a name="parameters"></a>Parameter

Diese Funktion hat keine Argumente.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Implementierung dieser Funktion muss 1 (**Int**) zurückgeben.
  
## <a name="remarks"></a>Hinweise

Verwenden Sie diese Funktion, wenn Ihre XLL muss jede Aufgabe abschließen, wenn es vom Add-In-Manager entfernt wird.
  
## <a name="example"></a>Beispiel

Finden Sie die Dateien `\SAMPLES\EXAMPLE\EXAMPLE.C` und `\SAMPLES\GENERIC\GENERIC.C` beispielsweise Implementierungen von dieser Funktion. Der folgende Code ist aus `\SAMPLES\EXAMPLE\EXAMPLE.C`.
  
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


[Add-In-Manager und Funktionen von XLL-Schnittstelle](add-in-manager-and-xll-interface-functions.md)

