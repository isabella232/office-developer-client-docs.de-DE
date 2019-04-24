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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351359"
---
# <a name="imapiclientshutdownnotifyprocessshutdown"></a><span data-ttu-id="3595a-103">IMAPIClientShutdown::NotifyProcessShutdown</span><span class="sxs-lookup"><span data-stu-id="3595a-103">IMAPIClientShutdown::NotifyProcessShutdown</span></span>

  
  
<span data-ttu-id="3595a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3595a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3595a-105">Gibt an, dass der MAPI-Client mit dem Herunterfahren fortfahren soll.</span><span class="sxs-lookup"><span data-stu-id="3595a-105">Indicates the intention of the MAPI client to proceed with shut down.</span></span>
  
```cpp
HRESULT NotifyProcessShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="3595a-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="3595a-106">Return value</span></span>

<span data-ttu-id="3595a-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="3595a-107">S_OK</span></span>
  
> <span data-ttu-id="3595a-108">Das MAPI-Subsystem hat versucht, geladene MAPI-Anbieter zu benachrichtigen, dass der MAPI-Client ein schnelles Herunterfahren durchführen wird.</span><span class="sxs-lookup"><span data-stu-id="3595a-108">The MAPI subsystem has attempted to notify loaded MAPI providers that the MAPI client is going to do a fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3595a-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3595a-109">Remarks</span></span>

<span data-ttu-id="3595a-110">Um Datenverluste beim schnellen Herunterfahren eines MAPI-Clients zu vermeiden, sollten MAPI-Clients die **IMAPIClientShutdown:: NotifyProcessShutdown** und [IMAPIClientShutdown::D ofastshutdown](imapiclientshutdown-dofastshutdown.md) -Methoden basierend auf dem vom MAPI-Subsystem zurückgegebenen Ergebnis S_OK in die [IMAPIClientShutdown:: QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) -Methode.</span><span class="sxs-lookup"><span data-stu-id="3595a-110">To avoid data loss from the fast shutdown of a MAPI client, MAPI clients should call the **IMAPIClientShutdown::NotifyProcessShutdown** and [IMAPIClientShutdown::DoFastShutdown](imapiclientshutdown-dofastshutdown.md) methods based on the S_OK result returned by the MAPI subsystem in the [IMAPIClientShutdown::QueryFastShutdown](imapiclientshutdown-queryfastshutdown.md) method.</span></span> <span data-ttu-id="3595a-111">Weitere Informationen finden Sie unter [bewährte Methoden für das schnelle Herunterfahren](best-practices-for-fast-shutdown.md).</span><span class="sxs-lookup"><span data-stu-id="3595a-111">For more information, see [Best Practices for Fast Shutdown](best-practices-for-fast-shutdown.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3595a-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3595a-112">See also</span></span>



[<span data-ttu-id="3595a-113">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3595a-113">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="3595a-114">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="3595a-114">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

