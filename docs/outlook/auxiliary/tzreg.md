---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Legt fest, wann die Sommerzeit beginnt, wann die Rückkehr zur Standardzeit erfolgt und wie viele Stunden die Sommer-Speicherschicht ist.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32307840"
---
# <a name="tzreg"></a>TZREG

Legt fest, wann die Sommerzeit beginnt, wann die Rückkehr zur Standardzeit erfolgt und wie viele Stunden die Sommer-Speicherschicht ist.
  
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

## <a name="members"></a>Elemente

_lBias_
  
> Der Offset aus der Greenwich Mean Time (GMT).
    
_lStandardBias_
  
> Der Offset von Bias während der Standardzeit.
    
_lDaylightBias_
  
> Der Offset von Bias während der Sommerzeit.
    
_stStandardDate_
  
> Die Zeit, zu der Standardzeit gewechselt werden soll.
    
_stDaylightDate_
  
> Die Zeit, die zur Sommerzeit wechselt.
    
## <a name="remarks"></a>Bemerkungen

Diese Struktur ähnelt **TIME_ZONE_INFORMATION**. Dies ist die Struktur, die von Legacyclients zum Speichern von Zeitzoneninformationen für wiederkehrende Besprechungen verwendet wird.
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

