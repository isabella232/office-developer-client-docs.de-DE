---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Ruft eine Zeichenfolge, die einen eindeutigen für soziale Netzwerkbezeichner für eine bestimmte sozialen Netzwerkverbindung darstellt.
ms.openlocfilehash: eb618ba8e8bb37278c1fdb09d984fba141a9d686
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796109"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="ef48c-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="ef48c-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="ef48c-104">Ruft eine Zeichenfolge, die einen eindeutigen für soziale Netzwerkbezeichner für eine bestimmte sozialen Netzwerkverbindung darstellt.</span><span class="sxs-lookup"><span data-stu-id="ef48c-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="ef48c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ef48c-105">Parameters</span></span>

<span data-ttu-id="ef48c-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="ef48c-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="ef48c-107">[out] Eine Zeichenfolge, die einen eindeutige für soziale Netzwerkbezeichner enthält.</span><span class="sxs-lookup"><span data-stu-id="ef48c-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ef48c-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ef48c-108">Remarks</span></span>

<span data-ttu-id="ef48c-109">Eine eindeutige ID ist eine Zeichenfolge, die Outlook Social Connector (OSC) Anbieter für soziale Netzwerke identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ef48c-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="ef48c-110">Diese Methode kann auch E_NOTIMPL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="ef48c-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ef48c-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ef48c-111">See also</span></span>

- [<span data-ttu-id="ef48c-112">ISocialSession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="ef48c-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

