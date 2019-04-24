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
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 01980b2da735838eeffa9afa5a0d139b69e76d0c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357316"
---
# <a name="mapiallocatemore"></a><span data-ttu-id="77d6a-103">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="77d6a-103">MAPIAllocateMore</span></span>

  
  
<span data-ttu-id="77d6a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="77d6a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="77d6a-105">Reserviert einen Arbeitsspeicherpuffer, der mit einem anderen Puffer verknüpft ist, der zuvor mit der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion reserviert wurde.</span><span class="sxs-lookup"><span data-stu-id="77d6a-105">Allocates a memory buffer that is linked to another buffer previously allocated with the [MAPIAllocateBuffer](mapiallocatebuffer.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="77d6a-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="77d6a-106">Header file:</span></span>  <br/> |<span data-ttu-id="77d6a-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="77d6a-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="77d6a-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="77d6a-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="77d6a-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="77d6a-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="77d6a-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="77d6a-110">Called by:</span></span>  <br/> |<span data-ttu-id="77d6a-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="77d6a-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
SCODE MAPIAllocateMore(
  ULONG cbSize,
  LPVOID lpObject,
  LPVOID FAR * lppBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="77d6a-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="77d6a-112">Parameters</span></span>

 <span data-ttu-id="77d6a-113">_cbSize_</span><span class="sxs-lookup"><span data-stu-id="77d6a-113">_cbSize_</span></span>
  
> <span data-ttu-id="77d6a-114">in Die Größe des neuen Puffers in Bytes, der reserviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="77d6a-114">[in] Size, in bytes, of the new buffer to be allocated.</span></span> 
    
 <span data-ttu-id="77d6a-115">_lpObject_</span><span class="sxs-lookup"><span data-stu-id="77d6a-115">_lpObject_</span></span>
  
> <span data-ttu-id="77d6a-116">in Zeiger auf einen vorhandenen MAPI-Puffer, der mit **MAPIAllocateBuffer**zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="77d6a-116">[in] Pointer to an existing MAPI buffer allocated using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="77d6a-117">_lppBuffer_</span><span class="sxs-lookup"><span data-stu-id="77d6a-117">_lppBuffer_</span></span>
  
> <span data-ttu-id="77d6a-118">Out Zeiger auf den zurückgegebenen, neu zugewiesenen Puffer.</span><span class="sxs-lookup"><span data-stu-id="77d6a-118">[out] Pointer to the returned, newly allocated buffer.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="77d6a-119">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="77d6a-119">Return value</span></span>

<span data-ttu-id="77d6a-120">S_OK</span><span class="sxs-lookup"><span data-stu-id="77d6a-120">S_OK</span></span> 
  
> <span data-ttu-id="77d6a-121">Der Aufruf war erfolgreich und hat einen Zeiger auf den angeforderten Speicher zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="77d6a-121">The call succeeded and has returned a pointer to the requested memory.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77d6a-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77d6a-122">Remarks</span></span>

<span data-ttu-id="77d6a-123">Während der **MAPIAllocateMore** -Anrufverarbeitung erwirbt die aufrufende Implementierung einen Speicherblock vom Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="77d6a-123">During **MAPIAllocateMore** call processing, the calling implementation acquires a block of memory from the operating system.</span></span> <span data-ttu-id="77d6a-124">Der Arbeitsspeicherpuffer wird für eine gerade nummerierte Byte-Adresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="77d6a-124">The memory buffer is allocated on an even-numbered byte address.</span></span> <span data-ttu-id="77d6a-125">Auf Plattformen, auf denen der Zugriff auf lange ganze Zahlen effizienter ist, weist das Betriebssystem den Puffer einer Adresse zu, deren Größe in Byte ein Vielfaches von vier ist.</span><span class="sxs-lookup"><span data-stu-id="77d6a-125">On platforms where long integer access is more efficient, the operating system allocates the buffer on an address whose size in bytes is a multiple of four.</span></span> 
  
<span data-ttu-id="77d6a-126">Die einzige Möglichkeit zum Freigeben eines mit **MAPIAllocateMore** zugeordneten Puffers besteht darin, den im _lpObject_ -Parameter angegebenen Pufferzeiger an die [mapifreebufferfreigegeben](mapifreebuffer.md) -Funktion zu übergeben.</span><span class="sxs-lookup"><span data-stu-id="77d6a-126">The only way to release a buffer allocated with **MAPIAllocateMore** is to pass the buffer pointer specified in the  _lpObject_ parameter to the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> <span data-ttu-id="77d6a-127">Die Verknüpfung zwischen den Speicherpuffern, die mit [MAPIAllocateBuffer](mapiallocatebuffer.md) und **MAPIAllocateMore** reserviert wurden, ermöglicht **mapifreebufferfreigegeben** das Freigeben beider Puffer mit einem einzelnen Aufruf.</span><span class="sxs-lookup"><span data-stu-id="77d6a-127">The link between the memory buffers allocated with [MAPIAllocateBuffer](mapiallocatebuffer.md) and **MAPIAllocateMore** enables **MAPIFreeBuffer** to release both buffers with a single call.</span></span> 
  

