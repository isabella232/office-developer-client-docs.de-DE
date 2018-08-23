---
title: IMAPIOfflineGetCurrentState
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCurrentState
api_type:
- COM
ms.assetid: f3769e83-d678-1087-fc0f-b4f156386333
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 5d6b1dfcd3866b0d0e7151e9d5399e1274810d14
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568203"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="9a3e5-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="9a3e5-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="9a3e5-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9a3e5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9a3e5-105">Ruft den aktuellen online oder offline-Status eines offline-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="9a3e5-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="9a3e5-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="9a3e5-106">Parameters</span></span>

 <span data-ttu-id="9a3e5-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="9a3e5-107">_pulState_</span></span>
  
> <span data-ttu-id="9a3e5-108">[out] Der aktuelle online oder offline Zustand eines offline-Objekts.</span><span class="sxs-lookup"><span data-stu-id="9a3e5-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="9a3e5-109">Es muss eine der folgenden zwei Werte sein:</span><span class="sxs-lookup"><span data-stu-id="9a3e5-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="9a3e5-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="9a3e5-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="9a3e5-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="9a3e5-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="9a3e5-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9a3e5-112">See also</span></span>



[<span data-ttu-id="9a3e5-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="9a3e5-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="9a3e5-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="9a3e5-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="9a3e5-115">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="9a3e5-115">MAPI Constants</span></span>](mapi-constants.md)

