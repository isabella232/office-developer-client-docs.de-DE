---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Stellt eine gesamte Zeitzone dar, einschließlich aller historischen, aktuellen und zukünftigen Zeitzonen-Schichtregeln für Sommerzeit.
ms.openlocfilehash: 845d2cb2195eb6736fe03f0b66e5110d692538ee
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631132"
---
# <a name="tzdefinition"></a>TZDEFINITION

Stellt eine gesamte Zeitzone dar, einschließlich aller historischen, aktuellen und zukünftigen Zeitzonen-Schichtregeln für Sommerzeit.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a>Elemente

_wFlags_
  
> Gibt an, dass der Schlüsselname, der die Zeitzone in der Windows Registrierung darstellt, gültig ist. Da jede Zeitzone immer durch einen Schlüsselnamen identifiziert werden soll, sollte dieses Element immer den Wert **TZDEFINITION_FLAG_VALID_KEYNAME** haben.
    
_pwszKeyName_
  
> Der Name des Schlüssels für diese Zeitzone in der Windows Registrierung. Dieser Name darf nicht lokalisiert werden. Es verfügt über eine maximale Größe von **MAX_PATH,** die in der Headerdatei "windows.h" des Windows Software Development Kit (SDK) definiert ist. 
    
_cRules_
  
> Die Anzahl der Zeitzonenregeln für diese Definition. Die maximale Anzahl von Regeln ist **TZ_MAX_RULES.** 
    
_rgRules_
  
> Ein Array von Regeln, die beschreiben, wann Schichten auftreten.
    
## <a name="remarks"></a>Bemerkungen

Es muss mindestens eine Regel in  *rgRules*  vorhanden sein. Die erste Regel in  *rgRules*  gilt als die Regel, die verwendet werden soll, bis die zweite Regel gestartet wird, unabhängig vom  *StStart*  der ersten Regel. 
  
Die Regeln sollten vom ältesten zum neuesten sortiert werden. Es ist keine Überlappung zwischen Regeln zulässig, daher gilt eine frühere Regel als beendet, wenn eine neue Regel gestartet wird.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

