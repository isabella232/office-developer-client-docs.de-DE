---
title: ISocialSessionGetPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2d0a2945-54d7-417f-b5c6-2647c70263cf
description: Ruft eine ISocialPerson-Schnittstelle basierend auf dem UserID-Parameter.
ms.openlocfilehash: 5769f4c41bb97f45ab722f1b3a3febe24c8a7ab2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795985"
---
# <a name="isocialsessiongetperson"></a><span data-ttu-id="3e423-103">ISocialSession::GetPerson</span><span class="sxs-lookup"><span data-stu-id="3e423-103">ISocialSession::GetPerson</span></span>

<span data-ttu-id="3e423-104">Ruft eine [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle basierend auf dem _UserID_ -Parameter.</span><span class="sxs-lookup"><span data-stu-id="3e423-104">Gets an [ISocialPerson](isocialpersoniunknown.md) interface based on the  _userID_ parameter.</span></span> 
  
```cpp
HRESULT _stdcall GetPerson([in] BSTR userId, [out, retval] ISocialPerson** result);
```

## <a name="parameters"></a><span data-ttu-id="3e423-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="3e423-105">Parameters</span></span>

<span data-ttu-id="3e423-106">_userId_</span><span class="sxs-lookup"><span data-stu-id="3e423-106">_userId_</span></span>
  
> <span data-ttu-id="3e423-107">[in] Eine Zeichenfolge, die eine Benutzer-ID oder SMTP-Adresse einer Person enthält.</span><span class="sxs-lookup"><span data-stu-id="3e423-107">[in] A string that contains a user ID or SMTP address of a person.</span></span>
    
<span data-ttu-id="3e423-108">_Ergebnis_</span><span class="sxs-lookup"><span data-stu-id="3e423-108">_result_</span></span>
  
> <span data-ttu-id="3e423-109">[out] Eine **ISocialPerson** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="3e423-109">[out] An **ISocialPerson** interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="3e423-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3e423-110">Remarks</span></span>

<span data-ttu-id="3e423-111">Der _Benutzer-ID_ -Parameter muss eine Benutzer-ID oder SMTP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="3e423-111">The  _userID_ parameter must be a user ID or SMTP address.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3e423-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e423-112">See also</span></span>

- [<span data-ttu-id="3e423-113">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3e423-113">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

