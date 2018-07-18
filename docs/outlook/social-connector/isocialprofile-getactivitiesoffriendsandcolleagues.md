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
ms.openlocfilehash: 54b5cd6d681aa1e8008eade024ef57783bf18ead
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796001"
---
# <a name="isocialprofilegetactivitiesoffriendsandcolleagues"></a><span data-ttu-id="c6059-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="c6059-103">ISocialProfile::GetActivitiesOfFriendsAndColleagues</span></span>

<span data-ttu-id="c6059-104">Diese Methode ist in Outlook Social Connector 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="c6059-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivitiesOfFriendsAndColleagues([in] DATE startTime, [out, retval] BSTR* activitiesCollection);
```

## <a name="remarks"></a><span data-ttu-id="c6059-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6059-105">Remarks</span></span>

<span data-ttu-id="c6059-106">Starten in Outlook Connector für soziale Netzwerke 2013, die OSC unterstützt nur bedarfsgesteuerten Synchronisierung von Aktivitäten und nicht zwischengespeichert oder Hybrid Synchronisierung von Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="c6059-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="c6059-107">Die OSC ignoriert die Einstellung **CacheActivities** in die XML-Funktionen und diese Methode nicht mehr aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="c6059-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and no longer calls this method.</span></span> <span data-ttu-id="c6059-108">Um Nachschlagetabelle dynamischen Aktivitäten zu unterstützen, implementieren Sie die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c6059-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="c6059-109">Legen Sie **GetActivities** und **DynamicActivitiesLookupEx** als **true**die OSC **ISocialSession2::GetActivitiesEx** stattdessen aufzurufen aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="c6059-109">Set **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="c6059-110">Weitere Informationen dazu, wie die OSC Freunde Aktivitäten abruft finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="c6059-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c6059-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c6059-111">See also</span></span>

- [<span data-ttu-id="c6059-112">ISocialProfile : ISocialPerson</span><span class="sxs-lookup"><span data-stu-id="c6059-112">ISocialProfile : ISocialPerson</span></span>](isocialprofileisocialperson.md)

