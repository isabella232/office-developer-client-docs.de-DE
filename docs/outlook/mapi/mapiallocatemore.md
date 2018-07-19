---
title: MAPIAllocateMore
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIAllocateMore
api_type:
- HeaderDef
ms.assetid: 3e48f76a-bc97-4cbc-9082-c07dd674b73e
description: 'Letzte Änderung: Montag, 9. März 2015'
ms.openlocfilehash: f6f986ae811f2c7a886231a3046038889b82d683
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793120"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="95bec-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="95bec-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="95bec-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="95bec-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="95bec-105">Ordnet Speicherpuffers, die mit einer anderen zuvor mit der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) reservierten Puffer verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="95bec-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="95bec-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="95bec-106">Header file:</span></span>  <br/> |<span data-ttu-id="95bec-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="95bec-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="95bec-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="95bec-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="95bec-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="95bec-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="95bec-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="95bec-110">Called by:</span></span>  <br/> |<span data-ttu-id="95bec-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="95bec-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="95bec-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="95bec-112">Parameters</span></span>

 <span data-ttu-id="95bec-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="95bec-113">_cbSize_</span></span>
  
> <span data-ttu-id="95bec-114">[in] Größe in Bytes des neuen Puffers zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="95bec-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="95bec-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="95bec-115">_lpObject_</span></span>
  
> <span data-ttu-id="95bec-116">[in] Zeiger auf eine vorhandene MAPI-Puffer mit **MAPIAllocateBuffer**reserviert.</span><span class="sxs-lookup"><span data-stu-id="95bec-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="95bec-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="95bec-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="95bec-118">[out] Zeiger auf das zurückgegebene Puffer neu zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="95bec-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="95bec-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="95bec-119">Return value</span></span>

<span data-ttu-id="95bec-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="95bec-120">S_OK</span></span> 
  
> <span data-ttu-id="95bec-121">Der Aufruf erfolgreich ausgeführt und hat einen Zeiger auf den angeforderten Speicher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="95bec-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="95bec-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95bec-122">Remarks</span></span>

<span data-ttu-id="95bec-123">Rufen Sie während der **MAPIAllocateMore** Verarbeitung, die aufrufende Implementierung erhält einen Block von Arbeitsspeicher vom Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="95bec-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="95bec-124">Der Arbeitsspeicherpuffer wird auf einer geraden Byteadresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="95bec-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="95bec-125">Auf Plattformen, auf dem vom Typ long Integer Access effizienter ist, weist das Betriebssystem den Puffer auf eine Adresse, deren Größe in Byte ein Vielfaches von vier ist.</span><span class="sxs-lookup"><span data-stu-id="95bec-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="95bec-126">Die einzige Möglichkeit, einen Puffer mit **MAPIAllocateMore** reservierte Version ist, übergeben den Zeiger auf den Puffer im _LpObject_ -Parameter an die Funktion [MAPIFreeBuffer](mapifreebuffer.md) angegeben.</span><span class="sxs-lookup"><span data-stu-id="95bec-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="95bec-127">Die Verknüpfung zwischen den Speicherpuffern mit [MAPIAllocateBuffer](mapiallocatebuffer.md) und **MAPIAllocateMore** reserviert ermöglicht **MAPIFreeBuffer** , beide Puffer mit einem einzigen Aufruf freizugeben.</span><span class="sxs-lookup"><span data-stu-id="95bec-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

