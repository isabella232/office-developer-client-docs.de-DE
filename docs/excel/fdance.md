---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fdance-Funktion [Excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311039"
---
# <a name="fdance"></a>fDance

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für einen benutzerdefinierten Befehl, mit dem die markierten Zellen des aktiven Arbeitsblatts geändert werden, bis der Benutzer **ESC**drückt. Wenn GENERIC. XLL geladen wird, wird ein benutzerdefiniertes Menü generisch erstellt, über das auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parameter

Die Funktion verwendet keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
## <a name="remarks"></a>Bemerkungen

Dies ist ein Beispiel für einen langwierigen Vorgang. Die Funktion [XlAbort](xlabort.md) wird gelegentlich aufgerufen. Dadurch wird der Prozessor (bei kooperativem Multitasking) und überprüft, ob der Benutzer **ESC** gedrückt hat, um den Vorgang abzubrechen. Wenn dies der Fall ist, bietet er dem Benutzer die Möglichkeit, den Abbruch abzubrechen. 
  
### <a name="example"></a>Beispiel

Den `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

