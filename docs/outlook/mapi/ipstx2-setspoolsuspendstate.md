---
title: IPSTX2SetSpoolSuspendState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX2.SetSpoolSuspendState
api_type:
- COM
ms.assetid: 396db029-1d4a-203d-2256-3353d03c6767
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b6a36c1e0c3854342b627b6fddd6eb5459211f62
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590428"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="6463f-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="6463f-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="6463f-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6463f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6463f-105">Legt den angehaltenen Zustand auf die Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="6463f-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="6463f-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="6463f-106">Parameters</span></span>

 <span data-ttu-id="6463f-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="6463f-107">_ulState_</span></span>
  
> <span data-ttu-id="6463f-108">[in] Der Zustand, legen Sie die Warteschlange auf.</span><span class="sxs-lookup"><span data-stu-id="6463f-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="6463f-109">Es muss eine der folgenden Werte sein:</span><span class="sxs-lookup"><span data-stu-id="6463f-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="6463f-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="6463f-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="6463f-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="6463f-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="6463f-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6463f-112">See also</span></span>



[<span data-ttu-id="6463f-113">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="6463f-113">MAPI Constants</span></span>](mapi-constants.md)

