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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 3cf8ad3966c44add3fd85b9f1adf677039bfce15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792242"
---
# <a name="imapiofflinegetcurrentstate"></a><span data-ttu-id="a73b4-103">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="a73b4-103">IMAPIOffline::GetCurrentState</span></span>

  
  
<span data-ttu-id="a73b4-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a73b4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a73b4-105">Ruft den aktuellen online oder offline-Status eines offline-Objekts ab.</span><span class="sxs-lookup"><span data-stu-id="a73b4-105">Gets the current online or offline state of an offline object.</span></span>
  
```cpp
HRESULT GetCurrentState( 
    ULONG* pulState 
);
```

## <a name="parameters"></a><span data-ttu-id="a73b4-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="a73b4-106">Parameters</span></span>

 <span data-ttu-id="a73b4-107">_pulState_</span><span class="sxs-lookup"><span data-stu-id="a73b4-107">_pulState_</span></span>
  
> <span data-ttu-id="a73b4-108">[out] Der aktuelle online oder offline Zustand eines offline-Objekts.</span><span class="sxs-lookup"><span data-stu-id="a73b4-108">[out] The current online or offline state of an offline object.</span></span> <span data-ttu-id="a73b4-109">Es muss eine der folgenden zwei Werte sein:</span><span class="sxs-lookup"><span data-stu-id="a73b4-109">It must be one of these two values:</span></span>
    
<span data-ttu-id="a73b4-110">MAPIOFFLINE_STATE_ONLINE</span><span class="sxs-lookup"><span data-stu-id="a73b4-110">MAPIOFFLINE_STATE_ONLINE</span></span>
  
> 
    
<span data-ttu-id="a73b4-111">MAPIOFFLINE_STATE_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="a73b4-111">MAPIOFFLINE_STATE_OFFLINE</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="a73b4-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a73b4-112">See also</span></span>



[<span data-ttu-id="a73b4-113">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="a73b4-113">IMAPIOffline::GetCapabilities</span></span>](imapioffline-getcapabilities.md)
  
[<span data-ttu-id="a73b4-114">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="a73b4-114">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)


[<span data-ttu-id="a73b4-115">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="a73b4-115">MAPI Constants</span></span>](mapi-constants.md)

