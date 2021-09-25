---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit-Funktion [excel 2007]
ms.localizationpriority: medium
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 8a355955d2d31247fce1d5b875472b0e749e554b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59617237"
---
# <a name="fexit"></a>fExit

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für einen benutzerdefinierten Befehl, mit dem GENERIC.xll entladen wird. Beim Laden von GENERIC.xll wird ein benutzerdefiniertes Menü ( Generic) erstellt, über das auf diesen Befehl zugegriffen wird. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parameter

Die Funktion akzeptiert keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
## <a name="remarks"></a>Bemerkungen

Hierbei handelt es sich um eine vom Benutzer initiierte Routine zum Beenden von GENERIC.xll. Sie sollten es vermeiden,  `UNREGISTER("GENERIC.XLL")` einfach diese Funktion aufzurufen. Dadurch würde die Registrierung aller Funktionen in dieser DLL erzwungen, auch wenn sie an einer anderen Stelle registriert sind. Heben Sie stattdessen die Registrierung der Funktionen nacheinander auf. 
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

