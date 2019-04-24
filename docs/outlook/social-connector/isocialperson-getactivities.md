---
title: ISocialPersonGetActivities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: cf727140-f6e7-4718-bd74-1f8feeccf70c
description: Diese Methode ist in Outlook Social Connector 2013 veraltet.
ms.openlocfilehash: abad4fc2a3e3aaea8a7097ac7e6f56b0aadae299
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286164"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="c0180-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="c0180-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="c0180-104">Diese Methode ist in Outlook Social Connector 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="c0180-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="c0180-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c0180-105">Remarks</span></span>

<span data-ttu-id="c0180-106">Beginnend mit Outlook Social Connector 2013 unterstützt OSC nur die bedarfsgesteuerte Synchronisierung von Aktivitäten und keine zwischengespeicherte oder hybride Synchronisierung von Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="c0180-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="c0180-107">OSC ignoriert die **cacheActivities** -Einstellung im Capabilities-XML und ruft diese Methode nicht auf.</span><span class="sxs-lookup"><span data-stu-id="c0180-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="c0180-108">Zur Unterstützung der Suche nach dynamischen Aktivitäten implementieren Sie die [ISocialSession2:: GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="c0180-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="c0180-109">Legen Sie **cacheActivities** als **false**, GetActivities und **dynamicActivitiesLookupEx** als **true**fest, wodurch der osc aufgefordert wird, **ISocialSession2:: GetActivitiesEx** stattdessen aufzurufen. \*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="c0180-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="c0180-110">Weitere Informationen dazu, wie die OSC-Aktivitäten von Freunden abgerufen werden, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="c0180-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c0180-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c0180-111">See also</span></span>

- [<span data-ttu-id="c0180-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c0180-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

