---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- Funktion "quit" [excel 2007]
ms.localizationpriority: medium
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 9524fdf060cb76a63eb867c3bbb809e341eb9f24
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59601352"
---
# <a name="fdance"></a>fDance

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für einen benutzerdefinierten Befehl, der die markierten Zellen im aktiven Arbeitsblatt so lange ändert, bis der Benutzer **ESC** drückt. Beim Laden von GENERIC.xll wird ein benutzerdefiniertes Menü ( Generic) erstellt, über das auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parameter

Die Funktion akzeptiert keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dies ist ein Beispiel für einen längeren Vorgang. Die Funktion [xlAbort](xlabort.md) wird gelegentlich aufgerufen. Dies liefert den Prozessor (hilft bei kooperativem Multitasking) und überprüft, ob der Benutzer **ESC** gedrückt hat, um den Vorgang abzubrechen. Wenn ja, bietet es dem Benutzer die Möglichkeit, den Abbruch abzubrechen. 
  
### <a name="example"></a>Beispiel

Informationen zum Quellcode für diese Funktion finden Sie  `\SAMPLES\GENERIC\GENERIC.C` unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

