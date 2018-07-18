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
ms.openlocfilehash: af952b6d57325e1b52093fcf655e6fdc271ca34f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795963"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="a7f72-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="a7f72-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="a7f72-104">Diese Methode ist in Outlook Social Connector 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="a7f72-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="a7f72-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7f72-105">Remarks</span></span>

<span data-ttu-id="a7f72-106">Starten in Outlook Connector für soziale Netzwerke 2013, die OSC unterstützt nur bedarfsgesteuerten Synchronisierung von Aktivitäten und nicht zwischengespeichert oder Hybrid Synchronisierung von Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="a7f72-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="a7f72-107">Die OSC ignoriert die Einstellung **CacheActivities** in die XML-Funktionen und ruft diese Methode nicht auf.</span><span class="sxs-lookup"><span data-stu-id="a7f72-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="a7f72-108">Um Nachschlagetabelle dynamischen Aktivitäten zu unterstützen, implementieren Sie die [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="a7f72-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="a7f72-109">Legen Sie **CacheActivities** als **false**, **GetActivities** und **DynamicActivitiesLookupEx** als **true**die OSC **ISocialSession2::GetActivitiesEx** stattdessen aufzurufen aufgefordert wird.</span><span class="sxs-lookup"><span data-stu-id="a7f72-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="a7f72-110">Weitere Informationen dazu, wie die OSC Freunde Aktivitäten abruft finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="a7f72-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a7f72-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a7f72-111">See also</span></span>

- [<span data-ttu-id="a7f72-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a7f72-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

