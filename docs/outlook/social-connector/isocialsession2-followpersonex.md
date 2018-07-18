---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Fügt die Person, die durch die Parameter EmailAddresses und DisplayName als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.
ms.openlocfilehash: 2f4df9afc4c769cce0502792373702c1281fcad7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796005"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="ce1a4-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="ce1a4-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="ce1a4-104">Fügt die Person, die durch die Parameter _EmailAddresses_ und _DisplayName_ als einen Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="ce1a4-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="ce1a4-105">Parameters</span></span>

<span data-ttu-id="ce1a4-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="ce1a4-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="ce1a4-107">[in] Ein Array mit einem oder mehreren gültige SMTP-Adressen für eine Person im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="ce1a4-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="ce1a4-108">_displayName_</span></span>
  
> <span data-ttu-id="ce1a4-109">[in] Eine Zeichenfolge, die den Anzeigenamen der Person, die als Freund hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ce1a4-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ce1a4-110">Remarks</span></span>

<span data-ttu-id="ce1a4-111">Wenn Outlook Social Connector (OSC) bietet mehr als auf kann SMTP-Adresse des Arrays in den Parameter **EmailAddresses** die OSC-Anbieter wird vorausgesetzt, dass das erste Element die primäre SMTP-Adresse ist.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="ce1a4-112">Wenn der Anbieter das **FollowPerson** -Element als **true** , in der **Funktionen** XML festgelegt hat und keine Elemente für _EmailAddresses_ einen Benutzer im Netzwerk übereinstimmt, muss der Anbieter den OSC_E_NOT_FOUND Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="ce1a4-113">Wenn der Anbieter **FollowPerson** als **false** in **Funktionen**festgelegt ist, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="ce1a4-114">Wenn die **FollowPersonEx** -Methode erfolgreich ist, können der Anbieter die Zeichenfolge in der Parameter _DisplayName_ die Person in alle nachfolgenden Friend-e-Mail, statt die SMTP-Adresse die Person adressieren behandeln.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="ce1a4-115">Andererseits, muss der Anbieter die OSC übergeben einer leeren Zeichenfolge für den Parameter _"DisplayName"_ behandeln können.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="ce1a4-116">Wenn der Anbieter die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementiert und **FollowPerson** als **true** in die XML-Funktionen eingerichtet hat, ruft der OSC **FollowPersonEx** anstelle von [ISocialSession::FollowPerson](isocialsession-followperson.md).</span><span class="sxs-lookup"><span data-stu-id="ce1a4-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="ce1a4-117">Wenn der Anbieter **FollowPerson** als **true** festgelegt wurde, aber nicht die **ISocialSession2** -Schnittstelle implementiert oder **FollowPersonEx** wird der OSC_E_NOTIMPL Fehler zurückgegeben, ruft der OSC **ISocialSession::FollowPerson**.</span><span class="sxs-lookup"><span data-stu-id="ce1a4-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="ce1a4-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ce1a4-118">See also</span></span>

- [<span data-ttu-id="ce1a4-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ce1a4-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

