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
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429915"
---
# <a name="fexit"></a>fExit

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für benutzerdefinierten Befehl, der GENERIC.xll auslädt. Wenn GENERIC.xll geladen wird, wird ein benutzerdefiniertes Menü, Generic, erstellt, über das auf diesen Befehl zugegriffen wird. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parameter

Die Funktion nimmt keine Parameter an.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
## <a name="remarks"></a>Hinweise

Dies ist eine vom Benutzer initiierte Routine zum Beenden von GENERIC.xll Sie sollten vermeiden, einfach  `UNREGISTER("GENERIC.XLL")` in dieser Funktion aufrufen. Dadurch würde die Registrierung aller Funktionen in dieser DLL auch dann aufgehoben, wenn sie an einem anderen Ort registriert sind. Aufheben sie stattdessen die Registrierung der Funktionen nach und nach. 
  
### <a name="example"></a>Beispiel

Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

