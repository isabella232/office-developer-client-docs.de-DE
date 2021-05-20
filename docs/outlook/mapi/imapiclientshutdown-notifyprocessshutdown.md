---
title: IMAPIClientShutdownNotifyProcessShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.NotifyProcessShutdown
api_type:
- COM
ms.assetid: 42dd7889-5e00-419a-91e7-8350be4efd35
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 6eef3047368caca5bd932e19738b1d996c3ff28a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438869"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="815e7-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="815e7-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="815e7-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="815e7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="815e7-105">Gibt die Absicht des MAPI-Clients an, mit dem Herunterfahren fortzufahren.</span><span class="sxs-lookup"><span data-stu-id="815e7-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="815e7-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="815e7-106">Return value</span></span>

<span data-ttu-id="815e7-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="815e7-107">S_OK</span></span>
  
> <span data-ttu-id="815e7-108">Das MAPI-Subsystem hat versucht, geladene MAPI-Anbieter zu benachrichtigen, dass der MAPI-Client ein schnelles Herunterfahren ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="815e7-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="815e7-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="815e7-109">Remarks</span></span>

<span data-ttu-id="815e7-110">Um Datenverluste durch das schnelle Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die **Methoden IMAPIClientShutdown::NotifyProcessShutdown** und [IMAPIClientShutdown::D oFastShutdown](imapiclientshutdown-dofastshutdown.md) basierend auf dem S_OK-Ergebnis aufrufen, das vom MAPI-Subsystem in der [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="815e7-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="815e7-111">Weitere Informationen finden Sie unter [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="815e7-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="815e7-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="815e7-112">See also</span></span>



[<span data-ttu-id="815e7-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="815e7-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="815e7-114">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="815e7-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

