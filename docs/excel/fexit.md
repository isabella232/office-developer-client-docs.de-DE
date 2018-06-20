---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- Fexit-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 3abb5cd68a45fbcd16665dbc4d492d764bbd315e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790493"
---
# <a name="fexit"></a>fExit

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel benutzerdefinierter Befehl, der GENERIC.xll entladen wird. Wenn GENERIC.xll geladen wird, erstellt es ein Menü benutzerdefinierte allgemeine, über die auf diesen Befehl zugegriffen wird. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parameter

Die Funktion akzeptiert keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
## <a name="remarks"></a>Hinweise

Dies ist eine vom Benutzer initiierte Routine GENERIC.xll beenden, sollten Sie einfach aufrufen `UNREGISTER("GENERIC.XLL")` in dieser Funktion. Dies würde erzwingen alle Funktionen in diese DLL aufgehoben, selbst wenn sie an einer beliebigen Stelle else registriert sind. Stattdessen Registrierung aufgehoben werden Sie die Funktionen eines zu einem Zeitpunkt. 
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

