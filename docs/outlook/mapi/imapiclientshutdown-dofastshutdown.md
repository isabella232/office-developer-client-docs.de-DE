---
title: IMAPIClientShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: 310cba9a-a343-484d-a029-fcd51b731460
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 32a0051207ae34f919523fbfe3e01601b7ea5d2a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408684"
---
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="70110-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="70110-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="70110-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="70110-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="70110-105">Gibt an, dass der MAPI-Client sofort den Clientprozess beenden soll.</span><span class="sxs-lookup"><span data-stu-id="70110-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="70110-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="70110-106">Return value</span></span>

<span data-ttu-id="70110-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="70110-107">S_OK</span></span>
  
> <span data-ttu-id="70110-108">Das MAPI-Subsystem hat den geladenen MAPI-Anbietern angezeigt, dass der MAPI-Client sofort beendet wird, und die MAPI-Anbieter sind bereit für den Client-Exit.</span><span class="sxs-lookup"><span data-stu-id="70110-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="70110-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="70110-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="70110-110">Das MAPI-Subsystem unterstützt das schnelle Herunterfahren des Clients nicht.</span><span class="sxs-lookup"><span data-stu-id="70110-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="70110-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="70110-111">Remarks</span></span>

<span data-ttu-id="70110-112">Um Datenverluste beim schnellen Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die [IMAPIClientShutdown:: NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und **IMAPIClientShutdown::D ofastshutdown** -Methoden basierend auf dem vom MAPI-Subsystem zurückgegebenen Ergebnis S_OK in die [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="70110-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="70110-113">Weitere Informationen finden Sie unter [bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="70110-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="70110-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="70110-114">See also</span></span>



[<span data-ttu-id="70110-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="70110-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="70110-116">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="70110-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

