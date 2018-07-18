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
ms.openlocfilehash: 22aad12010a4f367e18443d8c0831c6262cc37fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19793144"
---
# <a name="mapifreebuffer"></a><span data-ttu-id="c2184-103">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="c2184-103">MAPIFreeBuffer</span></span>

  
  
<span data-ttu-id="c2184-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c2184-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c2184-105">Gibt einen mit einem Aufruf der Funktion [MAPIAllocateBuffer](mapiallocatebuffer.md) oder die Funktion [MAPIAllocateMore](mapiallocatemore.md) reservierten Speicherpuffer frei.</span><span class="sxs-lookup"><span data-stu-id="c2184-105">Frees a memory buffer allocated with a call to the [MAPIAllocateBuffer](mapiallocatebuffer.md) function or the [MAPIAllocateMore](mapiallocatemore.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="c2184-106">Headerdatei</span><span class="sxs-lookup"><span data-stu-id="c2184-106">Header file:</span></span>  <br/> |<span data-ttu-id="c2184-107">Mapix.h</span><span class="sxs-lookup"><span data-stu-id="c2184-107">Mapix.h</span></span>  <br/> |
|<span data-ttu-id="c2184-108">Implementiert von:</span><span class="sxs-lookup"><span data-stu-id="c2184-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="c2184-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="c2184-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="c2184-110">Aufgerufen von:</span><span class="sxs-lookup"><span data-stu-id="c2184-110">Called by:</span></span>  <br/> |<span data-ttu-id="c2184-111">Clientanwendungen und -Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="c2184-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
ULONG MAPIFreeBuffer(
  LPVOID lpBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="c2184-112">Parameter</span><span class="sxs-lookup"><span data-stu-id="c2184-112">Parameters</span></span>

 <span data-ttu-id="c2184-113">_lpBuffer_</span><span class="sxs-lookup"><span data-stu-id="c2184-113">_lpBuffer_</span></span>
  
> <span data-ttu-id="c2184-114">[in] Zeiger auf einen Puffer zuvor reservierter Speicher.</span><span class="sxs-lookup"><span data-stu-id="c2184-114">[in] Pointer to a previously allocated memory buffer.</span></span> <span data-ttu-id="c2184-115">Wenn NULL in der _LpBuffer_ -Parameter übergeben wird, hat **MAPIFreeBuffer** keine Auswirkung.</span><span class="sxs-lookup"><span data-stu-id="c2184-115">If NULL is passed in the  _lpBuffer_ parameter, **MAPIFreeBuffer** does nothing.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="c2184-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="c2184-116">Return value</span></span>

<span data-ttu-id="c2184-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="c2184-117">S_OK</span></span> 
  
> <span data-ttu-id="c2184-118">Der Aufruf erfolgreich ausgeführt und den angeforderten Speicher freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c2184-118">The call succeeded and freed the memory requested.</span></span> <span data-ttu-id="c2184-119">**MAPIFreeBuffer** können auch S_OK zurückgeben, auf dem bereits freigegebenen Speicherorte oder wenn die Arbeitsspeicher-Block mit **MAPIAllocateBuffer** und **MAPIAllocateMore**kein Speicherplatz zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c2184-119">**MAPIFreeBuffer** can also return S_OK on already freed locations or if memory block is not allocated with **MAPIAllocateBuffer** and **MAPIAllocateMore**.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c2184-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c2184-120">Remarks</span></span>

<span data-ttu-id="c2184-121">In der Regel, wenn eine Clientanwendung oder Dienstanbieter [MAPIAllocateBuffer](mapiallocatebuffer.md) oder [MAPIAllocateMore](mapiallocatemore.md), der Betriebssystem-Konstrukte in einen zusammenhängenden Speicherpuffers einen oder mehrere komplexe Strukturen mit mehreren Ebenen von Zeigern aufruft.</span><span class="sxs-lookup"><span data-stu-id="c2184-121">Usually, when a client application or service provider calls [MAPIAllocateBuffer](mapiallocatebuffer.md) or [MAPIAllocateMore](mapiallocatemore.md), the operating system constructs in one contiguous memory buffer one or more complex structures with multiple levels of pointers.</span></span> <span data-ttu-id="c2184-122">Wenn ein MAPI-Funktion oder -Methode einen Puffer mit solchen Inhalte erstellt, kann ein Client später frei alle Strukturen, die im Puffer enthalten sind, indem Sie den Zeiger auf den Puffer zurückgegeben, die von der MAPI-Funktion, die den Puffer erstellt an **MAPIFreeBuffer** übergeben.</span><span class="sxs-lookup"><span data-stu-id="c2184-122">When a MAPI function or method creates a buffer with such contents, a client can later free all the structures contained in the buffer by passing to **MAPIFreeBuffer** the pointer to the buffer returned by the MAPI function that created the buffer.</span></span> <span data-ttu-id="c2184-123">Einem Dienstanbieter mit **MAPIFreeBuffer**Speicherpuffers frei muss er den Zeiger dem Puffer mit DSO-Objekt für den Anbieter zurückgegebenen bestehen.</span><span class="sxs-lookup"><span data-stu-id="c2184-123">For a service provider to free a memory buffer using **MAPIFreeBuffer**, it must pass the pointer to that buffer returned with the provider's support object.</span></span> 
  
<span data-ttu-id="c2184-124">Der Aufruf **MAPIFreeBuffer** auf einen bestimmten Puffer frei so bald wie ein Client vorgenommen werden muss, oder Anbieter wird nach Abschluss des Vorgangs mit diesen Puffer.</span><span class="sxs-lookup"><span data-stu-id="c2184-124">The call to **MAPIFreeBuffer** to free a particular buffer must be made as soon as a client or provider is finished using this buffer.</span></span> <span data-ttu-id="c2184-125">Einfach die [IMAPISession::Logoff](imapisession-logoff.md) -Methode aufruft, am Ende des MAPI-Sitzung wird nicht automatisch Speicherpuffern freigegeben.</span><span class="sxs-lookup"><span data-stu-id="c2184-125">Simply calling the [IMAPISession::Logoff](imapisession-logoff.md) method at the end of a MAPI session does not automatically release memory buffers.</span></span> 
  
<span data-ttu-id="c2184-126">Ein Client oder Dienstanbieter sollte auf der Annahme ausgeführt werden, dass nach dem erfolgreichen Beenden **MAPIFreeBuffer** _LpBuffer_ übergebene Zeiger ungültig ist.</span><span class="sxs-lookup"><span data-stu-id="c2184-126">A client or service provider should operate on the assumption that the pointer passed in  _lpBuffer_ is invalid after a successful return from **MAPIFreeBuffer**.</span></span> <span data-ttu-id="c2184-127">Wenn der Zeiger entweder einen nicht von der messaging-System über **MAPIAllocateBuffer** oder **MAPIAllocateMore** oder einen Speicherblock freien reservierten Arbeitsspeicher Block gibt, ist das Verhalten der **MAPIFreeBuffer** nicht definiert.</span><span class="sxs-lookup"><span data-stu-id="c2184-127">If the pointer indicates either a memory block not allocated by the messaging system through **MAPIAllocateBuffer** or **MAPIAllocateMore** or a free memory block, the behavior of **MAPIFreeBuffer** is undefined.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c2184-128">Übergeben einen null-Zeiger an **MAPIFreeBuffer** macht Anwendung Bereinigungscode einfacher und kleinere, da **MAPIFreeBuffer** können Zeiger auf NULL initialisiert, und klicken Sie dann in der Bereinigungscode frei, ohne sie zuerst zu testen.</span><span class="sxs-lookup"><span data-stu-id="c2184-128">Passing a null pointer to **MAPIFreeBuffer** makes application cleanup code simpler and smaller because **MAPIFreeBuffer** can initialize pointers to NULL and then free them in the cleanup code without having to test them first.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c2184-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2184-129">See also</span></span>



[<span data-ttu-id="c2184-130">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="c2184-130">IMAPISupport::GetMemAllocRoutines</span></span>](imapisupport-getmemallocroutines.md)

