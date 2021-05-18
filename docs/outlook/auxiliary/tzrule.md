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
# <a name="tzrule"></a><span data-ttu-id="e9db0-103">TZRULE</span><span class="sxs-lookup"><span data-stu-id="e9db0-103">TZRULE</span></span>

<span data-ttu-id="e9db0-104">Gibt Informationen für eine Zeitzonenregel zum Start der Sommerzeit und zum Jahr an, in dem diese Zeitzonenregel erstmals wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="e9db0-104">Specifies information for a time zone rule about when daylight saving time starts, and the year in which that time zone rule first takes effect.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="e9db0-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e9db0-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD        wFlags;  
    SYSTEMTIME  stStart; 
    TZREG       TZReg; 
} TZRULE;
```

## <a name="members"></a><span data-ttu-id="e9db0-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="e9db0-106">Members</span></span>

<span data-ttu-id="e9db0-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="e9db0-107">_wFlags_</span></span>
  
> <span data-ttu-id="e9db0-108">Die für dieses Mitglied festgelegten Kennzeichen identifizieren bestimmte Details für diese Zeitzonenregel.</span><span class="sxs-lookup"><span data-stu-id="e9db0-108">The flags set for this member identify specific details for this time zone rule.</span></span> <span data-ttu-id="e9db0-109">Die folgenden Flags sind möglich:</span><span class="sxs-lookup"><span data-stu-id="e9db0-109">The possible flags are as follows:</span></span>
    
   - <span data-ttu-id="e9db0-110">**TZRULE_FLAG_EFFECTIVE_TZREG** – Identifiziert die Regel als die Regel, die derzeit verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e9db0-110">**TZRULE_FLAG_EFFECTIVE_TZREG** —Identifies the rule as the one that should be used currently.</span></span> <span data-ttu-id="e9db0-111">Es kann nur eine Regel als effektive Regel markiert werden.</span><span class="sxs-lookup"><span data-stu-id="e9db0-111">Only one rule can be marked as the effective rule.</span></span> <span data-ttu-id="e9db0-112">Alle anderen Regeln dienen nur zu Vergleichszwecken.</span><span class="sxs-lookup"><span data-stu-id="e9db0-112">All other rules are for comparison purposes only.</span></span> 
    
   - <span data-ttu-id="e9db0-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** – Identifiziert bei besprechungsserien die Regel als übereinstimmung mit der Regel in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="e9db0-113">**TZRULE_FLAG_RECUR_CURRENT_TZREG** —On recurring meetings, identifies the rule as matching the rule in [PidLidTimeZoneStruct](https://msdn.microsoft.com/library/2acf0036-2f3e-4f90-8614-7aa667860f74%28Office.15%29.aspx).</span></span> <span data-ttu-id="e9db0-114">Dies kann verwendet werden, um zu ermitteln, ob **PidLidTimeZoneStruct** von einem Legacyclient erheblich geändert wurde, der andernfalls die neue, vollständigere Eigenschaft nicht kennen würde.</span><span class="sxs-lookup"><span data-stu-id="e9db0-114">This can be used to detect whether **PidLidTimeZoneStruct** has been modified significantly by a legacy client, which would be otherwise unaware of the new, more complete property.</span></span> 
    
<span data-ttu-id="e9db0-115">_stStart_</span><span class="sxs-lookup"><span data-stu-id="e9db0-115">_stStart_</span></span>
  
> <span data-ttu-id="e9db0-116">Die Uhrzeit in koordinierter Weltzeit (Coordinated Universal Time, UTC), zu der die Zeitzonenregel gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="e9db0-116">The time in Coordinated Universal Time (UTC) that the time zone rule started.</span></span>
    
<span data-ttu-id="e9db0-117">_TZReg_</span><span class="sxs-lookup"><span data-stu-id="e9db0-117">_TZReg_</span></span>
  
> <span data-ttu-id="e9db0-118">Die Zeitzoneninformationen für die Zeitzonenregel.</span><span class="sxs-lookup"><span data-stu-id="e9db0-118">The time zone information for the time zone rule.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e9db0-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e9db0-119">Remarks</span></span>

<span data-ttu-id="e9db0-120">Diese Struktur erweitert [TZREG](tzreg.md) durch zusätzliche Informationen, die angeben, wann Zeitzonenregeln wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="e9db0-120">This structure augments [TZREG](tzreg.md) by providing additional information indicating when time zone rules take effect.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9db0-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9db0-121">See also</span></span>

- [<span data-ttu-id="e9db0-122">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="e9db0-122">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) 
- [<span data-ttu-id="e9db0-123">Konstanten (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="e9db0-123">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="e9db0-124">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="e9db0-124">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)
- [<span data-ttu-id="e9db0-125">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="e9db0-125">TZDEFINITION</span></span>](tzdefinition.md)

