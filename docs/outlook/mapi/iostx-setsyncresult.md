---
title: IOSTXSetSyncResult
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.SetSyncResult
api_type:
- COM
ms.assetid: 7f083ee0-bf36-0059-1589-66e454fe0098
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 74a4e299da6c0637c3da70c329569266d43dbd9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792709"
---
# <a name="iostxsetsyncresult"></a><span data-ttu-id="3986a-103">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="3986a-103">IOSTX::SetSyncResult</span></span>

  
  
<span data-ttu-id="3986a-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3986a-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3986a-105">Das Ergebnis der Synchronisierung festgelegt.</span><span class="sxs-lookup"><span data-stu-id="3986a-105">Sets the result of the synchronization.</span></span>
  
```cpp
HRESULT SetSyncResult( 
    HRESULT hrSync 
);
```

## <a name="parameters"></a><span data-ttu-id="3986a-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3986a-106">Parameters</span></span>

 <span data-ttu-id="3986a-107">_hrSync_</span><span class="sxs-lookup"><span data-stu-id="3986a-107">_hrSync_</span></span>
  
>  <span data-ttu-id="3986a-108">[in] Das Ergebnis der Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="3986a-108">[in] The result of the synchronization.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3986a-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3986a-109">Remarks</span></span>

<span data-ttu-id="3986a-110">Rufen Sie **IOSTX::SetSyncResult** vor **IOSTX::SyncEnd** , um den lokalen Speicher des Ergebnisses der Synchronisierung zu informieren.</span><span class="sxs-lookup"><span data-stu-id="3986a-110">Call **IOSTX::SetSyncResult** before calling **IOSTX::SyncEnd** to inform the local store of the result of synchronization.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3986a-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3986a-111">See also</span></span>



[<span data-ttu-id="3986a-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="3986a-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="3986a-113">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="3986a-113">IOSTX::InitSync</span></span>](iostx-initsync.md)
  
[<span data-ttu-id="3986a-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="3986a-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="3986a-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="3986a-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="3986a-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="3986a-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="3986a-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="3986a-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)


[<span data-ttu-id="3986a-118">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3986a-118">MAPI Constants</span></span>](mapi-constants.md)

