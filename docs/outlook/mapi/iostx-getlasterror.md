---
title: IOSTXGetLastError
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.GetLastError
api_type:
- COM
ms.assetid: b25c9288-b391-6303-3643-5a5b66b75c48
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 78ae0f78e154c17f774817238b2083d98a8fb809
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584681"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="328f3-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="328f3-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="328f3-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="328f3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="328f3-105">Ruft Informationen über den letzten Fehler erweitert.</span><span class="sxs-lookup"><span data-stu-id="328f3-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="328f3-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="328f3-106">Parameters</span></span>

 <span data-ttu-id="328f3-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="328f3-107">_hResult_</span></span>
  
>  <span data-ttu-id="328f3-108">[in] Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="328f3-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="328f3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="328f3-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="328f3-110">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="328f3-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="328f3-111">Dies muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="328f3-111">This must be 0.</span></span> 
    
 <span data-ttu-id="328f3-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="328f3-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="328f3-113">[out] Zeiger auf die **MAPIERROR** -Struktur, die erweiterte Informationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="328f3-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="328f3-114">Finden Sie unter mapidefs.h für die Definition des **LPMAPIERROR**Typs.</span><span class="sxs-lookup"><span data-stu-id="328f3-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="328f3-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="328f3-115">See also</span></span>



[<span data-ttu-id="328f3-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="328f3-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="328f3-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="328f3-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="328f3-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="328f3-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="328f3-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="328f3-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="328f3-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="328f3-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="328f3-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="328f3-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="328f3-122">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="328f3-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="328f3-123">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="328f3-123">MAPI Constants</span></span>](mapi-constants.md)

