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
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: d9f08c13f68c7d3d9f41b9a67ac1888d6c507c34
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19792324"
---
# <a name="imapiprovidershutdownqueryfastshutdown"></a><span data-ttu-id="6e3e0-103">IMAPIProviderShutdown::QueryFastShutdown</span><span class="sxs-lookup"><span data-stu-id="6e3e0-103">IMAPIProviderShutdown::QueryFastShutdown</span></span>

  
  
<span data-ttu-id="6e3e0-104">**Betrifft**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6e3e0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6e3e0-105">Abfragen der MAPI-Anbieter für Schnelles Herunterfahren unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6e3e0-105">Queries the MAPI provider for fast shutdown support.</span></span> 
  
```cpp
HRESULT QueryFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="6e3e0-106">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="6e3e0-106">Return value</span></span>

<span data-ttu-id="6e3e0-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="6e3e0-107">S_OK</span></span>
  
> <span data-ttu-id="6e3e0-108">Der MAPI-Anbieter unterstützt den MAPI-Client zum Herunterfahren schnelle.</span><span class="sxs-lookup"><span data-stu-id="6e3e0-108">The MAPI provider supports the MAPI client to do fast shutdown.</span></span>
    
<span data-ttu-id="6e3e0-109">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="6e3e0-109">MAPI_E_NO_SUPPORT</span></span>
  
> <span data-ttu-id="6e3e0-110">MAPI-Anbieter unterstützt keine den MAPI-Client zum Herunterfahren schnelle.</span><span class="sxs-lookup"><span data-stu-id="6e3e0-110">The MAPI provider does not support the MAPI client to do fast shutdown.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6e3e0-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e3e0-111">Remarks</span></span>

<span data-ttu-id="6e3e0-112">MAPI-Anbieter, die keine schnelle Herunterfahren von Clients unterstützen müssen sollten weiterhin die [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) -Schnittstelle implementieren, und haben die **IMAPIProviderShutdown::QueryFastShutdown** -Methode MAPI_E_NO_SUPPORT zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6e3e0-112">MAPI providers that do not need to support client fast shutdown should still implement the [IMAPIProviderShutdown](imapiprovidershutdowniunknown.md) interface, and have the **IMAPIProviderShutdown::QueryFastShutdown** method return MAPI_E_NO_SUPPORT.</span></span> <span data-ttu-id="6e3e0-113">Für Outlook als MAPI-Client bewirkt, dass dieser Outlook warten, dass alle externen Verweise freigegeben werden muss, bevor sie beendet wird.</span><span class="sxs-lookup"><span data-stu-id="6e3e0-113">For Outlook as a MAPI client, this causes Outlook to wait for all external references to be released before it exits.</span></span> 
  
<span data-ttu-id="6e3e0-114">Je nach Windows-Registrierung des Benutzers verhindert Einstellung für das schnelle Herunterfahren nicht implementieren der **IMAPIProviderShutdown** -Schnittstelle nicht unbedingt ein schnelle Herunterfahren von Clients.</span><span class="sxs-lookup"><span data-stu-id="6e3e0-114">Depending on the user's Windows registry setting for fast shutdown, not implementing the **IMAPIProviderShutdown** interface does not necessarily prevent a client fast shutdown.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6e3e0-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6e3e0-115">See also</span></span>



[<span data-ttu-id="6e3e0-116">IMAPIProviderShutdown: IUnknown</span><span class="sxs-lookup"><span data-stu-id="6e3e0-116">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="6e3e0-117">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="6e3e0-117">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

