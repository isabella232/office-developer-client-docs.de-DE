---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: eb182d9cc51c196558f9e9192a65352e87372bf0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582518"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="64a92-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="64a92-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="64a92-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="64a92-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="64a92-105">Die Struktur wird mit [HrCreateOfflineObj](hrcreateofflineobj.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="64a92-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="64a92-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="64a92-106">Members</span></span>

 <span data-ttu-id="64a92-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="64a92-107">**ulSize**</span></span>
  
> <span data-ttu-id="64a92-108">Die Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="64a92-108">The size of the structure.</span></span>
    
 <span data-ttu-id="64a92-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="64a92-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="64a92-110">Ein Zeiger auf die IUnknown-Objekt, auf dem dieses Objekt gerade zusammengesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="64a92-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="64a92-111">Dadurch werden alle QueryInterface Anrufe über auf das erstellte Objekt zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="64a92-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="64a92-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="64a92-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="64a92-113">NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="64a92-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="64a92-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="64a92-114">See also</span></span>



[<span data-ttu-id="64a92-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="64a92-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="64a92-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="64a92-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

