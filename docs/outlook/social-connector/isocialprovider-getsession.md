---
title: ISocialProviderGetSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 371b48c5-6d77-4d2d-890c-bb234c7eaabc
description: Ruft eine ISocialSession-Schnittstelle ab.
ms.openlocfilehash: afa13bddd5cbbc53081f6ae7ddcc1671d1c40303
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419548"
---
# <a name="isocialprovidergetsession"></a><span data-ttu-id="e27a1-103">ISocialProvider::GetSession</span><span class="sxs-lookup"><span data-stu-id="e27a1-103">ISocialProvider::GetSession</span></span>

<span data-ttu-id="e27a1-104">Ruft eine [ISocialSession-Schnittstelle](isocialsessioniunknown.md) ab.</span><span class="sxs-lookup"><span data-stu-id="e27a1-104">Gets an [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="e27a1-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="e27a1-105">Parameters</span></span>

<span data-ttu-id="e27a1-106">_session_</span><span class="sxs-lookup"><span data-stu-id="e27a1-106">_session_</span></span>
  
> <span data-ttu-id="e27a1-107">[out] Eine **ISocialSession**-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e27a1-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e27a1-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e27a1-108">Remarks</span></span>

<span data-ttu-id="e27a1-109">Das Outlook Social Connector (OSC) verwendet die **ISocialSession-Schnittstelle,** um sich beim sozialen Netzwerk zu melden.</span><span class="sxs-lookup"><span data-stu-id="e27a1-109">The Outlook Social Connector (OSC) uses the **ISocialSession** interface to log on to the social network.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e27a1-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e27a1-110">See also</span></span>

- [<span data-ttu-id="e27a1-111">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e27a1-111">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

