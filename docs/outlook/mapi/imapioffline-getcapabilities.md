---
title: IMAPIOfflineGetCapabilities
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline.GetCapabilities
api_type:
- COM
ms.assetid: aa8dc48b-9e1c-8da0-9579-10b7174e99de
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 48d59d17d81da2ae78348a57ad8b1cb75486b1a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433374"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="3735c-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="3735c-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="3735c-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3735c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3735c-105">Ruft die Bedingungen ab, für die Rückrufe von einem Offlineobjekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="3735c-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="3735c-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="3735c-106">Parameters</span></span>

 <span data-ttu-id="3735c-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="3735c-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="3735c-108">[out] Eine Bitmaske der folgenden Funktionskennzeichen:</span><span class="sxs-lookup"><span data-stu-id="3735c-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="3735c-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="3735c-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="3735c-110">Das Offlineobjekt kann Offlinebenachrichtigungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3735c-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="3735c-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="3735c-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="3735c-112">Das Offlineobjekt kann Onlinebenachrichtigungen bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3735c-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3735c-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3735c-113">Remarks</span></span>

<span data-ttu-id="3735c-114">Beim Öffnen eines Offlineobjekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)** kann ein Client [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) abfragen, um einen Zeiger auf eine **IMAPIOffline-Schnittstelle** zu erhalten, und **IMAPIOffline::GetCapabilities** aufrufen, um die vom Objekt unterstützten Rückrufe zu finden.</span><span class="sxs-lookup"><span data-stu-id="3735c-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="3735c-115">Der Client kann dann mithilfe von **IMAPIOfflineMgr** Rückrufe einrichten.</span><span class="sxs-lookup"><span data-stu-id="3735c-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="3735c-116">Beachten Sie, dass ein Objekt, das Rückrufe für den Onlinebetrieb unterstützt, abhängig vom E-Mail-Server für ein Offlineobjekt nicht unbedingt Rückrufe für den Offlinebetrieb unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3735c-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="3735c-117">Beachten Sie außerdem, dass ein Offlineobjekt zwar Rückrufe für andere Änderungen als Online/Offline unterstützt, die Offlinestatus-API jedoch nur Online-/Offlineänderungen unterstützt, und Clients müssen nur auf diese Funktionen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="3735c-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3735c-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3735c-118">See also</span></span>



[<span data-ttu-id="3735c-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="3735c-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="3735c-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="3735c-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="3735c-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="3735c-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="3735c-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="3735c-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="3735c-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="3735c-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

