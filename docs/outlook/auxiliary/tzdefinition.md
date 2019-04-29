---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Stellt eine gesamte Zeitzone einschließlich aller historischen, aktuellen und zukünftigen Zeitzone-Schicht Regeln für Sommerzeit dar.
ms.openlocfilehash: 5f7000ecc1fa602b330670c2ee1c39f673a11a65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429341"
---
# <a name="tzdefinition"></a><span data-ttu-id="6c4fa-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="6c4fa-103">TZDEFINITION</span></span>

<span data-ttu-id="6c4fa-104">Stellt eine gesamte Zeitzone einschließlich aller historischen, aktuellen und zukünftigen Zeitzone-Schicht Regeln für Sommerzeit dar.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="6c4fa-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="6c4fa-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="6c4fa-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="6c4fa-106">Members</span></span>

<span data-ttu-id="6c4fa-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="6c4fa-107">_wFlags_</span></span>
  
> <span data-ttu-id="6c4fa-108">Gibt an, dass der Schlüsselname, der die Zeitzone in der Windows-Registrierung darstellt, gültig ist.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="6c4fa-109">Da jede Zeitzone immer mit einem Schlüsselnamen identifiziert werden sollte, sollte dieser Member immer den Wert **TZDEFINITION_FLAG_VALID_KEYNAME**haben.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="6c4fa-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="6c4fa-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="6c4fa-111">Der Name des Schlüssels für diese Zeitzone in der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="6c4fa-112">Dieser Name darf nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-112">This name must not be localized.</span></span> <span data-ttu-id="6c4fa-113">Es hat eine maximale Größe von **MAX_PATH**, die in der Windows Software Development Kit (SDK)-Headerdatei Windows. h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="6c4fa-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="6c4fa-114">_cRules_</span></span>
  
> <span data-ttu-id="6c4fa-115">Die Anzahl der Zeitzonenregeln für diese Definition.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="6c4fa-116">Die maximale Anzahl von Regeln lautet **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="6c4fa-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="6c4fa-117">_rgRules_</span></span>
  
> <span data-ttu-id="6c4fa-118">Ein Array von Regeln, die beschreiben, wenn Verschiebungen auftreten.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6c4fa-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c4fa-119">Remarks</span></span>

<span data-ttu-id="6c4fa-120">Es muss mindestens eine Regel in *RgRules* vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="6c4fa-121">Die erste Regel in *rgRules* gilt als die Regel, die verwendet werden soll, bis die zweite Regel gestartet wird, unabhängig von der *stStart* für die erste Regel.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="6c4fa-122">Die Regeln sollten vom ältesten zum neuesten sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="6c4fa-123">Zwischen den Regeln ist keine Überlappung zulässig, sodass eine frühere Regel als beendet gilt, wenn eine neue Regel beginnt.</span><span class="sxs-lookup"><span data-stu-id="6c4fa-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6c4fa-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6c4fa-124">See also</span></span>

- [<span data-ttu-id="6c4fa-125">Konstanten (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="6c4fa-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="6c4fa-126">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="6c4fa-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="6c4fa-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="6c4fa-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

