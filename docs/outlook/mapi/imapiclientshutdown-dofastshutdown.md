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
# <a name="imapiclientshutdowndofastshutdown"></a><span data-ttu-id="f2562-103">IMAPIClientShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="f2562-103">IMAPIClientShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="f2562-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2562-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2562-105">Gibt die Absicht des MAPI-Clients an, den Clientprozess sofort zu beenden.</span><span class="sxs-lookup"><span data-stu-id="f2562-105">Indicates the intention of the MAPI client to exit the client process immediately.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="f2562-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="f2562-106">Return value</span></span>

<span data-ttu-id="f2562-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="f2562-107">S_OK</span></span>
  
> <span data-ttu-id="f2562-108">Das MAPI-Subsystem hat für geladene MAPI-Anbieter angegeben, dass der MAPI-Client sofort beendet wird, und die MAPI-Anbieter sind für den Clientabgang bereit.</span><span class="sxs-lookup"><span data-stu-id="f2562-108">The MAPI subsystem has indicated to loaded MAPI providers that the MAPI client is exiting immediately, and the MAPI providers are ready for the client exit.</span></span>
    
<span data-ttu-id="f2562-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="f2562-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="f2562-110">Das MAPI-Subsystem unterstützt kein schnelles Herunterfahren des Clients.</span><span class="sxs-lookup"><span data-stu-id="f2562-110">The MAPI subsystem does not support client fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="f2562-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2562-111">Remarks</span></span>

<span data-ttu-id="f2562-112">Um Datenverluste durch das schnelle Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die [Methoden IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) und **IMAPIClientShutdown::D oFastShutdown** basierend auf dem S_OK-Ergebnis aufrufen, das vom MAPI-Subsystem in der [IMAPIClientShutdown::QueryFastShutdown-Methode](imapiclientshutdown-queryfastshutdown.md) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="f2562-112">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the [IMAPIClientShutdown::NotifyProcessShutdown](imapiclientshutdown-notifyprocessshutdown.md) and **IMAPIClientShutdown::DoFastShutdown** methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="f2562-113">Weitere Informationen finden Sie unter [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="f2562-113">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="f2562-114">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2562-114">See also</span></span>



[<span data-ttu-id="f2562-115">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f2562-115">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="f2562-116">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="f2562-116">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

