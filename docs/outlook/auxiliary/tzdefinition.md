---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Stellt eine gesamte Zeitzone dar, einschließlich aller verlaufs-, aktuellen und zukünftigen Zeitzonenverschiebungsregeln für Sommerzeit.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429341"
---
# <a name="tzdefinition"></a>TZDEFINITION

Stellt eine gesamte Zeitzone dar, einschließlich aller verlaufs-, aktuellen und zukünftigen Zeitzonenverschiebungsregeln für Sommerzeit.
  
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
  
> Gibt an, dass der Schlüsselname, der die Zeitzone in der Windows registrierung darstellt, gültig ist. Da jede Zeitzone immer durch einen Schlüsselnamen identifiziert werden sollte, sollte dieses Element immer den Wert **TZDEFINITION_FLAG_VALID_KEYNAME.**
    
_pwszKeyName_
  
> Der Name des Schlüssels für diese Zeitzone in der Windows Registrierung. Dieser Name darf nicht lokalisiert werden. Es hat eine maximale Größe von **MAX_PATH**, die in der Windows Software Development Kit (SDK)-Headerdatei windows.h definiert ist. 
    
_cRules_
  
> Die Anzahl der Zeitzonenregeln für diese Definition. Die maximale Anzahl von Regeln ist **TZ_MAX_RULES**. 
    
_rgRules_
  
> Ein Array von Regeln, die beschreiben, wann Verschiebungen auftreten.
    
## <a name="remarks"></a>Hinweise

Es muss mindestens eine Regel in *rgRules sein.* Die erste Regel in  *rgRules*  wird als die Regel betrachtet, die verwendet werden muss, bis die zweite Regel gestartet wird, unabhängig von  *stStart*  für die erste Regel. 
  
Die Regeln sollten von der ältesten zum neuesten sortiert werden. Es sind keine Überlappungen zwischen Regeln zulässig, daher gilt eine vorherige Regel als beendet, wenn eine neue Regel gestartet wird.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

