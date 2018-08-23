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
ms.openlocfilehash: c3ec99e4e284ca2cdc4fba8fcf53a6c5741594cb
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577814"
---
# <a name="imapisupportgetmemallocroutines"></a><span data-ttu-id="bef4f-103">IMAPISupport::GetMemAllocRoutines</span><span class="sxs-lookup"><span data-stu-id="bef4f-103">IMAPISupport::GetMemAllocRoutines</span></span>

  
  
<span data-ttu-id="bef4f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bef4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bef4f-105">Ruft die Adressen der MAPI-Speicher Reservierung und Freigabe Funktionen ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md)und [MAPIFreeBuffer](mapifreebuffer.md)).</span><span class="sxs-lookup"><span data-stu-id="bef4f-105">Retrieves the addresses of the MAPI memory allocation and deallocation functions ([MAPIAllocateBuffer](mapiallocatebuffer.md), [MAPIAllocateMore](mapiallocatemore.md), and [MAPIFreeBuffer](mapifreebuffer.md)).</span></span>
  
```cpp
HRESULT GetMemAllocRoutines(
  LPALLOCATEBUFFER FAR * lppAllocateBuffer,
  LPALLOCATEMORE FAR * lppAllocateMore,
  LPFREEBUFFER FAR * lppFreeBuffer
);
```

## <a name="parameters"></a><span data-ttu-id="bef4f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="bef4f-106">Parameters</span></span>

 <span data-ttu-id="bef4f-107">_lppAllocateBuffer_</span><span class="sxs-lookup"><span data-stu-id="bef4f-107">_lppAllocateBuffer_</span></span>
  
> <span data-ttu-id="bef4f-108">[out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateBuffer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bef4f-108">[out] A pointer to a pointer to the **MAPIAllocateBuffer** function.</span></span> <span data-ttu-id="bef4f-109">**MAPIAllocateBuffer** belegt.</span><span class="sxs-lookup"><span data-stu-id="bef4f-109">**MAPIAllocateBuffer** allocates memory.</span></span> 
    
 <span data-ttu-id="bef4f-110">_lppAllocateMore_</span><span class="sxs-lookup"><span data-stu-id="bef4f-110">_lppAllocateMore_</span></span>
  
> <span data-ttu-id="bef4f-111">[out] Ein Zeiger auf einen Zeiger auf die **MAPIAllocateMore** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bef4f-111">[out] A pointer to a pointer to the **MAPIAllocateMore** function.</span></span> <span data-ttu-id="bef4f-112">**MAPIAllocateMore** weist zusätzlichen Arbeitsspeicher für Speicher, der ursprünglich mithilfe von **MAPIAllocateBuffer**zugewiesen wurde.</span><span class="sxs-lookup"><span data-stu-id="bef4f-112">**MAPIAllocateMore** allocates additional memory for memory that was originally allocated by using **MAPIAllocateBuffer**.</span></span>
    
 <span data-ttu-id="bef4f-113">_lppFreeBuffer_</span><span class="sxs-lookup"><span data-stu-id="bef4f-113">_lppFreeBuffer_</span></span>
  
> <span data-ttu-id="bef4f-114">[out] Ein Zeiger auf einen Zeiger auf die **MAPIFreeBuffer** -Funktion.</span><span class="sxs-lookup"><span data-stu-id="bef4f-114">[out] A pointer to a pointer to the **MAPIFreeBuffer** function.</span></span> <span data-ttu-id="bef4f-115">**MAPIFreeBuffer** gibt Speicherplatz frei.</span><span class="sxs-lookup"><span data-stu-id="bef4f-115">**MAPIFreeBuffer** frees memory.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="bef4f-116">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="bef4f-116">Return value</span></span>

<span data-ttu-id="bef4f-117">S_OK</span><span class="sxs-lookup"><span data-stu-id="bef4f-117">S_OK</span></span> 
  
> <span data-ttu-id="bef4f-118">Die Funktion Adressen wurden erfolgreich zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="bef4f-118">The function addresses were successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bef4f-119">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="bef4f-119">Remarks</span></span>

<span data-ttu-id="bef4f-120">Die **IMAPISupport::GetMemAllocRoutines** -Methode wird für alle Unterstützungsobjekte implementiert.</span><span class="sxs-lookup"><span data-stu-id="bef4f-120">The **IMAPISupport::GetMemAllocRoutines** method is implemented for all support objects.</span></span> <span data-ttu-id="bef4f-121">Dienstanbieter anrufen **GetMemAllocRoutines** , um die Adressen der drei Speicherverwaltungsfunktionen abrufen, die an ihre Initialisierungsfunktion ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md)oder [XPProviderInit](xpproviderinit.md)) übergeben werden.</span><span class="sxs-lookup"><span data-stu-id="bef4f-121">Service providers call **GetMemAllocRoutines** to get the addresses of the three memory allocation functions that are passed to their initialization function ( [ABProviderInit](abproviderinit.md), [MSProviderInit](msproviderinit.md), or [XPProviderInit](xpproviderinit.md)).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="bef4f-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bef4f-122">See also</span></span>



[<span data-ttu-id="bef4f-123">MAPIAllocateBuffer</span><span class="sxs-lookup"><span data-stu-id="bef4f-123">MAPIAllocateBuffer</span></span>](mapiallocatebuffer.md)
  
[<span data-ttu-id="bef4f-124">MAPIAllocateMore</span><span class="sxs-lookup"><span data-stu-id="bef4f-124">MAPIAllocateMore</span></span>](mapiallocatemore.md)
  
[<span data-ttu-id="bef4f-125">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="bef4f-125">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="bef4f-126">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="bef4f-126">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

