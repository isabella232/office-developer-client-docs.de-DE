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
# <a name="tzreg"></a><span data-ttu-id="34373-103">TZREG</span><span class="sxs-lookup"><span data-stu-id="34373-103">TZREG</span></span>

<span data-ttu-id="34373-104">Definiert, wann die Sommerzeit beginnt, wann die Standardzeit zurückgeht und wie viele Stunden die Sommerzeitschicht ist.</span><span class="sxs-lookup"><span data-stu-id="34373-104">Defines when daylight saving time starts, when the return to standard time occurs, and how many hours the daylight saving shift is.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="34373-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="34373-105">Quick info</span></span>

```cpp
typedef struct RenTimeZone { 
    long        lBias;  
    long        lStandardBias; 
    long        lDaylightBias; 
    SYSTEMTIME  stStandardDate; 
    SYSTEMTIME  stDaylightDate; 
} TZREG; 

```

## <a name="members"></a><span data-ttu-id="34373-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="34373-106">Members</span></span>

<span data-ttu-id="34373-107">_lBias_</span><span class="sxs-lookup"><span data-stu-id="34373-107">_lBias_</span></span>
  
> <span data-ttu-id="34373-108">Der Offset von Greenwich Mean Time (GMT).</span><span class="sxs-lookup"><span data-stu-id="34373-108">The offset from Greenwich Mean Time (GMT).</span></span>
    
<span data-ttu-id="34373-109">_lStandardBias_</span><span class="sxs-lookup"><span data-stu-id="34373-109">_lStandardBias_</span></span>
  
> <span data-ttu-id="34373-110">Der Offset von bias während der Standardzeit.</span><span class="sxs-lookup"><span data-stu-id="34373-110">The offset from bias during standard time.</span></span>
    
<span data-ttu-id="34373-111">_lDaylightBias_</span><span class="sxs-lookup"><span data-stu-id="34373-111">_lDaylightBias_</span></span>
  
> <span data-ttu-id="34373-112">Der Offset von bias während der Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="34373-112">The offset from bias during daylight saving time.</span></span>
    
<span data-ttu-id="34373-113">_stStandardDate_</span><span class="sxs-lookup"><span data-stu-id="34373-113">_stStandardDate_</span></span>
  
> <span data-ttu-id="34373-114">Die Zeit zum Wechseln zur Standardzeit.</span><span class="sxs-lookup"><span data-stu-id="34373-114">The time to switch to standard time.</span></span>
    
<span data-ttu-id="34373-115">_stDaylightDate_</span><span class="sxs-lookup"><span data-stu-id="34373-115">_stDaylightDate_</span></span>
  
> <span data-ttu-id="34373-116">Die Zeit zum Wechseln zur Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="34373-116">The time to switch to daylight saving time.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="34373-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="34373-117">Remarks</span></span>

<span data-ttu-id="34373-118">Diese Struktur ähnelt **TIME_ZONE_INFORMATION**.</span><span class="sxs-lookup"><span data-stu-id="34373-118">This structure is similar to **TIME_ZONE_INFORMATION**.</span></span> <span data-ttu-id="34373-119">Dies ist die Struktur, die von Legacyclients zum Speichern von Zeitzoneninformationen für wiederkehrende Besprechungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34373-119">This is the structure used by legacy clients to store time zone information for recurring meetings.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="34373-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="34373-120">See also</span></span>

- [<span data-ttu-id="34373-121">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="34373-121">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="34373-122">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="34373-122">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)  
- [<span data-ttu-id="34373-123">TZRULE</span><span class="sxs-lookup"><span data-stu-id="34373-123">TZRULE</span></span>](tzrule.md)

