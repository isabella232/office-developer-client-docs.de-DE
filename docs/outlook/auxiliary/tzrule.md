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
# <a name="tzrule"></a><span data-ttu-id="b5d05-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="b5d05-103">TZRULE</span></span>

<span data-ttu-id="b5d05-104">Gibt Informationen für eine Regel zur Zeitzone Sommerzeit beim Starten und das Jahr, in dem diese Regel Time-Zone zuerst wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="b5d05-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="b5d05-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="b5d05-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="b5d05-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="b5d05-106">Members</span></span>

<span data-ttu-id="b5d05-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="b5d05-107">_wFlags_</span></span>
  
> <span data-ttu-id="b5d05-108">Die Flags Festlegen dieses Elements identifizieren Sie spezifische Details für diese Regel Time-Zone.</span><span class="sxs-lookup"><span data-stu-id="b5d05-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="b5d05-109">Die möglichen Flags lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="b5d05-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="b5d05-110">**TZRULE_FLAG_EFFECTIVE_TZREG** – identifiziert die Regel als diejenige, die derzeit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5d05-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="b5d05-111">Als die effektive Regel kann nur eine Regel gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="b5d05-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="b5d05-112">Allen anderen Regeln sind nur aus Gründen der Vergleich.</span><span class="sxs-lookup"><span data-stu-id="b5d05-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="b5d05-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** – auf Besprechungsserien, wird die Regel als Entsprechung die Regel in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="b5d05-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="b5d05-114">Dies kann verwendet werden, um festzustellen, ob **PidLidTimeZoneStruct** erheblich durch ein Legacyclient geändert wurde, die andernfalls erkennt die neue, genauere-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="b5d05-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="b5d05-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="b5d05-115">_stStart_</span></span>
  
> <span data-ttu-id="b5d05-116">Die Zeit in koordinierter Weltzeit (UTC), die die Regel Time-Zone gestartet.</span><span class="sxs-lookup"><span data-stu-id="b5d05-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="b5d05-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="b5d05-117">_TZReg_</span></span>
  
> <span data-ttu-id="b5d05-118">Die Informationen zur Zeitzone für die Zeitzone an.</span><span class="sxs-lookup"><span data-stu-id="b5d05-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b5d05-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5d05-119">Remarks</span></span>

<span data-ttu-id="b5d05-120">Diese Struktur erweitert [TZREG](tzreg.md) durch mit zusätzlichen Informationen angezeigt werden, wann Zeitzonenregeln wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="b5d05-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b5d05-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b5d05-121">See also</span></span>

- [<span data-ttu-id="b5d05-122">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="b5d05-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="b5d05-123">Konstanten (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="b5d05-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="b5d05-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="b5d05-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="b5d05-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="b5d05-125">TZDEFINITION</span></span>](tzdefinition.md)

