---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Fügt die Person, die vom Parameter "Email" als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird, hinzu.
ms.openlocfilehash: 849085bd40788039a96ac159fd76a5e252395916
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285364"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="77355-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="77355-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="77355-104">Fügt die Person, die vom Parameter " _Email_ " als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird, hinzu.</span><span class="sxs-lookup"><span data-stu-id="77355-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="77355-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="77355-105">Parameters</span></span>

<span data-ttu-id="77355-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="77355-106">_emailAddress_</span></span>
  
> <span data-ttu-id="77355-107">in Eine Zeichenfolge, die eine e-Mail-Adresse einer Person enthält.</span><span class="sxs-lookup"><span data-stu-id="77355-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="77355-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="77355-108">Remarks</span></span>

<span data-ttu-id="77355-109">Der Parameter " _Email_ Address" muss eine gültige SMTP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="77355-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="77355-110">Wenn der Outlook-Anbieter für soziale Netzwerke (OSC) die **followPerson** -Methode in den **Funktionen**als **true** festgelegt hat und das Argument für die e-mailemail nicht mit einem Benutzer im Netzwerk übereinstimmt, muss der Anbieter die OSC_E_NOT_FOUND zurückgeben. __ Fehler.</span><span class="sxs-lookup"><span data-stu-id="77355-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="77355-111">Wenn der Anbieter **followPerson** als **false** in- **Funktionen**festgelegt hat, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="77355-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="77355-112">Wenn der Anbieter die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementiert und **followPerson** als **true** in- **Funktionen**festgelegt hat, ruft der osc [ISocialSession2:: FollowPersonEx](isocialsession2-followpersonex.md) anstelle von \*\*ISocialSession:: followPerson \*\*.</span><span class="sxs-lookup"><span data-stu-id="77355-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="77355-113">Wenn der Anbieter die **ISocialSession2** -Schnittstelle nicht implementiert oder **ISocialSession2:: FollowPersonEx** den OSC_E_NOTIMPL-Fehler zurückgibt, ruft osc **ISocialSession:: FollowPerson** auf, solange der Anbieter festgelegt **hat followPerson** als **true** in- **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="77355-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="77355-114">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector-Anbieter – Fehlercodes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="77355-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="77355-115">Bei der Entscheidung, ob **ISocalSession:: FollowPerson** oder **ISocialSession2:: FollowPersonEx**implementiert werden soll, sollten Sie berücksichtigen, ob der Anbieter die anderen Methoden in **ISocialSession2**benötigt und ob Sie die _ djsplayName_ -Parameter in **FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="77355-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="77355-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="77355-116">See also</span></span>

- [<span data-ttu-id="77355-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="77355-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

