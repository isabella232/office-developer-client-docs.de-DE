---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Ruft eine ISocialPerson-Schnittstelle basierend auf dem userID-Parameter ab.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439821"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="26bc7-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="26bc7-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="26bc7-104">Ruft eine [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) basierend auf dem  _userID-Parameter_ ab.</span><span class="sxs-lookup"><span data-stu-id="26bc7-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="26bc7-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="26bc7-105">Parameters</span></span>

<span data-ttu-id="26bc7-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="26bc7-106">_userId_</span></span>
  
> <span data-ttu-id="26bc7-107">[in] Eine Zeichenfolge, die eine Benutzer-ID oder SMTP-Adresse einer Person enthält.</span><span class="sxs-lookup"><span data-stu-id="26bc7-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="26bc7-108">_result_</span><span class="sxs-lookup"><span data-stu-id="26bc7-108">_result_</span></span>
  
> <span data-ttu-id="26bc7-109">[out] Eine **ISocialPerson-Schnittstelle.**</span><span class="sxs-lookup"><span data-stu-id="26bc7-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="26bc7-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="26bc7-110">Remarks</span></span>

<span data-ttu-id="26bc7-111">Der  _parameter userID_ muss eine Benutzer-ID oder EINE SMTP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="26bc7-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="26bc7-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="26bc7-112">See also</span></span>

- [<span data-ttu-id="26bc7-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="26bc7-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

