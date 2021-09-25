---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Definiert, wann die Sommerzeit beginnt, wann die Rückkehr zur Standardzeit erfolgt und wie viele Stunden die Sommerzeit ist.
ms.openlocfilehash: ff0cda4da16a141be73955af5dcd758d575fe434
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59605244"
---
# <a name="tzreg"></a>TZREG

Definiert, wann die Sommerzeit beginnt, wann die Rückkehr zur Standardzeit erfolgt und wie viele Stunden die Sommerzeit ist.
  
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
  
> Der Offset von Greenwich Mean Time (GMT).
    
_lStandardBias_
  
> Der Offset von Bias während der Standardzeit.
    
_lDaylightBias_
  
> Der Offset von Bias während der Sommerzeit.
    
_stStandardDate_
  
> Die Zeit für den Wechsel zur Standardzeit.
    
_stDaylightDate_
  
> Die Zeit, um zur Sommerzeit zu wechseln.
    
## <a name="remarks"></a>HinwBemerkungeneise

Diese Struktur ähnelt **TIME_ZONE_INFORMATION**. Dies ist die Struktur, die von älteren Clients zum Speichern von Zeitzoneninformationen für Besprechungsserien verwendet wird.
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

