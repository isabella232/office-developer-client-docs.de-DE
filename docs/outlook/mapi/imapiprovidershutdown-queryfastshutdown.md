---
title: IMAPIProviderShutdownQueryFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.QueryFastShutdown
api_type:
- COM
ms.assetid: 12069912-4b87-4945-9123-51106e0d2d54
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 50b49761cf5923b11a450cbce7b7991f5ddd4d82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418218"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="36d4a-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="36d4a-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="36d4a-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="36d4a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="36d4a-105">Fragt den MAPI-Anbieter nach Unterstützung für schnelles Herunterfahren ab.</span><span class="sxs-lookup"><span data-stu-id="36d4a-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="36d4a-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="36d4a-106">Return value</span></span>

<span data-ttu-id="36d4a-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="36d4a-107">S_OK</span></span>
  
> <span data-ttu-id="36d4a-108">Der MAPI-Anbieter unterstützt den MAPI-Client zum schnellen Herunterfahren.</span><span class="sxs-lookup"><span data-stu-id="36d4a-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="36d4a-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="36d4a-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="36d4a-110">Der MAPI-Anbieter unterstützt den MAPI-Client nicht, um schnelles Herunterfahren zu tun.</span><span class="sxs-lookup"><span data-stu-id="36d4a-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="36d4a-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="36d4a-111">Remarks</span></span>

<span data-ttu-id="36d4a-112">MAPI-Anbieter, die das schnelle Herunterfahren des Clients nicht unterstützen müssen, sollten weiterhin die [IMAPIProviderShutdown-Schnittstelle](imapiprovidershutdowniunknown.md) implementieren und die **IMAPIProviderShutdown::QueryFastShutdown-Methode** MAPI_E_NO_SUPPORT.</span><span class="sxs-lookup"><span data-stu-id="36d4a-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="36d4a-113">Für Outlook als MAPI-Client führt dies dazu, dass Outlook warten, bis alle externen Verweise freigegeben werden, bevor sie beendet werden.</span><span class="sxs-lookup"><span data-stu-id="36d4a-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="36d4a-114">Abhängig von der Registrierungseinstellung Windows Benutzer für schnelles Herunterfahren verhindert das Nicht implementieren der **IMAPIProviderShutdown-Schnittstelle** nicht unbedingt das schnelle Herunterfahren eines Clients.</span><span class="sxs-lookup"><span data-stu-id="36d4a-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="36d4a-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="36d4a-115">See also</span></span>



[<span data-ttu-id="36d4a-116">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="36d4a-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="36d4a-117">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="36d4a-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

