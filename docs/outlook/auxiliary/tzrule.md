---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Gibt Informationen für eine Regel zur Zeitzone Sommerzeit beim Starten und das Jahr, in dem diese Regel Time-Zone zuerst wirksam wird.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25392697"
---
# <a name="tzrule"></a>TZRULE

Gibt Informationen für eine Regel zur Zeitzone Sommerzeit beim Starten und das Jahr, in dem diese Regel Time-Zone zuerst wirksam wird. 
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a>Elemente

_wFlags_
  
> Die Flags Festlegen dieses Elements identifizieren Sie spezifische Details für diese Regel Time-Zone. Die möglichen Flags lauten wie folgt:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** – identifiziert die Regel als diejenige, die derzeit verwendet werden soll. Als die effektive Regel kann nur eine Regel gekennzeichnet werden. Allen anderen Regeln sind nur aus Gründen der Vergleich. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** – auf Besprechungsserien, wird die Regel als Entsprechung die Regel in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Dies kann verwendet werden, um festzustellen, ob **PidLidTimeZoneStruct** erheblich durch ein Legacyclient geändert wurde, die andernfalls erkennt die neue, genauere-Eigenschaft. 
    
_stStart_
  
> Die Zeit in koordinierter Weltzeit (UTC), die die Regel Time-Zone gestartet.
    
_TZReg_
  
> Die Informationen zur Zeitzone für die Zeitzone an.
    
## <a name="remarks"></a>Hinweise

Diese Struktur erweitert [TZREG](tzreg.md) durch mit zusätzlichen Informationen angezeigt werden, wann Zeitzonenregeln wirksam werden. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

