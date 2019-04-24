---
title: IMAPIProviderShutdownDoFastShutdown
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIProviderShutdown.DoFastShutdown
api_type:
- COM
ms.assetid: d2b66a8e-2e28-4c32-af95-38d345c7bbd7
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4ff93ed9353d58ef6b68823bebf8b5b27a0df6e8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322421"
---
# <a name="imapiprovidershutdowndofastshutdown"></a><span data-ttu-id="62aff-103">IMAPIProviderShutdown::DoFastShutdown</span><span class="sxs-lookup"><span data-stu-id="62aff-103">IMAPIProviderShutdown::DoFastShutdown</span></span>

  
  
<span data-ttu-id="62aff-104">**Gilt für**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="62aff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="62aff-105">Gibt dem MAPI-Anbieter an, dass der MAPI-Client sofort beendet wird, sodass der MAPI-Anbieter Änderungen anhält, um Datenverluste zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="62aff-105">Indicates to the MAPI provider that the MAPI client is exiting immediately, so that the MAPI provider will persist changes to prevent data loss.</span></span>
  
```cpp
HRESULT DoFastShutdown ();
```

## <a name="return-value"></a><span data-ttu-id="62aff-106">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="62aff-106">Return value</span></span>

<span data-ttu-id="62aff-107">S_OK</span><span class="sxs-lookup"><span data-stu-id="62aff-107">S_OK</span></span>
  
> <span data-ttu-id="62aff-108">Der MAPI-Anbieter kann sofort mit dem MAPI-Client beendet werden.</span><span class="sxs-lookup"><span data-stu-id="62aff-108">The MAPI provider is ready for the MAPI client to exit immediately.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="62aff-109">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="62aff-109">See also</span></span>



[<span data-ttu-id="62aff-110">IMAPIProviderShutdown : IUnknown</span><span class="sxs-lookup"><span data-stu-id="62aff-110">IMAPIProviderShutdown : IUnknown</span></span>](imapiprovidershutdowniunknown.md)


[<span data-ttu-id="62aff-111">Herunterfahren von Clients in MAPI</span><span class="sxs-lookup"><span data-stu-id="62aff-111">Client Shutdown in MAPI</span></span>](client-shutdown-in-mapi.md)

