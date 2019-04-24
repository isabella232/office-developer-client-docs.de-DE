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
ms.openlocfilehash: e988114e8e71ad1f80d20ab0d5a30c37425f5952
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315057"
---
# <a name="ipstx2setspoolsuspendstate"></a><span data-ttu-id="ec5bf-103">IPSTX2::SetSpoolSuspendState</span><span class="sxs-lookup"><span data-stu-id="ec5bf-103">IPSTX2::SetSpoolSuspendState</span></span>

  
  
<span data-ttu-id="ec5bf-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ec5bf-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ec5bf-105">Legt den angehalten-Status für den Spooler fest.</span><span class="sxs-lookup"><span data-stu-id="ec5bf-105">Sets the suspended state on the spooler.</span></span>
  
```cpp
void SetSpoolSuspendState( 
    ULONG ulState 
);
```

## <a name="parameters"></a><span data-ttu-id="ec5bf-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="ec5bf-106">Parameters</span></span>

 <span data-ttu-id="ec5bf-107">_ulState_</span><span class="sxs-lookup"><span data-stu-id="ec5bf-107">_ulState_</span></span>
  
> <span data-ttu-id="ec5bf-108">in Der Zustand, auf den der Spooler festgelegt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ec5bf-108">[in] The state to set the spooler to.</span></span> <span data-ttu-id="ec5bf-109">Dabei muss es sich um einen der folgenden Werte handeln:</span><span class="sxs-lookup"><span data-stu-id="ec5bf-109">It must be one of the following values:</span></span>
    
 <span data-ttu-id="ec5bf-110">**SS_ACTIVE**</span><span class="sxs-lookup"><span data-stu-id="ec5bf-110">**SS_ACTIVE**</span></span>
  
> 
    
 <span data-ttu-id="ec5bf-111">**SS_SUSPENDED**</span><span class="sxs-lookup"><span data-stu-id="ec5bf-111">**SS_SUSPENDED**</span></span>
  
> 
    
## <a name="see-also"></a><span data-ttu-id="ec5bf-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ec5bf-112">See also</span></span>



[<span data-ttu-id="ec5bf-113">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="ec5bf-113">MAPI Constants</span></span>](mapi-constants.md)

