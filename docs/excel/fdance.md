---
title: fDance
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- fDance
keywords:
- fdance-Funktion [excel 2007]
localization_priority: Normal
ms.assetid: 8c2f2d83-b7aa-456e-b473-a54897bc35ae
description: 'Gilt für: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a191c07d2a06a1cb6123c235e8fac69d90426758
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409048"
---
# <a name="fdance"></a>fDance

 **Gilt für**: Excel 2013 | Office 2013 | Visual Studio 
  
Beispiel für benutzerdefinierten Befehl, der die ausgewählten Zellen im aktiven Arbeitsblatt ändert, bis der Benutzer **ESC drückt.** Wenn GENERIC.xll geladen wird, wird ein benutzerdefiniertes Menü, Generic, erstellt, über das auf diesen Befehl zugegriffen wird.
  
```cs
int WINAPI fDance(void);
```

## <a name="parameters"></a>Parameter

Die Funktion nimmt keine Parameter an.
  
## <a name="property-valuereturn-value"></a>Eigenschaftswert/Rückgabewert

Die Funktion gibt immer 1 zurück.
  
## <a name="remarks"></a>Hinweise

Dies ist ein Beispiel für einen langwierigen Vorgang. Die Funktion [xlAbort](xlabort.md) wird gelegentlich aufruft. Dies ergibt den Prozessor (hilft beim kooperativen Multitasking) und überprüft, ob der Benutzer **esC** gedrückt hat, um den Vorgang abgesagt zu haben. Wenn ja, bietet es dem Benutzer die Möglichkeit, den Abbruch abbricht. 
  
### <a name="example"></a>Beispiel

Den  `\SAMPLES\GENERIC\GENERIC.C` Quellcode für diese Funktion finden Sie unter. 
  
## <a name="see-also"></a>Siehe auch



[Funktionen in der generische DLL](functions-in-the-generic-dll.md)

