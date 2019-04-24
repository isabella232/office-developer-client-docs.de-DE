---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Entfernt die Person, die durch den Parameter userID als Freund im sozialen Netzwerk identifiziert wird.
ms.openlocfilehash: c276a9e5af18f7e4a3afbaa66d366d55de460a58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336778"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="a3073-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="a3073-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="a3073-104">Entfernt die Person, die durch den Parameter _UserID_ als Freund im sozialen Netzwerk identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="a3073-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="a3073-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a3073-105">Parameters</span></span>

<span data-ttu-id="a3073-106">_userID_</span><span class="sxs-lookup"><span data-stu-id="a3073-106">_userID_</span></span>
  
> <span data-ttu-id="a3073-107">in Eine Zeichenfolge, die eine soziale Netzwerk-Benutzer-ID für eine Person enthält.</span><span class="sxs-lookup"><span data-stu-id="a3073-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="a3073-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a3073-108">Remarks</span></span>

<span data-ttu-id="a3073-109">Der Parameter " _UserID_ " muss eine gültige Benutzer-ID für die Person im sozialen Netzwerk sein.</span><span class="sxs-lookup"><span data-stu-id="a3073-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="a3073-110">Wenn der Outlook Social Connector-Anbieter (OSC) **doNotFollowPerson** als **true** im XML for **Capabilities**festgelegt hat, muss der Anbieter den OSC_E_NOT_FOUND-Fehler zurückgeben, falls die Benutzer-ID, die übergeben wird, keinem Benutzer im Netzwerk entspricht.</span><span class="sxs-lookup"><span data-stu-id="a3073-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="a3073-111">Wenn der Anbieter **doNotFollowPerson** als **false** in- **Funktionen**festgelegt hat, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="a3073-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="a3073-112">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="a3073-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a3073-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a3073-113">See also</span></span>

- [<span data-ttu-id="a3073-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a3073-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

