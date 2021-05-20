---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Fügt die person hinzu, die durch die Parameter emailAddresses und displayName als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33429831"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="49901-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="49901-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="49901-104">Fügt die person hinzu, die durch die  _Parameter emailAddresses_ und  _displayName_ als Freund für den angemeldeten Benutzer im sozialen Netzwerk identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="49901-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="49901-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="49901-105">Parameters</span></span>

<span data-ttu-id="49901-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="49901-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="49901-107">[in] Ein Array, das eine oder mehrere gültige SMTP-Adressen für eine Person im sozialen Netzwerk enthält.</span><span class="sxs-lookup"><span data-stu-id="49901-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="49901-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="49901-108">_displayName_</span></span>
  
> <span data-ttu-id="49901-109">[in] Eine Zeichenfolge, die den Anzeigenamen der Person enthält, die als Freund hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="49901-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="49901-110">Hinweise</span><span class="sxs-lookup"><span data-stu-id="49901-110">Remarks</span></span>

<span data-ttu-id="49901-111">Wenn der Outlook Social Connector (OSC) mehr als die SMTP-Adresse im Array im **parameter emailAddresses** enthält, kann der OSC-Anbieter davon ausgehen, dass das erste Element die primäre SMTP-Adresse ist.</span><span class="sxs-lookup"><span data-stu-id="49901-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="49901-112">Wenn der Anbieter das **followPerson-Element**  im Funktionen-XML als **true** festgelegt hat und keines der Elemente für _emailAddresses_ einem Benutzer im Netzwerk zutrifft, muss der Anbieter den Fehler OSC_E_NOT_FOUND zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="49901-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="49901-113">Wenn der Anbieter **followPerson** in den Funktionen als **false** festgelegt **hat,** sollte der OSC_E_FAIL zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="49901-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="49901-114">Wenn die **FollowPersonEx-Methode** erfolgreich ist, kann der Anbieter die Zeichenfolge im  _displayName-Parameter_ verwenden, um die Person in jeder nachfolgenden E-Mail zur Freundesbestätigung anstatt die Person über die SMTP-Adresse zu adressieren.</span><span class="sxs-lookup"><span data-stu-id="49901-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="49901-115">Andererseits muss der Anbieter in der Lage sein, das OSC zu verarbeiten, das eine leere Zeichenfolge für den _parameter displayName übergeben._</span><span class="sxs-lookup"><span data-stu-id="49901-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="49901-116">Wenn der Anbieter die [ISocialSession2-Schnittstelle](isocialsession2iunknown.md) implementiert und **followPerson** im Funktionen-XML als **true** festgelegt hat, ruft das OSC **FollowPersonEx** anstelle von [ISocialSession::FollowPerson auf.](isocialsession-followperson.md)</span><span class="sxs-lookup"><span data-stu-id="49901-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="49901-117">Wenn der Anbieter **followPerson** als **true** festgelegt hat, aber die **ISocialSession2-Schnittstelle** nicht implementiert, oder **FollowPersonEx** den OSC_E_NOTIMPL-Fehler zurückgibt, ruft das OSC **ISocialSession::FollowPerson auf.**</span><span class="sxs-lookup"><span data-stu-id="49901-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="49901-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="49901-118">See also</span></span>

- [<span data-ttu-id="49901-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="49901-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

