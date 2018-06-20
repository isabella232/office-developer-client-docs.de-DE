---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Definiert, wenn Sommerzeit Uhrzeit gestartet wird, tritt die Rückkehr zur Standardzeit und wie viele Stunden der Sommerzeit UMSCHALT ist.
ms.openlocfilehash: 85812ab053d77c07f9360b6bf3a1faaf72cae573
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791217"
---
# <a name="tzreg"></a>TZREG

Definiert, wenn Sommerzeit Uhrzeit gestartet wird, tritt die Rückkehr zur Standardzeit und wie viele Stunden der Sommerzeit UMSCHALT ist.
  
## <a name="quick-info"></a>QuickInfo

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a>Members

_lBias_
  
> Der Abstand von Greenwich Mean Time (GMT).
    
_lStandardBias_
  
> Der Offset vom Verschiebungswert während der Normalzeit.
    
_lDaylightBias_
  
> Der Offset vom Verschiebungswert während der Sommerzeit.
    
_stStandardDate_
  
> Die Zeit zur Standardzeit wechseln.
    
_stDaylightDate_
  
> Die Zeit, um Sommerzeit zu wechseln.
    
## <a name="remarks"></a>Hinweise

Diese Struktur ist ähnlich **TIME_ZONE_INFORMATION**. Dies ist die Struktur, die zum Speichern von Informationen zur Zeitzone für Besprechungsserien von Legacyclients verwendet.
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

