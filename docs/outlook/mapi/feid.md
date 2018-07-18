---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Zuletzt geändert: 02 Juli 2012'
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19791677"
---
# <a name="feid"></a><span data-ttu-id="39e18-103">FEID</span><span class="sxs-lookup"><span data-stu-id="39e18-103">FEID</span></span>

 
  
<span data-ttu-id="39e18-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="39e18-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="39e18-105">Bezeichner für einen Ordner.</span><span class="sxs-lookup"><span data-stu-id="39e18-105">Identifier for a folder.</span></span> <span data-ttu-id="39e18-106">Sie enthält eine Eintrags-ID und weitere relevante Informationen.</span><span class="sxs-lookup"><span data-stu-id="39e18-106">It contains an entry identifier and other relevant information.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="39e18-107">QuickInfo</span><span class="sxs-lookup"><span data-stu-id="39e18-107">Quick info</span></span>

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a><span data-ttu-id="39e18-108">Elemente</span><span class="sxs-lookup"><span data-stu-id="39e18-108">Members</span></span>

 <span data-ttu-id="39e18-109">_abFlags_</span><span class="sxs-lookup"><span data-stu-id="39e18-109">_abFlags_</span></span>
  
> <span data-ttu-id="39e18-110">4-Byte-Eintrags-ID für den Ordner.</span><span class="sxs-lookup"><span data-stu-id="39e18-110">4-byte entry identifier for the folder.</span></span> <span data-ttu-id="39e18-111">Weitere Informationen zu MAPI-Eintragsbezeichner finden Sie unter **[ENTRYID](entryid.md)**.</span><span class="sxs-lookup"><span data-stu-id="39e18-111">For more information about MAPI entry identifiers, see **[ENTRYID](entryid.md)**.</span></span> 
    
 <span data-ttu-id="39e18-112">_muid_</span><span class="sxs-lookup"><span data-stu-id="39e18-112">_muid_</span></span>
  
> <span data-ttu-id="39e18-113">GUID, den Speicheranbieter identifiziert.</span><span class="sxs-lookup"><span data-stu-id="39e18-113">GUID that identifies the store provider.</span></span> <span data-ttu-id="39e18-114">Finden Sie unter mapidefs.h für die Definition des **MAPIUID**Typs.</span><span class="sxs-lookup"><span data-stu-id="39e18-114">See mapidefs.h for the type definition of **MAPIUID**.</span></span> 
    
 <span data-ttu-id="39e18-115">_Platzhalter_</span><span class="sxs-lookup"><span data-stu-id="39e18-115">_placeholder_</span></span>
  
> <span data-ttu-id="39e18-116">Dieser Member wird für die interne Verwendung von Outlook reserviert und wird nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="39e18-116">This member is reserved for the internal use of Outlook and is not supported.</span></span>
    
 <span data-ttu-id="39e18-117">_ltid_</span><span class="sxs-lookup"><span data-stu-id="39e18-117">_ltid_</span></span>
  
> <span data-ttu-id="39e18-118">Langfristige ID des Ordners.</span><span class="sxs-lookup"><span data-stu-id="39e18-118">Long-term ID of the folder.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="39e18-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39e18-119">See also</span></span>



[<span data-ttu-id="39e18-120">Informationen über den Replikationszustandsautomaten</span><span class="sxs-lookup"><span data-stu-id="39e18-120">About the Replication State Machine</span></span>](about-the-replication-state-machine.md)
  
[<span data-ttu-id="39e18-121">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="39e18-121">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="39e18-122">LTID</span><span class="sxs-lookup"><span data-stu-id="39e18-122">LTID</span></span>](ltid.md)
  
[<span data-ttu-id="39e18-123">UPFLD</span><span class="sxs-lookup"><span data-stu-id="39e18-123">UPFLD</span></span>](upfld.md)
  
[<span data-ttu-id="39e18-124">SYNC</span><span class="sxs-lookup"><span data-stu-id="39e18-124">SYNC</span></span>](sync.md)

