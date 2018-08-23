---
title: MAPIReallocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 182ab0c6-c9d3-4cc8-892f-f6b09312ceb9
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: e85e2da4d63442dc1fb912c5941be9d6f6f53824
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22593788"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="46ed5-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="46ed5-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="46ed5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="46ed5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="46ed5-105">Ordnet Speicherpuffers neu.</span><span class="sxs-lookup"><span data-stu-id="46ed5-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="46ed5-106">Es wird mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion verwendet.</span><span class="sxs-lookup"><span data-stu-id="46ed5-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="46ed5-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="46ed5-107">Header file:</span></span>  <br/> |<span data-ttu-id="46ed5-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="46ed5-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="46ed5-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="46ed5-109">Called by:</span></span>  <br/> |<span data-ttu-id="46ed5-110">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="46ed5-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="46ed5-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="46ed5-111">Parameters</span></span>

 <span data-ttu-id="46ed5-112">_LPV_</span><span class="sxs-lookup"><span data-stu-id="46ed5-112">_lpv_</span></span>
  
> <span data-ttu-id="46ed5-113">Ein Zeiger auf den Speicher neu reserviert werden.</span><span class="sxs-lookup"><span data-stu-id="46ed5-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="46ed5-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="46ed5-114">_ulSize_</span></span>
  
> <span data-ttu-id="46ed5-115">Die Größe des Puffers zuzuweisende in Bytes.</span><span class="sxs-lookup"><span data-stu-id="46ed5-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="46ed5-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="46ed5-116">_lppv_</span></span>
  
> <span data-ttu-id="46ed5-117">Ein Zeiger auf den zurückgegebenen zugewiesenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="46ed5-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="46ed5-118">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="46ed5-118">Remarks</span></span>

 <span data-ttu-id="46ed5-119">**MAPIReallocateBuffer** ordnet einen neuen Block des Systemspeichers auf die angeforderte Größe und kopiert den Inhalt des Puffers übergeben wird, die in dieser neuen Block Arbeitsspeicher.</span><span class="sxs-lookup"><span data-stu-id="46ed5-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="46ed5-120">Wenn der Block des Speichers, der übergeben wird interne Zeiger enthält, Ändern der Zeiger nicht entsprechend den neuen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="46ed5-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="46ed5-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46ed5-121">See also</span></span>



[<span data-ttu-id="46ed5-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="46ed5-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

