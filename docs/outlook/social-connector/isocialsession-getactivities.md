---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Diese Methode ist in OSC 1,1 veraltet.
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439296"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="99305-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="99305-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="99305-104">Diese Methode ist in OSC 1,1 veraltet.</span><span class="sxs-lookup"><span data-stu-id="99305-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="99305-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="99305-105">Remarks</span></span>

<span data-ttu-id="99305-106">Ab OSC 1,1 ruft der OSC getActivities nicht mehr \*\*\*\* auf.</span><span class="sxs-lookup"><span data-stu-id="99305-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="99305-107">OSC ignoriert den Wert von **dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="99305-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="99305-108">Zur Unterstützung der Suche nach dynamischen Aktivitäten implementieren Sie die [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="99305-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="99305-109">Legen **Sie cacheActivities** als **false**, \*\*\*\* und GetActivities und **DYNAMICACTIVITIESLOOKUPEX** als **true**fest, wodurch der osc aufgefordert wird, **ISocialSession2:: GetActivitiesEx** stattdessen aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="99305-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="99305-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="99305-110">See also</span></span>

- [<span data-ttu-id="99305-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="99305-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

