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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 04a9b631c3a4f33282bce44e06d92e089349c76b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792061"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="90f15-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="90f15-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="90f15-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90f15-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90f15-105">Gibt an, fahren Sie der Zweck der MAPI-Client, fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="90f15-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="90f15-106">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="90f15-106">Return value</span></span>

<span data-ttu-id="90f15-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="90f15-107">S_OK</span></span>
  
> <span data-ttu-id="90f15-108">MAPI-Subsystems hat versucht, um geladene MAPI-Anbieter zu benachrichtigen, dass der MAPI-Client wird ein Schnelles Herunterfahren führen.</span><span class="sxs-lookup"><span data-stu-id="90f15-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="90f15-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="90f15-109">Remarks</span></span>

<span data-ttu-id="90f15-110">Verlust von Daten über das schnelle Herunterfahren von einem MAPI-Client zu vermeiden, sollten MAPI-Clients die basierend auf dem S_OK Ergebnis des MAPI-Subsystems in zurückgegebene **IMAPIClientShutdown::NotifyProcessShutdown** und [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) -Methoden aufrufen. die [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="90f15-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="90f15-111">Weitere Informationen finden Sie unter [Bewährte Methoden für Schnelles Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="90f15-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="90f15-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90f15-112">See also</span></span>



[<span data-ttu-id="90f15-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="90f15-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="90f15-114">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="90f15-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

