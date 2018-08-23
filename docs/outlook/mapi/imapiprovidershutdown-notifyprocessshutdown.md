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
ms.openlocfilehash: 251359a98f89c88e707e4f705bd94b1f30b32cbd
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592052"
---
# <a name="imapiprovidershutdownnotifyprocessshutdown"></a><span data-ttu-id="b9cc4-103">IMAPIProviderShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="b9cc4-103">IMAPIProviderShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="b9cc4-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b9cc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b9cc4-105">Zeigt den MAPI-Anbieter, dass ein MAPI-Client ausführt, ein Schnelles Herunterfahren, so dass der Anbieter Aktionen, um Datenverlust zu vermeiden nutzen kann.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-105">Indicates to the MAPI provider that a MAPI client is going to do a fast shutdown, so that the provider can take actions to prevent data loss.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="b9cc4-106">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="b9cc4-106">Return value</span></span>

<span data-ttu-id="b9cc4-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="b9cc4-107">S_OK</span></span>
  
> <span data-ttu-id="b9cc4-108">MAPI-Anbieter ist Aktionen um Datenverlust zu vermeiden, wenn der MAPI-Client beendet wird.</span><span class="sxs-lookup"><span data-stu-id="b9cc4-108">The MAPI provider is taking actions to prevent data loss when the MAPI client shuts down.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="b9cc4-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b9cc4-109">See also</span></span>



[<span data-ttu-id="b9cc4-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b9cc4-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="b9cc4-111">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="b9cc4-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

