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
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: 589ad42199e6f2ec1039499dfd9beda044ccc3dd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425694"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="e215a-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e215a-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="e215a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e215a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e215a-105">Weist einen Speicherpuffer zu.</span><span class="sxs-lookup"><span data-stu-id="e215a-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e215a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="e215a-106">Header file:</span></span>  <br/> |<span data-ttu-id="e215a-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="e215a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="e215a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="e215a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="e215a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="e215a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="e215a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="e215a-110">Called by:</span></span>  <br/> |<span data-ttu-id="e215a-111">Clientanwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="e215a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="e215a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="e215a-112">Parameters</span></span>

 <span data-ttu-id="e215a-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="e215a-113">_cbSize_</span></span>
  
> <span data-ttu-id="e215a-114">[in] Größe des zu zugeordneten Puffers in Bytes.</span><span class="sxs-lookup"><span data-stu-id="e215a-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="e215a-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="e215a-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="e215a-116">[out] Zeiger auf den zurückgegebenen zugewiesenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="e215a-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e215a-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="e215a-117">Return value</span></span>

<span data-ttu-id="e215a-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="e215a-118">S_OK</span></span> 
  
> <span data-ttu-id="e215a-119">Der Aufruf ist erfolgreich und hat den angeforderten Speicherpuffer zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e215a-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e215a-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e215a-120">Remarks</span></span>

<span data-ttu-id="e215a-121">Während **der MAPIAllocateBuffer-Anrufverarbeitung** erhält die aufrufende Implementierung einen Speicherblock vom Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="e215a-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="e215a-122">Der Speicherpuffer wird für eine byte-Adresse mit gleichmäßiger Nummer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="e215a-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="e215a-123">Auf Plattformen, auf denen der lange ganzzahlige Zugriff effizienter ist, ordnet das Betriebssystem den Puffer einer Adresse zu, deren Größe in Bytes ein Vielfaches von vier ist.</span><span class="sxs-lookup"><span data-stu-id="e215a-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="e215a-124">Durch Aufrufen der [MAPIFreeBuffer-Funktion](mapifreebuffer.md) wird der von **MAPIAllocateBuffer zugewiesene** Speicherpuffer durch Aufrufen der [MAPIAllocateMore-Funktion](mapiallocatemore.md) und mit ihr verknüpfter Puffer frei, wenn der Arbeitsspeicher nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e215a-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e215a-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e215a-125">See also</span></span>



[<span data-ttu-id="e215a-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="e215a-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

