---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Zuletzt geändert: 03 Juli, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430308"
---
# <a name="meid"></a><span data-ttu-id="c8637-103">MEID</span><span class="sxs-lookup"><span data-stu-id="c8637-103">MEID</span></span>

 
  
<span data-ttu-id="c8637-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c8637-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c8637-105">Bezeichner für ein Outlook-Element.</span><span class="sxs-lookup"><span data-stu-id="c8637-105">Identifier for an Outlook item.</span></span> <span data-ttu-id="c8637-106">Sie enthält eine Eintrags-ID und andere relevante Informationen.</span><span class="sxs-lookup"><span data-stu-id="c8637-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="c8637-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="c8637-107">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="c8637-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="c8637-108">Members</span></span>

 <span data-ttu-id="c8637-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="c8637-109">_abFlags_</span></span>
  
> <span data-ttu-id="c8637-110">4-Byte-Eintrags-ID für das Outlook-Element.</span><span class="sxs-lookup"><span data-stu-id="c8637-110">4-byte entry identifier for the Outlook item.</span></span> <span data-ttu-id="c8637-111">Weitere Informationen zu MAPI-Eintrags Bezeichnern **[](entryid.md)** finden Sie Untereintrags-ID.</span><span class="sxs-lookup"><span data-stu-id="c8637-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="c8637-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="c8637-112">_muid_</span></span>
  
> <span data-ttu-id="c8637-113">GUID, die den Informationsspeicher Anbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="c8637-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="c8637-114">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **MAPIUID**.</span><span class="sxs-lookup"><span data-stu-id="c8637-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="c8637-115">_Platzhalter_</span><span class="sxs-lookup"><span data-stu-id="c8637-115">_placeholder_</span></span>
  
> <span data-ttu-id="c8637-116">Dieses Element ist für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c8637-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="c8637-117">_ltidFld_</span><span class="sxs-lookup"><span data-stu-id="c8637-117">_ltidFld_</span></span>
  
> <span data-ttu-id="c8637-118">Langfristige ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="c8637-118">Long-term ID of the folder.</span></span>
    
 <span data-ttu-id="c8637-119">_ltidMsg_</span><span class="sxs-lookup"><span data-stu-id="c8637-119">_ltidMsg_</span></span>
  
> <span data-ttu-id="c8637-120">Langfristige ID des Outlook-Elements.</span><span class="sxs-lookup"><span data-stu-id="c8637-120">Long-term ID of the Outlook item.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c8637-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8637-121">See also</span></span>



[<span data-ttu-id="c8637-122">Informationen über die Replikations-API</span><span class="sxs-lookup"><span data-stu-id="c8637-122">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="c8637-123">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="c8637-123">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="c8637-124">LTID</span><span class="sxs-lookup"><span data-stu-id="c8637-124">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="c8637-125">SYNCHRONISIERUNGS</span><span class="sxs-lookup"><span data-stu-id="c8637-125">SYNC</span></span>](sync.md)
  
[<span data-ttu-id="c8637-126">UPMSG</span><span class="sxs-lookup"><span data-stu-id="c8637-126">UPMSG</span></span>](upmsg.md)

