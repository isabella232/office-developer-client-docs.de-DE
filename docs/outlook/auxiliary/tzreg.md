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
# <a name="tzreg"></a><span data-ttu-id="dc255-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="dc255-103">TZREG</span></span>

<span data-ttu-id="dc255-104">Definiert, wenn Sommerzeit Uhrzeit gestartet wird, tritt die Rückkehr zur Standardzeit und wie viele Stunden der Sommerzeit UMSCHALT ist.</span><span class="sxs-lookup"><span data-stu-id="dc255-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="dc255-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="dc255-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="dc255-106">Members</span><span class="sxs-lookup"><span data-stu-id="dc255-106">Members</span></span>

<span data-ttu-id="dc255-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="dc255-107">_lBias_</span></span>
  
> <span data-ttu-id="dc255-108">Der Abstand von Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="dc255-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="dc255-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="dc255-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="dc255-110">Der Offset vom Verschiebungswert während der Normalzeit.</span><span class="sxs-lookup"><span data-stu-id="dc255-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="dc255-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="dc255-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="dc255-112">Der Offset vom Verschiebungswert während der Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="dc255-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="dc255-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="dc255-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="dc255-114">Die Zeit zur Standardzeit wechseln.</span><span class="sxs-lookup"><span data-stu-id="dc255-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="dc255-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="dc255-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="dc255-116">Die Zeit, um Sommerzeit zu wechseln.</span><span class="sxs-lookup"><span data-stu-id="dc255-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="dc255-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dc255-117">Remarks</span></span>

<span data-ttu-id="dc255-118">Diese Struktur ist ähnlich **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="dc255-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="dc255-119">Dies ist die Struktur, die zum Speichern von Informationen zur Zeitzone für Besprechungsserien von Legacyclients verwendet.</span><span class="sxs-lookup"><span data-stu-id="dc255-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="dc255-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dc255-120">See also</span></span>

- [<span data-ttu-id="dc255-121">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="dc255-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="dc255-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="dc255-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="dc255-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="dc255-123">TZRULE</span></span>](tzrule.md)

