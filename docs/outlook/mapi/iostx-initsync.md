---
title: IOSTXInitSync
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IOSTX.InitSync
api_type:
- COM
ms.assetid: e22244a2-ac5f-910a-501f-4483ea0667c2
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b9086383b45d40d5839284ac785d72438be60e00
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413353"
---
# <a name="iostxinitsync"></a><span data-ttu-id="633ab-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="633ab-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="633ab-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="633ab-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="633ab-105">Informiert den lokalen Nachrichtenspeicher darüber, dass die Synchronisierung gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="633ab-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="633ab-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="633ab-106">Parameters</span></span>

 <span data-ttu-id="633ab-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="633ab-107">_ulFlags_</span></span>
  
> <span data-ttu-id="633ab-108">[in] Flags, um das entsprechende Verhalten während der Synchronisierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="633ab-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="633ab-109">Outlook verwendet diese Flags in jedem Zustand des Replikationsstatuscomputers, um die Informationen zu bestimmen, die für den Client zur Verfügung stellen sollen.</span><span class="sxs-lookup"><span data-stu-id="633ab-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="633ab-110">Wenn der Client z. B. **SYNC_ONLY_ASSOCIATED,** gibt Outlook nur Informationen zu zugeordneten (oder ausgeblendeten) Elementen zurück.</span><span class="sxs-lookup"><span data-stu-id="633ab-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="633ab-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="633ab-111">See also</span></span>



[<span data-ttu-id="633ab-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="633ab-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="633ab-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="633ab-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="633ab-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="633ab-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="633ab-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="633ab-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="633ab-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="633ab-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="633ab-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="633ab-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="633ab-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="633ab-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="633ab-119">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="633ab-119">MAPI Constants</span></span>](mapi-constants.md)

