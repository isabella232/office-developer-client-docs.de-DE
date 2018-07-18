---
title: TZDEFINITION
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 0ae21571-2299-6407-807c-428668bb6798
description: Stellt eine gesamte Zeitzone, einschließlich aller historischen, aktuellen und zukünftigen Zeitzone UMSCHALT Regeln Sommerzeit.
ms.openlocfilehash: f436216f5da882ea8ac144e6bd384e51e31abb8e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791227"
---
# <a name="tzdefinition"></a><span data-ttu-id="cb0ea-103">TZDEFINITION</span><span class="sxs-lookup"><span data-stu-id="cb0ea-103">TZDEFINITION</span></span>

<span data-ttu-id="cb0ea-104">Stellt eine gesamte Zeitzone, einschließlich aller historischen, aktuellen und zukünftigen Zeitzone UMSCHALT Regeln Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-104">Represents an entire time zone including all historical, current, and future time zone shift rules for daylight saving time.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="cb0ea-105">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="cb0ea-105">Quick info</span></span>

```cpp
typedef struct { 
    WORD     wFlags;  
    LPWSTR   pwszKeyName; 
    WORD     cRules; 
    TZRULE*  rgRules; 
} TZDEFINITION;
```

## <a name="members"></a><span data-ttu-id="cb0ea-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="cb0ea-106">Members</span></span>

<span data-ttu-id="cb0ea-107">_wFlags_</span><span class="sxs-lookup"><span data-stu-id="cb0ea-107">_wFlags_</span></span>
  
> <span data-ttu-id="cb0ea-108">Gibt an, dass der Name des Schlüssels, der die Zeitzone in der Windows-Registrierung gültig ist.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-108">Indicates that the key name that represents the time zone in the Windows registry is valid.</span></span> <span data-ttu-id="cb0ea-109">Da jede Zeitzone immer mit einem Schlüsselnamen bestimmt werden soll, sollte dieser Member immer den Wert **TZDEFINITION_FLAG_VALID_KEYNAME**haben.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-109">Because each time zone should always be identified by a key name, this member should always have the value **TZDEFINITION_FLAG_VALID_KEYNAME**.</span></span>
    
<span data-ttu-id="cb0ea-110">_pwszKeyName_</span><span class="sxs-lookup"><span data-stu-id="cb0ea-110">_pwszKeyName_</span></span>
  
> <span data-ttu-id="cb0ea-111">Der Name des Schlüssels für diese Zeitzone in der Windows-Registrierung.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-111">The name of the key for this time zone in the Windows registry.</span></span> <span data-ttu-id="cb0ea-112">Dieser Name muss nicht lokalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-112">This name must not be localized.</span></span> <span data-ttu-id="cb0ea-113">Es wurde eine maximale Größe von **MAX_PATH**, die in der Windows Software Development Kit (SDK) Kopfzeile Datei windows.h definiert ist.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-113">It has a maximum size of **MAX_PATH**, which is defined in the Windows Software Development Kit (SDK) header file windows.h.</span></span> 
    
<span data-ttu-id="cb0ea-114">_cRules_</span><span class="sxs-lookup"><span data-stu-id="cb0ea-114">_cRules_</span></span>
  
> <span data-ttu-id="cb0ea-115">Die Anzahl der Zeitzonenregeln für diese Definition.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-115">The number of time zone rules for this definition.</span></span> <span data-ttu-id="cb0ea-116">Die maximale Anzahl von Regeln ist **TZ_MAX_RULES**.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-116">The maximum number of rules is **TZ_MAX_RULES**.</span></span> 
    
<span data-ttu-id="cb0ea-117">_rgRules_</span><span class="sxs-lookup"><span data-stu-id="cb0ea-117">_rgRules_</span></span>
  
> <span data-ttu-id="cb0ea-118">Ein Array von Regeln, die beim Auftreten von Schichten beschreiben.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-118">An array of rules that describe when shifts occur.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cb0ea-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cb0ea-119">Remarks</span></span>

<span data-ttu-id="cb0ea-120">Es muss mindestens eine Regel in *RgRules* .</span><span class="sxs-lookup"><span data-stu-id="cb0ea-120">There must be at least one rule in  *rgRules*  .</span></span> <span data-ttu-id="cb0ea-121">Die erste Regel in *RgRules* wird unabhängig von der *StStart* auf die erste Regel angesehen werden die Regel verwenden, bis die zweite Regel beginnt.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-121">The first rule in  *rgRules*  is considered to be the rule to use until the second rule starts, regardless of the  *stStart*  on the first rule.</span></span> 
  
<span data-ttu-id="cb0ea-122">Die Regeln sollten von ALT zu neu sortiert werden.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-122">The rules should be sorted from oldest to newest.</span></span> <span data-ttu-id="cb0ea-123">Überschneidung zwischen Regeln, damit eine vorherige Regel gilt für das Ende beim Starten einer neuen Regel zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="cb0ea-123">There is no overlap allowed between rules, so a prior rule is deemed to end when a new rule starts.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cb0ea-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb0ea-124">See also</span></span>

- [<span data-ttu-id="cb0ea-125">Konstanten (Outlook exportierter APIs)</span><span class="sxs-lookup"><span data-stu-id="cb0ea-125">Constants (Outlook exported APIs)</span></span>](constants-outlook-exported-apis.md)
- [<span data-ttu-id="cb0ea-126">Zum neuen Basisadressen Kalender programmgesteuert Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="cb0ea-126">About rebasing calendars programmatically for Daylight Saving Time</span></span>](about-rebasing-calendars-programmatically-for-daylight-saving-time.md)  
- [<span data-ttu-id="cb0ea-127">HrCreateApptRebaser</span><span class="sxs-lookup"><span data-stu-id="cb0ea-127">HrCreateApptRebaser</span></span>](hrcreateapptrebaser.md)

