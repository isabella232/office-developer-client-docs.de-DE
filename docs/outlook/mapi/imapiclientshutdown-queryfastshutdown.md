---
title: IMAPIClientShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIClientShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: b743b5b6-4a7c-46b8-99eb-afd13ee947db
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 784a2f497811ba7c4ba0abf260ff32fde75de76a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584933"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="cee9e-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="cee9e-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="cee9e-104">**Betrifft**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cee9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cee9e-105">Abfragen des MAPI-Subsystems für Schnelles Herunterfahren unterstützt, die von geladenen MAPI-Anbieter bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cee9e-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="cee9e-106">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="cee9e-106">Return value</span></span>

<span data-ttu-id="cee9e-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="cee9e-107">S_OK</span></span>
  
> <span data-ttu-id="cee9e-108">MAPI-Subsystems unterstützt den MAPI-Client zum Herunterfahren schnelle.</span><span class="sxs-lookup"><span data-stu-id="cee9e-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="cee9e-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="cee9e-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="cee9e-110">MAPI-Anbieter unterstützt keine den MAPI-Client zum Herunterfahren schnelle.</span><span class="sxs-lookup"><span data-stu-id="cee9e-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="cee9e-111">HinwBemerkungeneise</span><span class="sxs-lookup"><span data-stu-id="cee9e-111">Remarks</span></span>

<span data-ttu-id="cee9e-112">Ob die MAPI-Subsystems auf Herunterfahren schnelle führen Sie den MAPI-Client unterstützt, hängt von Einstellung in der Windows-Registrierung des Benutzers oder das Standardverhalten des MAPI-Client für Schnelles Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="cee9e-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="cee9e-113">Außerdem hängt die Möglichkeit der geladenen MAPI-Anbieter zur Unterstützung von schnellen Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="cee9e-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="cee9e-114">Weitere Informationen finden Sie unter [Fast Herunterfahren Benutzeroptionen](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="cee9e-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="cee9e-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cee9e-115">See also</span></span>



[<span data-ttu-id="cee9e-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="cee9e-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="cee9e-117">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="cee9e-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

