---
title: fExit
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fExit
keywords:
- fexit-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: d85685fa-df70-45bb-b629-a9d43b5cb926
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 97f0a1ec797176fb51c87c58f94e46a323ae5b32
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310857"
---
# <a name="fexit"></a>fExit

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für einen benutzerdefinierten Befehl, der generische. XLL entlädt. Wenn GENERIC. XLL geladen wird, wird ein benutzerdefiniertes Menü generisch erstellt, über das auf diesen Befehl zugegriffen wird. 
  
```cs
int WINAPI fExit(void);
```

## <a name="parameters"></a>Parameter

Die Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
## <a name="remarks"></a>Bemerkungen

Hierbei handelt es sich um eine vom Benutzer initiierte Routine zum Beenden von GENERIC. XLL `UNREGISTER("GENERIC.XLL")` . Dadurch werden die Registrierung aller Funktionen in dieser DLL erzwungen, auch wenn Sie an einer anderen Stelle registriert sind. Heben Sie die Registrierung der Funktionen stattdessen einzeln auf. 
  
### <a name="example"></a>Beispiel

Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

