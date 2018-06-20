---
title: IMAPISupportGetMemAllocRoutines
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.GetMemAllocRoutines
api_type:
- COM
ms.assetid: 52d45876-367b-42da-b99a-29cdb71fa5a9
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 782c04d05ea5cea811784b031e8a118a9c08cbb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792380"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="b51eb-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="b51eb-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="b51eb-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="b51eb-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="b51eb-105">Ruft die Adressen der MAPI-Speicher Reservierung und Freigabe Funktionen ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="b51eb-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="b51eb-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b51eb-106">Parameters</span></span>

 <span data-ttu-id="b51eb-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="b51eb-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="b51eb-108">[out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateBuffer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b51eb-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="b51eb-109">**MAPIAllocateBuffer** belegt.</span><span class="sxs-lookup"><span data-stu-id="b51eb-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="b51eb-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="b51eb-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="b51eb-111">[out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateMore** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b51eb-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="b51eb-112">**MAPIAllocateMore** weist zusätzlichen Arbeitsspeicher für Speicher, der ursprünglich mithilfe von **MAPIAllocateBuffer**zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="b51eb-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="b51eb-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="b51eb-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="b51eb-114">[out] Ein Zeiger auf einen Zeiger auf die **MAPIFreeBuffer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="b51eb-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="b51eb-115">**MAPIFreeBuffer** gibt Speicherplatz frei.</span><span class="sxs-lookup"><span data-stu-id="b51eb-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="b51eb-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b51eb-116">Return value</span></span>

<span data-ttu-id="b51eb-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="b51eb-117">S_OK</span></span> 
  
> <span data-ttu-id="b51eb-118">Die Funktion Adressen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b51eb-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b51eb-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b51eb-119">Remarks</span></span>

<span data-ttu-id="b51eb-120">Die **IMAPISupport::GetMemAllocRoutines** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="b51eb-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="b51eb-121">Dienstanbieter anrufen **GetMemAllocRoutines** , um die Adressen der drei Speicherverwaltungsfunktionen abrufen, die an ihre Initialisierungsfunktion ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)oder [XPProviderInit](xpproviderinit.md)) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="b51eb-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b51eb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b51eb-122">See also</span></span>



[<span data-ttu-id="b51eb-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="b51eb-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="b51eb-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="b51eb-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="b51eb-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b51eb-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b51eb-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b51eb-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

