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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437742"
---
# <a name="isocialpersongetactivities"></a><span data-ttu-id="15d3f-103">ISocialPerson::GetActivities</span><span class="sxs-lookup"><span data-stu-id="15d3f-103">ISocialPerson::GetActivities</span></span>

<span data-ttu-id="15d3f-104">Diese Methode ist in Outlook Social Connector 2013 veraltet.</span><span class="sxs-lookup"><span data-stu-id="15d3f-104">This method has been deprecated in Outlook Social Connector 2013.</span></span>
  
```cpp
HRESULT _stdcall GetActivities([in] DATE startTime, [out, retval] BSTR* activities);
```

## <a name="remarks"></a><span data-ttu-id="15d3f-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="15d3f-105">Remarks</span></span>

<span data-ttu-id="15d3f-106">Ab Outlook Social Connector 2013 unterstützt das OSC nur die on-demand-Synchronisierung von Aktivitäten und keine zwischengespeicherte oder hybride Synchronisierung von Aktivitäten.</span><span class="sxs-lookup"><span data-stu-id="15d3f-106">Starting in Outlook Social Connector 2013, the OSC supports only on-demand synchronization of activities and not cached or hybrid synchronization of activities.</span></span> <span data-ttu-id="15d3f-107">Die OSC ignoriert die **Einstellung cacheActivities** im Capabilities XML und aufruft diese Methode nicht.</span><span class="sxs-lookup"><span data-stu-id="15d3f-107">The OSC ignores the **cacheActivities** setting in the capabilities XML and does not call this method.</span></span> <span data-ttu-id="15d3f-108">Implementieren Sie die [ISocialSession2::GetActivitiesEx-Methode,](isocialsession2-getactivitiesex.md) um die Suche nach dynamischen Aktivitäten zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="15d3f-108">To support dynamic activities lookup, implement the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method.</span></span> <span data-ttu-id="15d3f-109">Legen Sie **cacheActivities** als **false**, **getActivities** und **dynamicActivitiesLookupEx** als **true** fest, wodurch das OSC **stattdessen ISocialSession2::GetActivitiesEx** aufruft.</span><span class="sxs-lookup"><span data-stu-id="15d3f-109">Set **cacheActivities** as **false**, **getActivities** and **dynamicActivitiesLookupEx** as **true**, which will prompt the OSC to call **ISocialSession2::GetActivitiesEx** instead.</span></span> 
  
<span data-ttu-id="15d3f-110">Weitere Informationen dazu, wie das OSC die Aktivitäten von Freunden erhält, finden Sie [unter Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="15d3f-110">For more information about how the OSC gets friends' activities, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="15d3f-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="15d3f-111">See also</span></span>

- [<span data-ttu-id="15d3f-112">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="15d3f-112">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)

