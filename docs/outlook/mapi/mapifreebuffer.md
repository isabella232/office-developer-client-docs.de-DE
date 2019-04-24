---
title: MAPIFreeBuffer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPIFreeBuffer
api_type:
- HeaderDef
ms.assetid: 9412594f-8acc-4c7e-a668-4ec1da0ad9cf
description: 'Letzte �nderung: Montag, 9. M�rz 2015'
ms.openlocfilehash: 8794bb233eb69d0f246fb1019954ab718db6f464
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346662"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="f9e1b-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="f9e1b-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="f9e1b-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f9e1b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f9e1b-105">Gibt einen Speicherpuffer frei, der mit einem Aufruf der [MAPIAllocateBuffer](mapiallocatebuffer.md) -Funktion oder der [MAPIAllocateMore](mapiallocatemore.md) -Funktion reserviert wurde.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="f9e1b-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="f9e1b-106">Header file:</span></span>  <br/> |<span data-ttu-id="f9e1b-107">Mapix. h</span><span class="sxs-lookup"><span data-stu-id="f9e1b-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="f9e1b-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="f9e1b-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f9e1b-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f9e1b-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f9e1b-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="f9e1b-110">Called by:</span></span>  <br/> |<span data-ttu-id="f9e1b-111">Client Anwendungen und Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="f9e1b-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="f9e1b-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="f9e1b-112">Parameters</span></span>

 <span data-ttu-id="f9e1b-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="f9e1b-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="f9e1b-114">in Zeiger auf einen zuvor reservierten Speicherpuffer.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="f9e1b-115">Wenn NULL im _lpBuffer_ -Parameter übergeben wird, bewirkt **mapifreebufferfreigegeben** nichts.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="f9e1b-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f9e1b-116">Return value</span></span>

<span data-ttu-id="f9e1b-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="f9e1b-117">S_OK</span></span> 
  
> <span data-ttu-id="f9e1b-118">Der Aufruf wurde erfolgreich durchgeführt und der angeforderte Arbeitsspeicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="f9e1b-119">**Mapifreebufferfreigegeben** kann auch S_OK auf bereits freigegebenen Speicherorten zurückgeben oder wenn der Speicherblock nicht mit **MAPIAllocateBuffer** und **MAPIAllocateMore**zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f9e1b-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9e1b-120">Remarks</span></span>

<span data-ttu-id="f9e1b-121">Wenn eine Clientanwendung oder ein Dienstanbieter [MAPIAllocateBuffer](mapiallocatebuffer.md) oder [MAPIAllocateMore](mapiallocatemore.md)aufruft, erstellt das Betriebssystem in der Regel eine oder mehrere komplexe Strukturen mit mehreren Zeiger Ebenen in einem zusammenhängenden Speicherpuffer.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="f9e1b-122">Wenn eine MAPI-Funktion oder-Methode einen Puffer mit solchen Inhalten erstellt, kann ein Client später alle im Puffer enthaltenen Strukturen freigeben, indem er an **mapifreebufferfreigegeben** den Zeiger auf den Puffer übergibt, der von der MAPI-Funktion zurückgegeben wurde, die den Puffer erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="f9e1b-123">Damit ein Dienstanbieter einen Speicherpuffer mithilfe von **mapifreebufferfreigegeben**freigeben kann, muss er den Zeiger an diesen Puffer übergeben, der mit dem Support Objekt des Anbieters zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="f9e1b-124">Der Aufruf an **mapifreebufferfreigegeben** , einen bestimmten Puffer freizugeben, muss vorgenommen werden, sobald ein Client oder Anbieter diesen Puffer verwendet.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="f9e1b-125">Beim einfachen Aufrufen der [IMAPISession:: Logout](imapisession-logoff.md) -Methode am Ende einer MAPI-Sitzung werden Speicherpuffer nicht automatisch freigegeben.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="f9e1b-126">Ein Client oder Dienstanbieter sollte davon ausgehen, dass der in _lpBuffer_ übergebene Zeiger nach einer erfolgreichen Rückgabe von **mapifreebufferfreigegeben**ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="f9e1b-127">Wenn der Zeiger entweder einen vom Messagingsystem nicht zugewiesenen Speicherblock über **MAPIAllocateBuffer** oder **MAPIAllocateMore** oder einen freien Speicherblock angibt, ist das Verhalten von **mapifreebufferfreigegeben** nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="f9e1b-128">Durch das Übergeben eines NULL-Zeigers an **mapifreebufferfreigegeben** wird der Anwendungs Bereinigungscode einfacher und kleiner, da **MAPIFREEBUFFERFREIGEGEBEN** Zeiger auf Null initialisieren und dann im Bereinigungscode freigeben kann, ohne Sie zuerst testen zu müssen.</span><span class="sxs-lookup"><span data-stu-id="f9e1b-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="f9e1b-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9e1b-129">See also</span></span>



[<span data-ttu-id="f9e1b-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="f9e1b-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

