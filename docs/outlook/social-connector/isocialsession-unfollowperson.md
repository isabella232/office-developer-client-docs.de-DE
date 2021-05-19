---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Entfernt die person, die durch den parameter userID als Freund im sozialen Netzwerk identifiziert wird.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418435"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="6a1bf-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="6a1bf-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="6a1bf-104">Entfernt die person, die durch den  _parameter userID_ als Freund im sozialen Netzwerk identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="6a1bf-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="6a1bf-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="6a1bf-105">Parameters</span></span>

<span data-ttu-id="6a1bf-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="6a1bf-106">_userID_</span></span>
  
> <span data-ttu-id="6a1bf-107">[in] Eine Zeichenfolge, die eine Benutzer-ID des sozialen Netzwerks für eine Person enthält.</span><span class="sxs-lookup"><span data-stu-id="6a1bf-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6a1bf-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6a1bf-108">Remarks</span></span>

<span data-ttu-id="6a1bf-109">Der  _parameter userID_ muss eine gültige Benutzer-ID für die Person im sozialen Netzwerk sein.</span><span class="sxs-lookup"><span data-stu-id="6a1bf-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="6a1bf-110">Wenn der Outlook Social Connector (OSC)-Anbieter **doNotFollowPerson** in der XML für Funktionen als **true** festgelegt **hat,** muss der Anbieter den OSC_E_NOT_FOUND-Fehler zurückgeben, wenn die übergebene Benutzer-ID keinem Benutzer im Netzwerk zutrifft.</span><span class="sxs-lookup"><span data-stu-id="6a1bf-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="6a1bf-111">Wenn der Anbieter **doNotFollowPerson** **in** funktionen als **false** festgelegt hat, sollte der Anbieter den Fehler OSC_E_FAIL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="6a1bf-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="6a1bf-112">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="6a1bf-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="6a1bf-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6a1bf-113">See also</span></span>

- [<span data-ttu-id="6a1bf-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6a1bf-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

