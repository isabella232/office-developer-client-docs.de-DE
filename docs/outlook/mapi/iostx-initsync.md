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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32317192"
---
# <a name="iostxinitsync"></a><span data-ttu-id="def1f-103">IOSTX::InitSync</span><span class="sxs-lookup"><span data-stu-id="def1f-103">IOSTX::InitSync</span></span>

  
  
<span data-ttu-id="def1f-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="def1f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="def1f-105">Informiert den lokalen Nachrichtenspeicher über die Synchronisierung, die gestartet werden soll.</span><span class="sxs-lookup"><span data-stu-id="def1f-105">Informs the local message store that synchronization is about to start.</span></span>
  
```cpp
HRESULT InitSync( 
    ULONG ulFlags 
);
```

## <a name="parameters"></a><span data-ttu-id="def1f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="def1f-106">Parameters</span></span>

 <span data-ttu-id="def1f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="def1f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="def1f-108">in Flags zum Bestimmen des geeigneten Verhaltens während der Synchronisierung.</span><span class="sxs-lookup"><span data-stu-id="def1f-108">[in] Flags to determine appropriate behavior during synchronization.</span></span> <span data-ttu-id="def1f-109">Outlook verwendet diese Flags in jedem Status des Replikationsstatus Computers, um die Informationen zu ermitteln, die für den Client bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="def1f-109">Outlook uses these flags in each state of the replication state machine to determine the information that it should provide for the client.</span></span> <span data-ttu-id="def1f-110">Wenn der Client beispielsweise **SYNC_ONLY_ASSOCIATED**übergibt, gibt Outlook nur Informationen zurück, die sich auf zugeordnete (oder ausgeblendete) Elemente beziehen.</span><span class="sxs-lookup"><span data-stu-id="def1f-110">For example, if the client passes **SYNC_ONLY_ASSOCIATED**, Outlook will only return information related to associated (or hidden) items.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="def1f-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="def1f-111">See also</span></span>



[<span data-ttu-id="def1f-112">IOSTX::GetLastError</span><span class="sxs-lookup"><span data-stu-id="def1f-112">IOSTX::GetLastError</span></span>](iostx-getlasterror.md)
  
[<span data-ttu-id="def1f-113">IOSTX::SetSyncResult</span><span class="sxs-lookup"><span data-stu-id="def1f-113">IOSTX::SetSyncResult</span></span>](iostx-setsyncresult.md)
  
[<span data-ttu-id="def1f-114">IOSTX::SyncBeg</span><span class="sxs-lookup"><span data-stu-id="def1f-114">IOSTX::SyncBeg</span></span>](iostx-syncbeg.md)
  
[<span data-ttu-id="def1f-115">IOSTX::SyncEnd</span><span class="sxs-lookup"><span data-stu-id="def1f-115">IOSTX::SyncEnd</span></span>](iostx-syncend.md)
  
[<span data-ttu-id="def1f-116">IOSTX::SyncHdrBeg</span><span class="sxs-lookup"><span data-stu-id="def1f-116">IOSTX::SyncHdrBeg</span></span>](iostx-synchdrbeg.md)
  
[<span data-ttu-id="def1f-117">IOSTX::SyncHdrEnd</span><span class="sxs-lookup"><span data-stu-id="def1f-117">IOSTX::SyncHdrEnd</span></span>](iostx-synchdrend.md)
  
[<span data-ttu-id="def1f-118">IOSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="def1f-118">IOSTX : IUnknown</span></span>](iostxiunknown.md)


[<span data-ttu-id="def1f-119">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="def1f-119">MAPI Constants</span></span>](mapi-constants.md)

