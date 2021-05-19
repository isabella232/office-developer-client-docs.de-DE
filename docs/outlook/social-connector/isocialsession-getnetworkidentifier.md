---
title: ISocialSessionGetNetworkIdentifier
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534e404f-54c6-4d2b-a8d0-d2ee990a972f
description: Ruft eine Zeichenfolge ab, die eine eindeutige ID für soziale Netzwerke für eine bestimmte Verbindung mit sozialen Netzwerken darstellt.
ms.openlocfilehash: 3051abd6dcccec878e8c53332980731772d543eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433276"
---
# <a name="isocialsessiongetnetworkidentifier"></a><span data-ttu-id="d504c-103">ISocialSession::GetNetworkIdentifier</span><span class="sxs-lookup"><span data-stu-id="d504c-103">ISocialSession::GetNetworkIdentifier</span></span>

<span data-ttu-id="d504c-104">Ruft eine Zeichenfolge ab, die eine eindeutige ID für soziale Netzwerke für eine bestimmte Verbindung mit sozialen Netzwerken darstellt.</span><span class="sxs-lookup"><span data-stu-id="d504c-104">Gets a string that represents a unique social network identifier for a given social network connection.</span></span> 
  
```cpp
HRESULT _stdcall GetNetworkIdentifier([out, retval] BSTR* networkIdentifier);
```

## <a name="parameters"></a><span data-ttu-id="d504c-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="d504c-105">Parameters</span></span>

<span data-ttu-id="d504c-106">_networkIdentifier_</span><span class="sxs-lookup"><span data-stu-id="d504c-106">_networkIdentifier_</span></span>
  
> <span data-ttu-id="d504c-107">[out] Eine Zeichenfolge, die einen eindeutigen Bezeichner für soziale Netzwerke enthält.</span><span class="sxs-lookup"><span data-stu-id="d504c-107">[out] A string that contains a unique social network identifier.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d504c-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d504c-108">Remarks</span></span>

<span data-ttu-id="d504c-109">Ein eindeutiger Netzwerkbezeichner ist eine Zeichenfolge, die das soziale Netzwerk Outlook Social Connector (OSC) identifiziert.</span><span class="sxs-lookup"><span data-stu-id="d504c-109">A unique network identifier is a string that identifies the Outlook Social Connector (OSC) provider social network.</span></span> <span data-ttu-id="d504c-110">Diese Methode kann auch E_NOTIMPL.</span><span class="sxs-lookup"><span data-stu-id="d504c-110">This method can also return E_NOTIMPL.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d504c-111">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d504c-111">See also</span></span>

- [<span data-ttu-id="d504c-112">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d504c-112">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

