---
title: ISocialSessionGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6546be99-aee4-41a6-8297-ace378776503
description: Diese Methode ist in OSC 1.1 veraltet.
ms.openlocfilehash: dc5fe25e4c4f83717309d407963d0046aa6063ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795984"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="8b4f0-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="8b4f0-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="8b4f0-104">Diese Methode ist in OSC 1.1 veraltet.</span><span class="sxs-lookup"><span data-stu-id="8b4f0-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="8b4f0-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8b4f0-105">Remarks</span></span>

<span data-ttu-id="8b4f0-106">In Version 1.1 OSC starten, ruft der OSC nicht mehr **GetActivities**.</span><span class="sxs-lookup"><span data-stu-id="8b4f0-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="8b4f0-107">Die OSC wird den Wert der **DynamicActivitiesLookup**ignoriert.</span><span class="sxs-lookup"><span data-stu-id="8b4f0-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="8b4f0-108">Um Nachschlagetabelle dynamischen Aktivitäten zu unterstützen, implementieren Sie die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="8b4f0-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="8b4f0-109">Legen Sie **CacheActivities** als **"false"**, und **GetActivities** und **DynamicActivitiesLookupEx** als **true**die OSC **ISocialSession2::GetActivitiesEx** stattdessen aufzurufen aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="8b4f0-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="8b4f0-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8b4f0-110">See also</span></span>

- [<span data-ttu-id="8b4f0-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8b4f0-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

