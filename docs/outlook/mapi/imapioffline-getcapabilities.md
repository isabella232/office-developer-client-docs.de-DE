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
ms.openlocfilehash: 699e77479e0d09e7549c0d2741d5ba54ecc8ce33
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572032"
---
# <a name="imapiofflinegetcapabilities"></a><span data-ttu-id="fc94d-103">IMAPIOffline::GetCapabilities</span><span class="sxs-lookup"><span data-stu-id="fc94d-103">IMAPIOffline::GetCapabilities</span></span>

  
  
<span data-ttu-id="fc94d-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fc94d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fc94d-105">Ruft die Bedingungen für die Rückrufe durch eine offline-Objekt unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="fc94d-105">Gets the conditions for which callbacks are supported by an offline object.</span></span>
  
```cpp
HRESULT GetCapabilities( 
    ULONG *pulCapabilities 
);
```

## <a name="parameters"></a><span data-ttu-id="fc94d-106">Parameter</span><span class="sxs-lookup"><span data-stu-id="fc94d-106">Parameters</span></span>

 <span data-ttu-id="fc94d-107">_pulCapablities_</span><span class="sxs-lookup"><span data-stu-id="fc94d-107">_pulCapablities_</span></span>
  
> <span data-ttu-id="fc94d-108">[out] Eine Bitmaske der folgenden Funktion Flags:</span><span class="sxs-lookup"><span data-stu-id="fc94d-108">[out] A bitmask of the following capability flags:</span></span>
    
<span data-ttu-id="fc94d-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span><span class="sxs-lookup"><span data-stu-id="fc94d-109">MAPIOFFLINE_CAPABILITY_OFFLINE</span></span>
  
> <span data-ttu-id="fc94d-110">Das offline-Objekt ist offline Benachrichtigungen bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="fc94d-110">The offline object is capable of providing offline notifications.</span></span>
    
<span data-ttu-id="fc94d-111">MAPIOFFLINE_CAPABILITY_ONLINE</span><span class="sxs-lookup"><span data-stu-id="fc94d-111">MAPIOFFLINE_CAPABILITY_ONLINE</span></span>
  
> <span data-ttu-id="fc94d-112">Das offline-Objekt ist online Benachrichtigungen bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="fc94d-112">The offline object is capable of providing online notifications.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc94d-113">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="fc94d-113">Remarks</span></span>

<span data-ttu-id="fc94d-114">Beim Öffnen einer offline-Objekts mithilfe von **[HrOpenOfflineObj](hropenofflineobj.md)**, kann ein Client eine Abfrage auf [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) an, um einen Zeiger auf eine **IMAPIOffline** -Schnittstelle, und rufen **IMAPIOffline::GetCapabilities** , um die Rückrufe unterstützt zu erhalten durch das Objekt.</span><span class="sxs-lookup"><span data-stu-id="fc94d-114">Upon opening an offline object using **[HrOpenOfflineObj](hropenofflineobj.md)**, a client can query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md) to obtain a pointer to an **IMAPIOffline** interface, and call **IMAPIOffline::GetCapabilities** to find out the callbacks supported by the object.</span></span> <span data-ttu-id="fc94d-115">Der Client kann, wählen Sie dann mithilfe von **IMAPIOfflineMgr**Rückrufe eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="fc94d-115">The client can then choose to set up callbacks by using **IMAPIOfflineMgr**.</span></span>
  
<span data-ttu-id="fc94d-116">Beachten Sie, dass je nach den Mailserver für eine offline-Objekt, ein Objekt, das Rückrufe für den Onlinemodus wechseln unterstützt keine unbedingt Rückrufe unterstützt für den Wechsel in den Offlinemodus.</span><span class="sxs-lookup"><span data-stu-id="fc94d-116">Note that, depending on the mail server for an offline object, an object that supports callbacks for going online does not necessarily support callbacks for going offline.</span></span>
  
<span data-ttu-id="fc94d-117">Beachten Sie, dass auch während ein offline-Objekt kann Rückrufe für Änderungen als online/offline unterstützen, die Offline Zustand-API nur online/offline ändert sich unterstützt und Clients müssen für nur solche Funktionen überprüfen.</span><span class="sxs-lookup"><span data-stu-id="fc94d-117">Also note that, while an offline object may support callbacks for changes other than online/offline, the Offline State API supports only online/offline changes, and clients must check for only such capabilities.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="fc94d-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc94d-118">See also</span></span>



[<span data-ttu-id="fc94d-119">IMAPIOffline::GetCurrentState</span><span class="sxs-lookup"><span data-stu-id="fc94d-119">IMAPIOffline::GetCurrentState</span></span>](imapioffline-getcurrentstate.md)
  
[<span data-ttu-id="fc94d-120">IMAPIOffline::SetCurrentState</span><span class="sxs-lookup"><span data-stu-id="fc94d-120">IMAPIOffline::SetCurrentState</span></span>](imapioffline-setcurrentstate.md)
  
[<span data-ttu-id="fc94d-121">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="fc94d-121">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="fc94d-122">MAPI-Konstanten</span><span class="sxs-lookup"><span data-stu-id="fc94d-122">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="fc94d-123">HrOpenOfflineObj</span><span class="sxs-lookup"><span data-stu-id="fc94d-123">HrOpenOfflineObj</span></span>](hropenofflineobj.md)

