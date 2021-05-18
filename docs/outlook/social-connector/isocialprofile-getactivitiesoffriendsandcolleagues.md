---
title: ISocialProfileGetActivitiesOfFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4aaf7417-0a03-42a4-a282-599327ec5381
description: Diese Methode ist in Outlook Social Connector 2013 veraltet.
ms.openlocfilehash: c02cf0e8a6d2da3f9fb7704c92e10e0409042393
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406892"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="64fde-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="64fde-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="64fde-104">Diese Methode ist in Outlook Social Connector 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="64fde-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="64fde-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="64fde-105">Remarks</span></span>

<span data-ttu-id="64fde-106">Ab Outlook Social Connector 2013 unterstützt das OSC nur die on-demand-Synchronisierung von Aktivitäten und keine zwischengespeicherte oder hybride Synchronisierung von Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="64fde-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="64fde-107">Die OSC ignoriert die **Einstellung cacheActivities** im Capabilities XML und ruft diese Methode nicht mehr auf.</span><span class="sxs-lookup"><span data-stu-id="64fde-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="64fde-108">Implementieren Sie die [ISocialSession2::GetActivitiesEx-Methode,](isocialsession2-getactivitiesex.md) um die Suche nach dynamischen Aktivitäten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="64fde-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="64fde-109">Legen **Sie getActivities** und **dynamicActivitiesLookupEx** als **true** fest, wodurch das OSC **stattdessen ISocialSession2::GetActivitiesEx aufruft.**</span><span class="sxs-lookup"><span data-stu-id="64fde-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="64fde-110">Weitere Informationen dazu, wie das OSC die Aktivitäten von Freunden erhält, finden Sie [unter Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="64fde-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="64fde-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64fde-111">See also</span></span>

- [<span data-ttu-id="64fde-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="64fde-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

