---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Zuletzt geändert: 03 Juli 2012'
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793281"
---
# <a name="meid"></a><span data-ttu-id="e5cdf-103">MEID</span><span class="sxs-lookup"><span data-stu-id="e5cdf-103">MEID</span></span>

 
  
<span data-ttu-id="e5cdf-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="e5cdf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="e5cdf-105">Bezeichner für ein Outlook-Element.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="e5cdf-106">Sie enthält eine Eintrags-ID und weitere relevante Informationen.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="e5cdf-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="e5cdf-107">Quick info</span></span>

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a><span data-ttu-id="e5cdf-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="e5cdf-108">Members</span></span>

 <span data-ttu-id="e5cdf-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="e5cdf-109">_abFlags_</span></span>
  
> <span data-ttu-id="e5cdf-110">4-Byte-Eintrags-ID für das Outlook-Element.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="e5cdf-111">Weitere Informationen zu MAPI-Eintragsbezeichner finden Sie unter **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="e5cdf-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="e5cdf-112">_muid_</span></span>
  
> <span data-ttu-id="e5cdf-113">GUID, den Speicheranbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="e5cdf-114">Finden Sie unter mapidefs.h für die Definition des **MAPIUID**Typs.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="e5cdf-115">_Platzhalter_</span><span class="sxs-lookup"><span data-stu-id="e5cdf-115">_placeholder_</span></span>
  
> <span data-ttu-id="e5cdf-116">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="e5cdf-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="e5cdf-117">_ltidFld_</span></span>
  
> <span data-ttu-id="e5cdf-118">Langfristige ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="e5cdf-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="e5cdf-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="e5cdf-120">Langfristige ID des Outlook-Elements.</span><span class="sxs-lookup"><span data-stu-id="e5cdf-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e5cdf-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5cdf-121">See also</span></span>



[<span data-ttu-id="e5cdf-122">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="e5cdf-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e5cdf-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="e5cdf-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="e5cdf-124">LTID</span><span class="sxs-lookup"><span data-stu-id="e5cdf-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="e5cdf-125">SYNC</span><span class="sxs-lookup"><span data-stu-id="e5cdf-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="e5cdf-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="e5cdf-126">UPMSG</span></span>](upmsg.md)

