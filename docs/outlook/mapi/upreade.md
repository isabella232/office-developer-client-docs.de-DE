---
title: UPREADE
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d146ee74-0c3a-5fdd-b1aa-af6498550801
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: fd593b68ef7ca25b1f8ceec613786cdbdd03fd76
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22579074"
---
# <a name="upreade"></a><span data-ttu-id="a6baf-103">UPREADE</span><span class="sxs-lookup"><span data-stu-id="a6baf-103">UPREADE</span></span>

<span data-ttu-id="a6baf-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6baf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6baf-105">Erweiterte Informationen zum Hochladen eines Elements Zustand "gelesen" während der [Upload lesen Status Zustand](upload-read-status-state.md).</span><span class="sxs-lookup"><span data-stu-id="a6baf-105">Extended information for uploading the read state of an item during the [upload read status state](upload-read-status-state.md).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="a6baf-106">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="a6baf-106">Quick info</span></span>

```cpp
struct UPREADE 
{ 
    ULONG ulFlags; 
    SKEY skey; 
};
```

## <a name="members"></a><span data-ttu-id="a6baf-107">Elemente</span><span class="sxs-lookup"><span data-stu-id="a6baf-107">Members</span></span>

<span data-ttu-id="a6baf-108">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a6baf-108">_ulFlags_</span></span>
  
>  <span data-ttu-id="a6baf-109">[Out] / [in] Flags, um das entsprechende Verhalten beim Hochladen zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="a6baf-109">[out]/[in] Flags to determine the appropriate behavior during the upload.</span></span> 
    
  - <span data-ttu-id="a6baf-110">UPR_ASSOC</span><span class="sxs-lookup"><span data-stu-id="a6baf-110">UPR_ASSOC</span></span>
    
    - <span data-ttu-id="a6baf-111">[out] Element ausgeblendet ist.</span><span class="sxs-lookup"><span data-stu-id="a6baf-111">[out] Item is hidden.</span></span>
    
  - <span data-ttu-id="a6baf-112">UPR_READ</span><span class="sxs-lookup"><span data-stu-id="a6baf-112">UPR_READ</span></span>
    
    - <span data-ttu-id="a6baf-113">[out] Der schreibgeschützte Status des Elements wurde geändert.</span><span class="sxs-lookup"><span data-stu-id="a6baf-113">[out] The read status of the item has been changed.</span></span>
    
  - <span data-ttu-id="a6baf-114">UPR_OK</span><span class="sxs-lookup"><span data-stu-id="a6baf-114">UPR_OK</span></span>
    
    - <span data-ttu-id="a6baf-115">[in] Der Upload war erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="a6baf-115">[in] Upload was successful.</span></span> <span data-ttu-id="a6baf-116">Der Client legt dies nach dem Hochladen von Informationen an den Server.</span><span class="sxs-lookup"><span data-stu-id="a6baf-116">The client sets this after uploading information to the server.</span></span>
    
  - <span data-ttu-id="a6baf-117">UPR_COMMIT</span><span class="sxs-lookup"><span data-stu-id="a6baf-117">UPR_COMMIT</span></span>
    
    - <span data-ttu-id="a6baf-118">[in] Hochladen des lesen Status des Elements jetzt, anstatt zu warten, bis zum Ende der [Tabelle Zustand hochladen](upload-table-state.md) zur Stapelverarbeitung mehr als ein Element.</span><span class="sxs-lookup"><span data-stu-id="a6baf-118">[in] Upload the read status of the item now, instead of waiting to the end of the [upload table state](upload-table-state.md) to batch-process more than one item.</span></span> 
    
<span data-ttu-id="a6baf-119">_SKEY_</span><span class="sxs-lookup"><span data-stu-id="a6baf-119">_skey_</span></span>
  
> <span data-ttu-id="a6baf-120">[out] Quellschlüssel des Elements.</span><span class="sxs-lookup"><span data-stu-id="a6baf-120">[out] Source key of the item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a6baf-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a6baf-121">See also</span></span>

- [<span data-ttu-id="a6baf-122">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="a6baf-122">About the Replication API</span></span>](about-the-replication-api.md)
- [<span data-ttu-id="a6baf-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="a6baf-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
- [<span data-ttu-id="a6baf-124">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a6baf-124">MAPI Constants</span></span>](mapi-constants.md)
- [<span data-ttu-id="a6baf-125">UPREAD</span><span class="sxs-lookup"><span data-stu-id="a6baf-125">UPREAD</span></span>](upread.md)

