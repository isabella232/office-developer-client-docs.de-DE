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
ms.openlocfilehash: 9c29011ae2e9b59a7a0a38148fa6c5b673fd9590
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332165"
---
# <a name="iostxgetlasterror"></a><span data-ttu-id="edc4a-103">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="edc4a-103">IOSTX::GetLastError</span></span>

  
  
<span data-ttu-id="edc4a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="edc4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="edc4a-105">Ruft erweiterte Informationen zum letzten Fehler ab.</span><span class="sxs-lookup"><span data-stu-id="edc4a-105">Gets extended information about the last error.</span></span>
  
```cpp
HRESULT GetLastError( 
    HRESULT hResult, 
    ULONG ulFlags, 
    LPMAPIERROR *lppMAPIError 
);
```

## <a name="parameters"></a><span data-ttu-id="edc4a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="edc4a-106">Parameters</span></span>

 <span data-ttu-id="edc4a-107">_hResult_</span><span class="sxs-lookup"><span data-stu-id="edc4a-107">_hResult_</span></span>
  
>  <span data-ttu-id="edc4a-108">in Fehlercode.</span><span class="sxs-lookup"><span data-stu-id="edc4a-108">[in] Error code.</span></span> 
    
 <span data-ttu-id="edc4a-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="edc4a-109">_ulFlags_</span></span>
  
>  <span data-ttu-id="edc4a-110">[in] Flags, die Verhalten ändern.</span><span class="sxs-lookup"><span data-stu-id="edc4a-110">[in] Flags to modify behavior.</span></span> <span data-ttu-id="edc4a-111">Dies muss 0 sein.</span><span class="sxs-lookup"><span data-stu-id="edc4a-111">This must be 0.</span></span> 
    
 <span data-ttu-id="edc4a-112">_lppMAPIError_</span><span class="sxs-lookup"><span data-stu-id="edc4a-112">_lppMAPIError_</span></span>
  
>  <span data-ttu-id="edc4a-113">Out Zeiger auf die **MAPIERROR** -Struktur, die die erweiterten Informationen für den Fehler enthält.</span><span class="sxs-lookup"><span data-stu-id="edc4a-113">[out] Pointer to the **MAPIERROR** structure that contains the extended information for the error.</span></span> <span data-ttu-id="edc4a-114">Weitere Informationen finden Sie unter mapidefs. h für die Typdefinition von **LPMAPIERROR**.</span><span class="sxs-lookup"><span data-stu-id="edc4a-114">See mapidefs.h for the type definition of **LPMAPIERROR**.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="edc4a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edc4a-115">See also</span></span>



[<span data-ttu-id="edc4a-116">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="edc4a-116">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="edc4a-117">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="edc4a-117">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="edc4a-118">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="edc4a-118">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="edc4a-119">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="edc4a-119">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="edc4a-120">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="edc4a-120">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="edc4a-121">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="edc4a-121">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="edc4a-122">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="edc4a-122">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="edc4a-123">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="edc4a-123">MAPI Constants</span></span>](mapi-constants.md)

