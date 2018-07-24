---
title: ISocialProviderGetAutoConfiguredSession
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8d41ced-c2bb-482e-b0bc-1b46c82121bd
description: Ruft eine automatisch konfigurierte ISocialSession-Schnittstelle ab.
ms.openlocfilehash: 7108a7e42e9b54e069d8d420283c1ebad3367830
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795997"
---
# <a name="isocialprovidergetautoconfiguredsession"></a><span data-ttu-id="e532b-103">ISocialProvider::GetAutoConfiguredSession</span><span class="sxs-lookup"><span data-stu-id="e532b-103">ISocialProvider::GetAutoConfiguredSession</span></span>

<span data-ttu-id="e532b-104">Ruft eine automatisch konfigurierte [ISocialSession](isocialsessioniunknown.md)-Schnittstelle ab.</span><span class="sxs-lookup"><span data-stu-id="e532b-104">Gets an automatically configured [ISocialSession](isocialsessioniunknown.md) interface.</span></span> 
  
```cpp
HRESULT _stdcall GetAutoConfiguredSession([out, retval] ISocialSession** session);
```

## <a name="parameters"></a><span data-ttu-id="e532b-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="e532b-105">Parameters</span></span>

<span data-ttu-id="e532b-106">_session_</span><span class="sxs-lookup"><span data-stu-id="e532b-106">_Session_</span></span>
  
> <span data-ttu-id="e532b-107">[out] Eine **ISocialSession**-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="e532b-107">[out] An **ISocialSession** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="e532b-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e532b-108">Remarks</span></span>

<span data-ttu-id="e532b-109">Die zurückgegebene **ISocialSession**-Schnittstelle wird basierend auf einer anbieterspezifischen Methode automatisch am Netzwerk angemeldet.</span><span class="sxs-lookup"><span data-stu-id="e532b-109">The returned **ISocialSession** interface is automatically logged on to the network, based on a method that is specific to the provider.</span></span> 
  
<span data-ttu-id="e532b-110">Der Anbieter sollte den Fehler OSC_E_NOT_IMPLEMENTED zurückgeben, wenn das soziale Netzwerk die automatische Konfiguration nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e532b-110">The provider should return the OSC_E_NOT_IMPLEMENTED error if the social network does not support automatic configuration.</span></span> <span data-ttu-id="e532b-111">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="e532b-111">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e532b-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e532b-112">See also</span></span>

- [<span data-ttu-id="e532b-113">ISocialProvider : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e532b-113">ISocialProvider : IUnknown</span></span>](isocialprovideriunknown.md)

