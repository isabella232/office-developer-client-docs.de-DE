---
title: IMAPIProviderShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: a00d71b1-d705-40d5-b667-f91b57db85da
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4b18cfc2191ffee936e1056d9bb656a7ad7dd3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405247"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="9f015-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="9f015-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="9f015-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9f015-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9f015-105">Gibt dem MAPI-Anbieter an, dass ein MAPI-Client ein schnelles Herunterfahren durchführen soll, damit der Anbieter Maßnahmen ergreifen kann, um Datenverluste zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="9f015-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="9f015-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="9f015-106">Return value</span></span>

<span data-ttu-id="9f015-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="9f015-107">S_OK</span></span>
  
> <span data-ttu-id="9f015-108">Der MAPI-Anbieter führt Aktionen aus, um Datenverluste beim Herunterfahren des MAPI-Clients zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="9f015-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="9f015-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f015-109">See also</span></span>



[<span data-ttu-id="9f015-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9f015-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="9f015-111">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="9f015-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

