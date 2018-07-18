---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Stellt eine gesamte Zeitzone, einschließlich aller historischen, aktuellen und zukünftigen Zeitzone UMSCHALT Regeln Sommerzeit.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791227"
---
# <a name="tzdefinition"></a>TZDEFINITION

Stellt eine gesamte Zeitzone, einschließlich aller historischen, aktuellen und zukünftigen Zeitzone UMSCHALT Regeln Sommerzeit.
  
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
  
> Gibt an, dass der Name des Schlüssels, der die Zeitzone in der Windows-Registrierung gültig ist. Da jede Zeitzone immer mit einem Schlüsselnamen bestimmt werden soll, sollte dieser Member immer den Wert **TZDEFINITION_FLAG_VALID_KEYNAME**haben.
    
_pwszKeyName_
  
> Der Name des Schlüssels für diese Zeitzone in der Windows-Registrierung. Dieser Name muss nicht lokalisiert werden. Es wurde eine maximale Größe von **MAX_PATH**, die in der Windows Software Development Kit (SDK) Kopfzeile Datei windows.h definiert ist. 
    
_cRules_
  
> Die Anzahl der Zeitzonenregeln für diese Definition. Die maximale Anzahl von Regeln ist **TZ_MAX_RULES**. 
    
_rgRules_
  
> Ein Array von Regeln, die beim Auftreten von Schichten beschreiben.
    
## <a name="remarks"></a>Bemerkungen

Es muss mindestens eine Regel in *RgRules* . Die erste Regel in *RgRules* wird unabhängig von der *StStart* auf die erste Regel angesehen werden die Regel verwenden, bis die zweite Regel beginnt. 
  
Die Regeln sollten von ALT zu neu sortiert werden. Überschneidung zwischen Regeln, damit eine vorherige Regel gilt für das Ende beim Starten einer neuen Regel zulässig ist.
  
## <a name="see-also"></a>Siehe auch

- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)

