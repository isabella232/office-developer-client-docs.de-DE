---
title: MAPIOFFLINE_AGGREGATEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2e502d28-ae09-49d9-a35a-5d77acdcd6f4
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 24e16aeb1bbee1c35cf8fbd5813fb3e83b762187
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793127"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="6ee71-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="6ee71-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="6ee71-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6ee71-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6ee71-105">Die Struktur wird mit [HrCreateOfflineObj](hrcreateofflineobj.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ee71-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="6ee71-106">Elemente</span><span class="sxs-lookup"><span data-stu-id="6ee71-106">Members</span></span>

 <span data-ttu-id="6ee71-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="6ee71-107">**ulSize**</span></span>
  
> <span data-ttu-id="6ee71-108">Die Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="6ee71-108">The size of the structure.</span></span>
    
 <span data-ttu-id="6ee71-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="6ee71-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="6ee71-110">Ein Zeiger auf die IUnknown-Objekt, auf dem dieses Objekt gerade zusammengesetzt wird.</span><span class="sxs-lookup"><span data-stu-id="6ee71-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="6ee71-111">Dadurch werden alle QueryInterface Anrufe über auf das erstellte Objekt zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="6ee71-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="6ee71-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="6ee71-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="6ee71-113">NULL muss sein.</span><span class="sxs-lookup"><span data-stu-id="6ee71-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6ee71-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6ee71-114">See also</span></span>



[<span data-ttu-id="6ee71-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="6ee71-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="6ee71-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="6ee71-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

