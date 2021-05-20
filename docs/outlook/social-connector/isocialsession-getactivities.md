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
ms.openlocfilehash: 29a7cdc9895dcfa2bd926d95dbd2089b7a5dc778
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439296"
---
# <a name="isocialsessiongetactivities"></a><span data-ttu-id="a8199-103">ISocialSession::GetActivities</span><span class="sxs-lookup"><span data-stu-id="a8199-103">ISocialSession::GetActivities</span></span>

<span data-ttu-id="a8199-104">Diese Methode ist in OSC 1.1 veraltet.</span><span class="sxs-lookup"><span data-stu-id="a8199-104">This method has been deprecated in OSC 1.1.</span></span>
  
```cpp
HRESULT GetActivities([in] SAFEARRAY(BSTR) emailAddresses, [in] DATE startTime, [out, retval] BSTR *activities);
```

## <a name="remarks"></a><span data-ttu-id="a8199-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a8199-105">Remarks</span></span>

<span data-ttu-id="a8199-106">Ab OSC 1.1 ruft das OSC **getActivities** nicht mehr auf.</span><span class="sxs-lookup"><span data-stu-id="a8199-106">Starting in OSC 1.1, the OSC no longer calls **GetActivities**.</span></span> <span data-ttu-id="a8199-107">Das OSC ignoriert den Wert **von dynamicActivitiesLookup**.</span><span class="sxs-lookup"><span data-stu-id="a8199-107">The OSC ignores the value of **dynamicActivitiesLookup**.</span></span> <span data-ttu-id="a8199-108">Implementieren Sie die [ISocialSession2::GetActivitiesEx-Methode,](isocialsession2-getactivitiesex.md) um die Suche nach dynamischen Aktivitäten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a8199-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="a8199-109">Legen Sie **cacheActivities** als **false** und **getActivities** und **dynamicActivitiesLookupEx** als **true** fest, wodurch das OSC **stattdessen ISocialSession2::GetActivitiesEx** aufruft.</span><span class="sxs-lookup"><span data-stu-id="a8199-109">Set **cacheActivities** as **false**, and **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8199-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8199-110">See also</span></span>

- [<span data-ttu-id="a8199-111">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a8199-111">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

