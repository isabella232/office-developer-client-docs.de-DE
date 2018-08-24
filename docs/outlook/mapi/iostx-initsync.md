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
ms.openlocfilehash: 5a0632ffd892c08fdf19de2c9b34607c27534f19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594040"
---
# <a name="iostxinitsync"></a><span data-ttu-id="b1f9c-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="b1f9c-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="b1f9c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b1f9c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b1f9c-105">Informiert dem lokalen Nachrichtenspeicher, dass Synchronisierung gestartet.</span><span class="sxs-lookup"><span data-stu-id="b1f9c-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="b1f9c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="b1f9c-106">Parameters</span></span>

 <span data-ttu-id="b1f9c-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b1f9c-107">_ulFlags_</span></span>
  
> <span data-ttu-id="b1f9c-108">[in] Kennzeichen, die um entsprechende Verhalten während der Synchronisierung zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="b1f9c-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="b1f9c-109">Outlook verwendet diese Flags in jedem Status des Computers Zustand Replikation, um die Informationen zu ermitteln, die für den Client bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="b1f9c-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="b1f9c-110">Angenommen, wenn der Client **SYNC_ONLY_ASSOCIATED**übergibt, wird Outlook nur Informationen im Zusammenhang mit der zugehörigen (oder ausgeblendet) Elemente zurück.</span><span class="sxs-lookup"><span data-stu-id="b1f9c-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b1f9c-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1f9c-111">See also</span></span>



[<span data-ttu-id="b1f9c-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="b1f9c-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="b1f9c-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="b1f9c-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="b1f9c-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="b1f9c-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="b1f9c-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="b1f9c-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="b1f9c-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="b1f9c-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="b1f9c-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="b1f9c-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="b1f9c-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b1f9c-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="b1f9c-119">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="b1f9c-119">MAPI Constants</span></span>](mapi-constants.md)

