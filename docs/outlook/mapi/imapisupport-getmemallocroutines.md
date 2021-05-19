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
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 680fd16771b62d705808a04d768115a076e54750
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415537"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="4f8aa-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="4f8aa-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="4f8aa-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4f8aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4f8aa-105">Ruft die Adressen der MapI-Speicherzuweisungs- und -deallocation-Funktionen ab ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="4f8aa-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="4f8aa-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="4f8aa-106">Parameters</span></span>

 <span data-ttu-id="4f8aa-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="4f8aa-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="4f8aa-108">[out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateBuffer-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="4f8aa-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="4f8aa-109">**MAPIAllocateBuffer weist** Speicher zu.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="4f8aa-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="4f8aa-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="4f8aa-111">[out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateMore-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="4f8aa-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="4f8aa-112">**MAPIAllocateMore** weist zusätzlichen Arbeitsspeicher für speicher zu, der ursprünglich mithilfe von **MAPIAllocateBuffer zugewiesen wurde.**</span><span class="sxs-lookup"><span data-stu-id="4f8aa-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="4f8aa-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="4f8aa-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="4f8aa-114">[out] Ein Zeiger auf einen Zeiger auf die **MAPIFreeBuffer-Funktion.**</span><span class="sxs-lookup"><span data-stu-id="4f8aa-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="4f8aa-115">**MAPIFreeBuffer gibt** Arbeitsspeicher frei.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="4f8aa-116">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="4f8aa-116">Return value</span></span>

<span data-ttu-id="4f8aa-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="4f8aa-117">S_OK</span></span> 
  
> <span data-ttu-id="4f8aa-118">Die Funktionsadressen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="4f8aa-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4f8aa-119">Remarks</span></span>

<span data-ttu-id="4f8aa-120">Die **IMAPISupport::GetMemAllocRoutines-Methode** wird für alle Supportobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="4f8aa-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="4f8aa-121">Dienstanbieter rufen **GetMemAllocRoutines auf,** um die Adressen der drei Speicherzuweisungsfunktionen zu erhalten, die an ihre Initialisierungsfunktion übergeben werden ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)oder [XPProviderInit](xpproviderinit.md)).</span><span class="sxs-lookup"><span data-stu-id="4f8aa-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4f8aa-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f8aa-122">See also</span></span>



[<span data-ttu-id="4f8aa-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="4f8aa-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="4f8aa-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="4f8aa-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="4f8aa-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="4f8aa-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="4f8aa-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="4f8aa-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

