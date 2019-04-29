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
ms.openlocfilehash: 4775de0707eb90549f07525e3aa54ec5842f6050
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438162"
---
# <a name="mapiofflineaggregateinfo"></a><span data-ttu-id="03ca9-103">MAPIOFFLINE_AGGREGATEINFO</span><span class="sxs-lookup"><span data-stu-id="03ca9-103">MAPIOFFLINE_AGGREGATEINFO</span></span>

  
  
<span data-ttu-id="03ca9-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03ca9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03ca9-105">Die Struktur wird mit [HrCreateOfflineObj](hrcreateofflineobj.md)verwendet.</span><span class="sxs-lookup"><span data-stu-id="03ca9-105">The structure is used with [HrCreateOfflineObj](hrcreateofflineobj.md).</span></span> 
  
```cpp
typedef struct
{
  ULONG            ulSize;
  IUnknown*          pOuterObj;
  IUnknown*          pRefTrackRoot;
} MAPIOFFLINE_AGGREGATEINFO;
```

## <a name="members"></a><span data-ttu-id="03ca9-106">Members</span><span class="sxs-lookup"><span data-stu-id="03ca9-106">Members</span></span>

 <span data-ttu-id="03ca9-107">**ulSize**</span><span class="sxs-lookup"><span data-stu-id="03ca9-107">**ulSize**</span></span>
  
> <span data-ttu-id="03ca9-108">Die Größe der Struktur.</span><span class="sxs-lookup"><span data-stu-id="03ca9-108">The size of the structure.</span></span>
    
 <span data-ttu-id="03ca9-109">**pOuterObj**</span><span class="sxs-lookup"><span data-stu-id="03ca9-109">**pOuterObj**</span></span>
  
> <span data-ttu-id="03ca9-110">Ein Zeiger auf das IUnknown-Objekt, auf das dieses Objekt aggregiert wird.</span><span class="sxs-lookup"><span data-stu-id="03ca9-110">A pointer to the IUnknown object onto which this object is being aggregated.</span></span> <span data-ttu-id="03ca9-111">Dadurch können QueryInterface-Aufrufe an das erstellte Objekt weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="03ca9-111">This allows any QueryInterface calls to pass through to the created object.</span></span>
    
 <span data-ttu-id="03ca9-112">**pRefTrackRoot**</span><span class="sxs-lookup"><span data-stu-id="03ca9-112">**pRefTrackRoot**</span></span>
  
> <span data-ttu-id="03ca9-113">Muss NULL sein.</span><span class="sxs-lookup"><span data-stu-id="03ca9-113">Must be NULL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="03ca9-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="03ca9-114">See also</span></span>



[<span data-ttu-id="03ca9-115">HrCreateOfflineObj</span><span class="sxs-lookup"><span data-stu-id="03ca9-115">HrCreateOfflineObj</span></span>](hrcreateofflineobj.md)
  
[<span data-ttu-id="03ca9-116">MAPIOFFLINE_CREATEINFO</span><span class="sxs-lookup"><span data-stu-id="03ca9-116">MAPIOFFLINE_CREATEINFO</span></span>](mapioffline_createinfo.md)

