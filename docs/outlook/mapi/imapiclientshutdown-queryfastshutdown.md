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
ms.openlocfilehash: 6a76488f56f9d1eb1b344c01de2615627dd5d3ec
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418148"
---
# <a name="imapiclientshutdownqueryfastshutdown"></a><span data-ttu-id="49ae1-103">IMAPIClientShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="49ae1-103">IMAPIClientShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="49ae1-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="49ae1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="49ae1-105">Fragt das MAPI-Subsystem zur Unterstützung des schnellen Herunterfahrens ab, das von geladenen MAPI-Anbietern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="49ae1-105">Queries the MAPI subsystem for fast shutdown support that is provided by loaded MAPI providers.</span></span>
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="49ae1-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="49ae1-106">Return value</span></span>

<span data-ttu-id="49ae1-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="49ae1-107">S_OK</span></span>
  
> <span data-ttu-id="49ae1-108">Das MAPI-Subsystem unterstützt den MAPI-Client für schnelles Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="49ae1-108">The MAPI subsystem supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="49ae1-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="49ae1-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="49ae1-110">Der MAPI-Anbieter unterstützt den MAPI-Client nicht für schnelles Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="49ae1-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49ae1-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="49ae1-111">Remarks</span></span>

<span data-ttu-id="49ae1-112">Ob das MAPI-Subsystem den MAPI-Client für schnelles Herunterfahren unterstützt, hängt von der Windows-Registrierungseinstellung des Benutzers oder dem Standardverhalten des MAPI-Clients für schnelles Herunterfahren ab.</span><span class="sxs-lookup"><span data-stu-id="49ae1-112">Whether the MAPI subsystem supports the MAPI client to do fast shutdown depends on the user's Windows registry setting or the default behavior of the MAPI client for fast shutdown.</span></span> <span data-ttu-id="49ae1-113">Außerdem hängt es von der Fähigkeit der geladenen MAPI-Anbieter ab, das schnelle Herunterfahren zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="49ae1-113">It also depends on the ability of the loaded MAPI providers to support fast shutdown.</span></span> <span data-ttu-id="49ae1-114">Weitere Informationen finden Sie unter [Benutzeroptionen für das schnelle Herunterfahren](fast-shutdown-user-options.md).</span><span class="sxs-lookup"><span data-stu-id="49ae1-114">For more information, see [Fast Shutdown User Options](fast-shutdown-user-options.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49ae1-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49ae1-115">See also</span></span>



[<span data-ttu-id="49ae1-116">IMAPIClientShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49ae1-116">IMAPIClientShutdown : IUnknown</span></span>](imapiclientshutdowniunknown.md)


[<span data-ttu-id="49ae1-117">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="49ae1-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

