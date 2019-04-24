---
title: MAPIAllocateBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateBuffer
api_type:
- HeaderDef
ms.assetid: f1fc7fc5-c71f-44f7-930a-571773eb6809
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357309"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="0041b-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0041b-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="0041b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0041b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0041b-105">Weist einen Speicherpuffer zu.</span><span class="sxs-lookup"><span data-stu-id="0041b-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="0041b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="0041b-106">Header file:</span></span>  <br/> |<span data-ttu-id="0041b-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="0041b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="0041b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="0041b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="0041b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="0041b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="0041b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="0041b-110">Called by:</span></span>  <br/> |<span data-ttu-id="0041b-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="0041b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="0041b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="0041b-112">Parameters</span></span>

 <span data-ttu-id="0041b-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="0041b-113">_cbSize_</span></span>
  
> <span data-ttu-id="0041b-114">in Die Größe des Puffers in Byte, der reserviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="0041b-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="0041b-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="0041b-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="0041b-116">Out Zeiger auf den zurückgegebenen reservierten Puffer.</span><span class="sxs-lookup"><span data-stu-id="0041b-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0041b-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="0041b-117">Return value</span></span>

<span data-ttu-id="0041b-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="0041b-118">S_OK</span></span> 
  
> <span data-ttu-id="0041b-119">Der Aufruf war erfolgreich, und der angeforderte Speicherpuffer wurde zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="0041b-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0041b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0041b-120">Remarks</span></span>

<span data-ttu-id="0041b-121">Während der **MAPIAllocateBuffer** -Anrufverarbeitung erwirbt die aufrufende Implementierung einen Speicherblock vom Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="0041b-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="0041b-122">Der Arbeitsspeicherpuffer wird für eine gerade nummerierte Byte-Adresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="0041b-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="0041b-123">Auf Plattformen, auf denen der Zugriff auf lange ganze Zahlen effizienter ist, weist das Betriebssystem den Puffer einer Adresse zu, deren Größe in Byte ein Vielfaches von vier ist.</span><span class="sxs-lookup"><span data-stu-id="0041b-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="0041b-124">Das Aufrufen der [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion gibt den von **MAPIAllocateBuffer**zugewiesenen Speicherpuffer frei, indem die [MAPIAllocateMore](mapiallocatemore.md) -Funktion und alle damit verknüpften Puffer aufgerufen werden, wenn der Arbeitsspeicher nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="0041b-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0041b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0041b-125">See also</span></span>



[<span data-ttu-id="0041b-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="0041b-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

