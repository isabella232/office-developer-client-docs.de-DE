---
title: TZREG
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a353e1a3-0187-20af-b9ba-43438f6024d5
description: Definiert, wann die Sommerzeit beginnt, wann die Standardzeit zurückgeht und wie viele Stunden die Sommerzeitschicht ist.
ms.openlocfilehash: 136ff6ad0c1a9bc2ad61ef7ba698d66d645165d8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419366"
---
# <a name="tzreg"></a>TZREG

Definiert, wann die Sommerzeit beginnt, wann die Standardzeit zurückgeht und wie viele Stunden die Sommerzeitschicht ist.
  
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
  
> Der Offset von bias während der Standardzeit.
    
_lDaylightBias_
  
> Der Offset von bias während der Sommerzeit.
    
_stStandardDate_
  
> Die Zeit zum Wechseln zur Standardzeit.
    
_stDaylightDate_
  
> Die Zeit zum Wechseln zur Sommerzeit.
    
## <a name="remarks"></a>Hinweise

Diese Struktur ähnelt **TIME_ZONE_INFORMATION**. Dies ist die Struktur, die von Legacyclients zum Speichern von Zeitzoneninformationen für wiederkehrende Besprechungen verwendet wird.
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [HrCreateApptRebaser](hrcreateapptrebaser.md)  
- [TZRULE](tzrule.md)

