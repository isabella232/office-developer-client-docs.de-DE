---
title: TZRULE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 75ed353c-7d3e-e148-4057-715e82a0f32c
description: Gibt Informationen für eine Zeitzonenregel zum Beginn der Sommerzeit und zum Jahr an, in dem diese Zeitzonenregel zuerst wirksam wird.
ms.openlocfilehash: cd77840da1ff391ec3027787e902893fe701382b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59631111"
---
# <a name="tzrule"></a>TZRULE

Gibt Informationen für eine Zeitzonenregel zum Beginn der Sommerzeit und zum Jahr an, in dem diese Zeitzonenregel zuerst wirksam wird. 
  
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
  
> Die für dieses Element festgelegten Flags identifizieren bestimmte Details für diese Zeitzonenregel. Die folgenden Flags sind möglich:
    
   - **TZRULE_FLAG_EFFECTIVE_TZREG** : Identifiziert die Regel als die Regel, die derzeit verwendet werden soll. Nur eine Regel kann als effektive Regel markiert werden. Alle anderen Regeln dienen nur zu Vergleichszwecken. 
    
   - **TZRULE_FLAG_RECUR_CURRENT_TZREG** : Identifiziert bei Besprechungsserien die Regel als mit der Regel in [PidLidTimeZoneStruct übereinstimmend.](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx) Dies kann verwendet werden, um zu ermitteln, ob **PidLidTimeZoneStruct** von einem Legacyclient erheblich geändert wurde, was andernfalls die neue, vollständigere Eigenschaft nicht kennen würde. 
    
_stStart_
  
> Die Zeit in koordinierter Weltzeit (UTC), zu der die Zeitzonenregel gestartet wurde.
    
_TZReg_
  
> Die Zeitzoneninformationen für die Zeitzonenregel.
    
## <a name="remarks"></a>Bemerkungen

Diese Struktur ergänzt [TZREG](tzreg.md) durch zusätzliche Informationen, die angeben, wann Zeitzonenregeln wirksam werden. 
  
## <a name="see-also"></a>Siehe auch

- [Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [Konstanten (Outlook exportierter APIs)](constants-outlook-exported-apis.md)
- [HrCreateApptRebaser](hrcreateapptrebaser.md)
- [TZDEFINITION](tzdefinition.md)

