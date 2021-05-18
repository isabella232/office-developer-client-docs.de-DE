---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Gibt Informationen für eine Zeitzonenregel zum Start der Sommerzeit und zum Jahr an, in dem diese Zeitzonenregel erstmals wirksam wird.
ms.openlocfilehash: 71ede7c0061a058c2dd85c7b9b36c42583a6bb84
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328616"
---
# <a name="tzrule"></a>TZRULE

Gibt Informationen für eine Zeitzonenregel zum Start der Sommerzeit und zum Jahr an, in dem diese Zeitzonenregel erstmals wirksam wird. 
  
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
  
> Die für dieses Mitglied festgelegten Kennzeichen identifizieren bestimmte Details für diese Zeitzonenregel. Die folgenden Flags sind möglich:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** – Identifiziert die Regel als die Regel, die derzeit verwendet werden soll. Es kann nur eine Regel als effektive Regel markiert werden. Alle anderen Regeln dienen nur zu Vergleichszwecken. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** – Identifiziert bei besprechungsserien die Regel als übereinstimmung mit der Regel in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx). Dies kann verwendet werden, um zu ermitteln, ob **PidLidTimeZoneStruct** von einem Legacyclient erheblich geändert wurde, der andernfalls die neue, vollständigere Eigenschaft nicht kennen würde. 
    
_stStart_
  
> Die Uhrzeit in koordinierter Weltzeit (Coordinated Universal Time, UTC), zu der die Zeitzonenregel gestartet wurde.
    
_TZReg_
  
> Die Zeitzoneninformationen für die Zeitzonenregel.
    
## <a name="remarks"></a>Hinweise

Diese Struktur erweitert [TZREG](tzreg.md) durch zusätzliche Informationen, die angeben, wann Zeitzonenregeln wirksam werden. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

