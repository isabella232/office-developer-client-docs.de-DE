---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- Fdance-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Gilt f�r: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: b7a2fbdf723d06dcf9b02789178d7d12d0515884
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19790506"
---
# <a name="fdance"></a>fDance

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Benutzerdefinierte Beispielbefehl, der die markierten Zellen im aktiven Arbeitsblatt um zurückführt, bis der Benutzer die **ESC-Taste**drückt. Wenn GENERIC.xll geladen wird, erstellt es ein Menü benutzerdefinierte allgemeine, über die auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parameter

Die Funktion akzeptiert keine Parameter.
  
## <a name="property-valuereturn-value"></a>Eigenschaft Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
## <a name="remarks"></a>Hinweise

Dies ist ein Beispiel einer langen Operation. Sie ruft die Funktion [Bereichsgröße](xlabort.md) gelegentlich. Dies ergibt den Prozessor (hilft Ihnen bei der gemeinsame Multitasking), und überprüft, ob der Benutzer die **ESC-Taste** , um den Vorgang abzubrechen gedrückt hat. Wenn dies der Fall ist, bietet es dem Benutzer eine Möglichkeit, diesen Vorgang abbrechen. 
  
### <a name="example"></a>Beispiel

Finden Sie unter `\SAMPLES\GENERIC\GENERIC.C` für den Quellcode für diese Funktion. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

