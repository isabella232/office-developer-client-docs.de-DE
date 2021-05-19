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
ms.openlocfilehash: 59d0ce192605257dc0aebed46d8093a352fce05f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435285"
---
# <a name="mapireallocatebuffer"></a><span data-ttu-id="79859-103">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="79859-103">MAPIReallocateBuffer</span></span>

  
  
<span data-ttu-id="79859-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="79859-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="79859-105">Gibt einen Speicherpuffer neu zu.</span><span class="sxs-lookup"><span data-stu-id="79859-105">Reallocates a memory buffer.</span></span> <span data-ttu-id="79859-106">Es wird mit der [MAPIAllocateBuffer-Funktion](mapiallocatebuffer.md) verwendet.</span><span class="sxs-lookup"><span data-stu-id="79859-106">It is used with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="79859-107">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="79859-107">Header file:</span></span>  <br/> |<span data-ttu-id="79859-108">omapix.h</span><span class="sxs-lookup"><span data-stu-id="79859-108">omapix.h</span></span>  <br/> |
|<span data-ttu-id="79859-109">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="79859-109">Called by:</span></span>  <br/> |<span data-ttu-id="79859-110">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="79859-110">Client applications and service providers</span></span>  <br/> |
   
```cpp
STDMETHODIMP_(SCODE) MAPIReallocateBuffer
(
LPVOID lpv, 
ULONG ulSize, 
LPVOID * lppv
);
```

## <a name="parameters"></a><span data-ttu-id="79859-111">Parameter</span><span class="sxs-lookup"><span data-stu-id="79859-111">Parameters</span></span>

 <span data-ttu-id="79859-112">_lpv_</span><span class="sxs-lookup"><span data-stu-id="79859-112">_lpv_</span></span>
  
> <span data-ttu-id="79859-113">Ein Zeiger auf den speicher, der neu zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="79859-113">A pointer to the memory to be reallocated.</span></span>
    
 <span data-ttu-id="79859-114">_ulSize_</span><span class="sxs-lookup"><span data-stu-id="79859-114">_ulSize_</span></span>
  
> <span data-ttu-id="79859-115">Die Größe des zu zugeordneten Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="79859-115">The size, in bytes, of the buffer to be allocated.</span></span>
    
 <span data-ttu-id="79859-116">_lppv_</span><span class="sxs-lookup"><span data-stu-id="79859-116">_lppv_</span></span>
  
> <span data-ttu-id="79859-117">Ein Zeiger auf den zurückgegebenen zugewiesenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="79859-117">A pointer to the returned allocated buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="79859-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="79859-118">Remarks</span></span>

 <span data-ttu-id="79859-119">**MAPIReallocateBuffer** weist einen neuen Speicherblock der angeforderten Größe zu und kopiert den Inhalt des Puffers, der an diesen neuen Speicherblock übergeben wird.</span><span class="sxs-lookup"><span data-stu-id="79859-119">**MAPIReallocateBuffer** allocates a new block of memory of the requested size and copies the contents of the buffer that is passed into this new block of memory.</span></span> <span data-ttu-id="79859-120">Wenn der übergebene Speicherblock interne Zeiger enthält, ändern sich die Zeiger nicht an den neuen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="79859-120">If the block of memory that is passed contains internal pointers, the pointers do not change to match the new location.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="79859-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="79859-121">See also</span></span>



[<span data-ttu-id="79859-122">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="79859-122">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)

