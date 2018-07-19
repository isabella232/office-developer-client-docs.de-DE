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
ms.openlocfilehash: 8ba00ecc1d9ff1c0b7db63d3e6d667b374245742
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793107"
---
# <a name="mapiallocatebuffer"></a><span data-ttu-id="be092-103">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="be092-103">MAPIAllocateBuffer</span></span>

  
  
<span data-ttu-id="be092-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="be092-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="be092-105">Ordnet einen Arbeitsspeicherpuffer.</span><span class="sxs-lookup"><span data-stu-id="be092-105">Allocates a memory buffer.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="be092-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="be092-106">Header file:</span></span>  <br/> |<span data-ttu-id="be092-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="be092-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="be092-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="be092-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="be092-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="be092-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="be092-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="be092-110">Called by:</span></span>  <br/> |<span data-ttu-id="be092-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="be092-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateBuffer(
  ULONG cbSize,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="be092-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="be092-112">Parameters</span></span>

 <span data-ttu-id="be092-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="be092-113">_cbSize_</span></span>
  
> <span data-ttu-id="be092-114">[in] Größe des Puffers zuzuweisende in Bytes.</span><span class="sxs-lookup"><span data-stu-id="be092-114">[in] Size, in bytes, of the buffer to be allocated.</span></span> 
    
 <span data-ttu-id="be092-115">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="be092-115">_lppBuffer_</span></span>
  
> <span data-ttu-id="be092-116">[out] Zeiger auf den zurückgegebenen zugewiesenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="be092-116">[out] Pointer to the returned allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="be092-117">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="be092-117">Return value</span></span>

<span data-ttu-id="be092-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="be092-118">S_OK</span></span> 
  
> <span data-ttu-id="be092-119">Der Aufruf erfolgreich ausgeführt und angeforderten Pufferüberläufe zurückgegeben hat.</span><span class="sxs-lookup"><span data-stu-id="be092-119">The call succeeded and has returned the requested memory buffer.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="be092-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="be092-120">Remarks</span></span>

<span data-ttu-id="be092-121">Rufen Sie während der **MAPIAllocateBuffer** Verarbeitung, die aufrufende Implementierung erhält einen Block von Arbeitsspeicher vom Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="be092-121">During **MAPIAllocateBuffer** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="be092-122">Der Arbeitsspeicherpuffer wird auf einer geraden Byteadresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="be092-122">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="be092-123">Auf Plattformen, auf dem vom Typ long Integer Access effizienter ist, weist das Betriebssystem den Puffer auf eine Adresse, deren Größe in Byte ein Vielfaches von vier ist.</span><span class="sxs-lookup"><span data-stu-id="be092-123">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="be092-124">Die [MAPIFreeBuffer](mapifreebuffer.md) Funktion-Versionen aufrufen verknüpft der **MAPIAllocateBuffer**, durch Aufrufen der [MAPIAllocateMore](mapiallocatemore.md) -Funktion und alle Puffer reservierte Speicherpuffer, wenn der Speicher nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="be092-124">Calling the [MAPIFreeBuffer](mapifreebuffer.md) function releases the memory buffer allocated by **MAPIAllocateBuffer**, by calling the [MAPIAllocateMore](mapiallocatemore.md) function and any buffers linked to it, when the memory is no longer needed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="be092-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="be092-125">See also</span></span>



[<span data-ttu-id="be092-126">MAPIReallocateBuffer</span><span class="sxs-lookup"><span data-stu-id="be092-126">MAPIReallocateBuffer</span></span>](mapireallocatebuffer.md)

