---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Ruft eine ISocialPerson-Schnittstelle basierend auf dem Parameter userID ab.
ms.openlocfilehash: b54e39b3712fb57d89d03787f1e5fa0ff50ff84a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439821"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="998cc-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="998cc-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="998cc-104">Ruft eine [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle basierend auf dem Parameter _UserID_ ab.</span><span class="sxs-lookup"><span data-stu-id="998cc-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="998cc-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="998cc-105">Parameters</span></span>

<span data-ttu-id="998cc-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="998cc-106">_userId_</span></span>
  
> <span data-ttu-id="998cc-107">in Eine Zeichenfolge, die eine Benutzer-ID oder eine SMTP-Adresse einer Person enthält.</span><span class="sxs-lookup"><span data-stu-id="998cc-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="998cc-108">_result_</span><span class="sxs-lookup"><span data-stu-id="998cc-108">_result_</span></span>
  
> <span data-ttu-id="998cc-109">Out Eine **ISocialPerson** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="998cc-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="998cc-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="998cc-110">Remarks</span></span>

<span data-ttu-id="998cc-111">Der Parameter _UserID_ muss eine Benutzer-ID oder eine SMTP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="998cc-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="998cc-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="998cc-112">See also</span></span>

- [<span data-ttu-id="998cc-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="998cc-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

