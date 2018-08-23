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
ms.openlocfilehash: 1c66032788758b04558a37a4c35ff4dd6c702fa2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568266"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="093f8-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="093f8-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="093f8-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="093f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="093f8-105">Gibt an, fahren Sie der Zweck der MAPI-Client, fortsetzen.</span><span class="sxs-lookup"><span data-stu-id="093f8-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="093f8-106">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="093f8-106">Return value</span></span>

<span data-ttu-id="093f8-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="093f8-107">S_OK</span></span>
  
> <span data-ttu-id="093f8-108">MAPI-Subsystems hat versucht, um geladene MAPI-Anbieter zu benachrichtigen, dass der MAPI-Client wird ein Schnelles Herunterfahren führen.</span><span class="sxs-lookup"><span data-stu-id="093f8-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="093f8-109">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="093f8-109">Remarks</span></span>

<span data-ttu-id="093f8-110">Verlust von Daten über das schnelle Herunterfahren von einem MAPI-Client zu vermeiden, sollten MAPI-Clients die basierend auf dem S_OK Ergebnis des MAPI-Subsystems in zurückgegebene **IMAPIClientShutdown::NotifyProcessShutdown** und [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) -Methoden aufrufen. die [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="093f8-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="093f8-111">Weitere Informationen finden Sie unter [Bewährte Methoden für Schnelles Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="093f8-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="093f8-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="093f8-112">See also</span></span>



[<span data-ttu-id="093f8-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="093f8-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="093f8-114">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="093f8-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

