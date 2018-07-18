---
title: ISocialSessionFollowPerson
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de7f56e2-c131-4955-b945-0a72043e0f5a
description: Fügt die Person, die durch den Parameter EmailAddress als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.
ms.openlocfilehash: 6dc289801c99f2f3bf1647e9c98c072d2f53d066
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795987"
---
# <a name="isocialsessionfollowperson"></a><span data-ttu-id="23bfa-103">ISocialSession::FollowPerson</span><span class="sxs-lookup"><span data-stu-id="23bfa-103">ISocialSession::FollowPerson</span></span>

<span data-ttu-id="23bfa-104">Fügt die Person, die durch den Parameter _EmailAddress_ als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.</span><span class="sxs-lookup"><span data-stu-id="23bfa-104">Adds the person identified by the  _emailAddress_ parameter as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPerson([in] BSTR emailAddress);
```

## <a name="parameters"></a><span data-ttu-id="23bfa-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="23bfa-105">Parameters</span></span>

<span data-ttu-id="23bfa-106">_emailAddress_</span><span class="sxs-lookup"><span data-stu-id="23bfa-106">_emailAddress_</span></span>
  
> <span data-ttu-id="23bfa-107">[in] Eine Zeichenfolge, die eine e-Mail-Adresse einer Person enthält.</span><span class="sxs-lookup"><span data-stu-id="23bfa-107">[in] A string that contains an email address of a person.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="23bfa-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23bfa-108">Remarks</span></span>

<span data-ttu-id="23bfa-109">Der Parameter _EmailAddress_ muss eine gültige SMTP-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="23bfa-109">The  _emailAddress_ parameter must be a valid SMTP address.</span></span> <span data-ttu-id="23bfa-110">Wenn der Anbieter Outlook Social Connector (OSC) die **FollowPerson** -Methode als **true** , in **Funktionen festgelegt hat**und das Argument für _EmailAddress_ keinen Benutzer im Netzwerk überein stimmt, muss der Anbieter die OSC_E_NOT_FOUND zurück. Fehler.</span><span class="sxs-lookup"><span data-stu-id="23bfa-110">If the Outlook Social Connector (OSC) provider has set the **followPerson** method as **true** in **capabilities**, and the argument for  _emailAddress_ does not match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="23bfa-111">Wenn der Anbieter **FollowPerson** als **false** in **Funktionen**festgelegt ist, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="23bfa-111">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span>
  
<span data-ttu-id="23bfa-112">Wenn der Anbieter die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementiert und hat **FollowPerson** in **Funktionen**als **true** festgelegt, wird die OSC [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) anstelle von **ISocialSession::FollowPerson aufrufen. **.</span><span class="sxs-lookup"><span data-stu-id="23bfa-112">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in **capabilities**, the OSC will call [ISocialSession2::FollowPersonEx](isocialsession2-followpersonex.md) instead of **ISocialSession::FollowPerson**.</span></span> <span data-ttu-id="23bfa-113">Wenn der Anbieter nicht die **ISocialSession2** -Schnittstelle implementiert oder **ISocialSession2::FollowPersonEx** wird der OSC_E_NOTIMPL Fehler zurückgegeben, wird die OSC **ISocialSession::FollowPerson** aufrufen, solange der Anbieter **festgelegt hat FollowPerson** als **true** **Funktionen**.</span><span class="sxs-lookup"><span data-stu-id="23bfa-113">If the provider does not implement the **ISocialSession2** interface, or **ISocialSession2::FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC will call **ISocialSession::FollowPerson** as long as the provider has set **followPerson** as **true** in **capabilities**.</span></span> <span data-ttu-id="23bfa-114">Informationen zu Fehlercodes finden Sie unter [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span><span class="sxs-lookup"><span data-stu-id="23bfa-114">For information about error codes, see [Outlook Social Connector Provider Error Codes](outlook-social-connector-provider-error-codes.md).</span></span>
  
<span data-ttu-id="23bfa-115">Bei der Entscheidung, ob **ISocalSession::FollowPerson** oder **ISocialSession2::FollowPersonEx**zu implementieren, Sie berücksichtigen sollten, ob der Anbieter die andere Methoden in **ISocialSession2**benötigt, und ob können Sie die _verwenden. DjsplayName_ -Parameter im **FollowPersonEx**.</span><span class="sxs-lookup"><span data-stu-id="23bfa-115">In deciding whether to implement **ISocalSession::FollowPerson** or **ISocialSession2::FollowPersonEx**, you should consider whether your provider needs the other methods in **ISocialSession2**, and whether you can use the  _djsplayName_ parameter in **FollowPersonEx**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="23bfa-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23bfa-116">See also</span></span>

- [<span data-ttu-id="23bfa-117">ISocialSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="23bfa-117">ISocialSession : IUnknown</span></span>](isocialsessioniunknown.md)

