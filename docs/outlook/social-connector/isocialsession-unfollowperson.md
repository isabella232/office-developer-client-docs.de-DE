---
title: ISocialSessionUnFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 66c83041-ee83-41d5-b9dc-a4dc4c670f82
description: Entfernt die Person, die durch den Benutzer-ID-Parameter als einen Freund im sozialen Netzwerk identifiziert.
ms.openlocfilehash: 8b9a1e4f903e4bc805481b8679481103ea1ec82c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795996"
---
# <a name="isocialsessionunfollowperson"></a><span data-ttu-id="8fa5a-103">ISocialSession::UnFollowPerson</span><span class="sxs-lookup"><span data-stu-id="8fa5a-103">ISocialSession::UnFollowPerson</span></span>

<span data-ttu-id="8fa5a-104">Entfernt die Person, die durch den _Benutzer-ID_ -Parameter als einen Freund im sozialen Netzwerk identifiziert.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-104">Removes the person identified by the  _userID_ parameter as a friend on the social network.</span></span> 
  
```cpp
HRESULT _stdcall UnFollowPerson([in] BSTR userID);
```

## <a name="parameters"></a><span data-ttu-id="8fa5a-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="8fa5a-105">Parameters</span></span>

<span data-ttu-id="8fa5a-106">_Benutzer-ID_</span><span class="sxs-lookup"><span data-stu-id="8fa5a-106">_userID_</span></span>
  
> <span data-ttu-id="8fa5a-107">[in] Eine Zeichenfolge, die eine Benutzer-ID für soziale Netzwerke für eine Person enthält.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-107">[in] A string that contains a social network user ID for a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8fa5a-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8fa5a-108">Remarks</span></span>

<span data-ttu-id="8fa5a-109">_UserID_ -Parameter muss eine gültige Benutzer-ID für die Person im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-109">The  _userID_ parameter must be a valid user ID for the person on the social network.</span></span> 
  
<span data-ttu-id="8fa5a-110">Wenn der Anbieter Outlook Social Connector (OSC) **DoNotFollowPerson** als **true** in den XML-Code für **Funktionen**eingerichtet hat, muss der Anbieter den OSC_E_NOT_FOUND Fehler im Fall zurück, dass der Benutzer, dem Übergeben von ID in ein Benutzer im Netzwerk nicht übereinstimmt.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-110">If the Outlook Social Connector (OSC) provider has set **doNotFollowPerson** as **true** in the XML for **capabilities**, the provider must return the OSC_E_NOT_FOUND error in the case that the user ID passed in does not match a user on the network.</span></span> <span data-ttu-id="8fa5a-111">Wenn der Anbieter **DoNotFollowPerson** als **false** in **Funktionen**festgelegt ist, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="8fa5a-111">If the provider has set **doNotFollowPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> <span data-ttu-id="8fa5a-112">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="8fa5a-112">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8fa5a-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8fa5a-113">See also</span></span>

- [<span data-ttu-id="8fa5a-114">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8fa5a-114">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

