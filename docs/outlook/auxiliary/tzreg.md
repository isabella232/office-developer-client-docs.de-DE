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
# <a name="tzreg"></a><span data-ttu-id="c5849-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="c5849-103">TZREG</span></span>

<span data-ttu-id="c5849-104">Legt fest, wann die Sommerzeit beginnt, wann die Rückkehr zur Standardzeit erfolgt und wie viele Stunden die Sommer-Speicherschicht ist.</span><span class="sxs-lookup"><span data-stu-id="c5849-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c5849-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c5849-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="c5849-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="c5849-106">Members</span></span>

<span data-ttu-id="c5849-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="c5849-107">_lBias_</span></span>
  
> <span data-ttu-id="c5849-108">Der Offset aus der Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="c5849-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="c5849-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="c5849-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="c5849-110">Der Offset von Bias während der Standardzeit.</span><span class="sxs-lookup"><span data-stu-id="c5849-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="c5849-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="c5849-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="c5849-112">Der Offset von Bias während der Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="c5849-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="c5849-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="c5849-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="c5849-114">Die Zeit, zu der Standardzeit gewechselt werden soll.</span><span class="sxs-lookup"><span data-stu-id="c5849-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="c5849-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="c5849-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="c5849-116">Die Zeit, die zur Sommerzeit wechselt.</span><span class="sxs-lookup"><span data-stu-id="c5849-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c5849-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c5849-117">Remarks</span></span>

<span data-ttu-id="c5849-118">Diese Struktur ähnelt **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="c5849-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="c5849-119">Dies ist die Struktur, die von Legacyclients zum Speichern von Zeitzoneninformationen für wiederkehrende Besprechungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c5849-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="c5849-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c5849-120">See also</span></span>

- [<span data-ttu-id="c5849-121">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="c5849-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="c5849-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="c5849-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="c5849-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="c5849-123">TZRULE</span></span>](tzrule.md)

