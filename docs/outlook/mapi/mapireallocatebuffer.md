---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 26dcc31f2ebdd1892f966bfb95fda1a65c5140cb
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793145"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="41092-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="41092-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="41092-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="41092-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="41092-105">Ordnet Speicherpuffers neu.</span><span class="sxs-lookup"><span data-stu-id="41092-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="41092-106">Es wird mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="41092-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="41092-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="41092-107">Header file:</span></span>  <br/> |<span data-ttu-id="41092-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="41092-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="41092-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="41092-109">Called by:</span></span>  <br/> |<span data-ttu-id="41092-110">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="41092-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="41092-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="41092-111">Parameters</span></span>

 <span data-ttu-id="41092-112">_LPV_</span><span class="sxs-lookup"><span data-stu-id="41092-112">_lpv_</span></span>
  
> <span data-ttu-id="41092-113">Ein Zeiger auf den Speicher neu reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="41092-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="41092-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="41092-114">_ulSize_</span></span>
  
> <span data-ttu-id="41092-115">Die Größe des Puffers zuzuweisende in Bytes.</span><span class="sxs-lookup"><span data-stu-id="41092-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="41092-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="41092-116">_lppv_</span></span>
  
> <span data-ttu-id="41092-117">Ein Zeiger auf den zurückgegebenen zugewiesenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="41092-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="41092-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41092-118">Remarks</span></span>

 <span data-ttu-id="41092-119">**MAPIReallocateBuffer** ordnet einen neuen Block des Systemspeichers auf die angeforderte Größe und kopiert den Inhalt des Puffers übergeben wird, die in dieser neuen Block Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="41092-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="41092-120">Wenn der Block des Speichers, der übergeben wird interne Zeiger enthält, Ändern der Zeiger nicht entsprechend den neuen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="41092-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="41092-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41092-121">See also</span></span>



[<span data-ttu-id="41092-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="41092-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

