---
title: ISocialSession2FollowPersonEx
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17b4af7f-7967-422b-996c-792705c93ad3
description: Fügt die Person, die von den Parametern "Email" und "displayName" identifiziert wird, als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu.
ms.openlocfilehash: b44b442ba928b48411e5b1fc8a0c8b76477022ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339655"
---
# <a name="isocialsession2followpersonex"></a><span data-ttu-id="b3be5-103">ISocialSession2::FollowPersonEx</span><span class="sxs-lookup"><span data-stu-id="b3be5-103">ISocialSession2::FollowPersonEx</span></span>

<span data-ttu-id="b3be5-104">Fügt die Person, die von den Parametern " _Email_ " und " _DisplayName_ " identifiziert wird, als Freund für den angemeldeten Benutzer im sozialen Netzwerk hinzu.</span><span class="sxs-lookup"><span data-stu-id="b3be5-104">Adds the person identified by the  _emailAddresses_ and  _displayName_ parameters as a friend for the logged-on user on the social network.</span></span> 
  
```cpp
HRESULT _stdcall FollowPersonEx([in] SAFEARRAY(BSTR) emailAddresses, [in] BSTR displayName);
```

## <a name="parameters"></a><span data-ttu-id="b3be5-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="b3be5-105">Parameters</span></span>

<span data-ttu-id="b3be5-106">_emailAddresses_</span><span class="sxs-lookup"><span data-stu-id="b3be5-106">_emailAddresses_</span></span>
  
> <span data-ttu-id="b3be5-107">in Ein Array, das eine oder mehrere gültige SMTP-Adressen für eine Person im sozialen Netzwerk enthält.</span><span class="sxs-lookup"><span data-stu-id="b3be5-107">[in] An array that contains one or multiple valid SMTP addresses for a person on the social network.</span></span>
    
<span data-ttu-id="b3be5-108">_displayName_</span><span class="sxs-lookup"><span data-stu-id="b3be5-108">_displayName_</span></span>
  
> <span data-ttu-id="b3be5-109">in Eine Zeichenfolge, die den Anzeigenamen der Person enthält, die als Friend hinzugefügt werden soll.</span><span class="sxs-lookup"><span data-stu-id="b3be5-109">[in] A string that contains the display name of the person to be added as a friend.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b3be5-110">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b3be5-110">Remarks</span></span>

<span data-ttu-id="b3be5-111">Wenn der Outlook Connector für soziale Netzwerke (OSC) mehr als eine SMTP-Adresse im Array im \*\*\*\* Parameter Emails enthält, kann der osc-Anbieter davon ausgehen, dass das erste Element die primäre SMTP-Adresse ist.</span><span class="sxs-lookup"><span data-stu-id="b3be5-111">If the Outlook Social Connector (OSC) provides more than on SMTP address in the array in the **emailAddresses** parameter, the OSC provider can assume the first element is the primary SMTP address.</span></span> 
  
<span data-ttu-id="b3be5-112">Wenn der Anbieter das **followPerson** -Element im **Capabilities** -XML als **true** festgelegt hat und keines der Elemente für _Email_ -Absender mit einem Benutzer im Netzwerk übereinstimmt, muss der Anbieter den OSC_E_NOT_FOUND-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b3be5-112">If the provider has set the **followPerson** element as **true** in the **capabilities** XML, and none of the elements for  _emailAddresses_ match a user on the network, the provider must return the OSC_E_NOT_FOUND error.</span></span> <span data-ttu-id="b3be5-113">Wenn der Anbieter **followPerson** als **false** in- **Funktionen**festgelegt hat, sollte der Anbieter den OSC_E_FAIL-Fehler zurückgeben.</span><span class="sxs-lookup"><span data-stu-id="b3be5-113">If the provider has set **followPerson** as **false** in **capabilities**, the provider should return the OSC_E_FAIL error.</span></span> 
  
<span data-ttu-id="b3be5-114">Wenn die **FollowPersonEx** -Methode erfolgreich ist, kann der Anbieter die Zeichenfolge im Parameter _DisplayName_ verwenden, um die Person in einer späteren Friend-Bestätigungs-e-Mail zu adressieren, statt die Person anhand der SMTP-Adresse zu adressieren.</span><span class="sxs-lookup"><span data-stu-id="b3be5-114">If the **FollowPersonEx** method succeeds, the provider can use the string in the  _displayName_ parameter to address the person in any subsequent friend-confirmation email, rather than addressing the person by the SMTP address.</span></span> <span data-ttu-id="b3be5-115">Andererseits muss der Anbieter in der Lage sein, den OSC zu behandeln, der eine leere Zeichenfolge für den _DisplayName_ -Parameter übergibt.</span><span class="sxs-lookup"><span data-stu-id="b3be5-115">On the other hand, the provider must be able to handle the OSC passing an empty string for the  _displayName_ parameter.</span></span> 
  
<span data-ttu-id="b3be5-116">Wenn der Anbieter die [ISocialSession2](isocialsession2iunknown.md) -Schnittstelle implementiert und **followPerson** als **true** im Capabilities-XML festgelegt hat, ruft osc **FollowPersonEx** anstelle von [ISocialSession: followPerson](isocialsession-followperson.md)auf.</span><span class="sxs-lookup"><span data-stu-id="b3be5-116">If the provider implements the [ISocialSession2](isocialsession2iunknown.md) interface and has set **followPerson** as **true** in the capabilities XML, the OSC calls **FollowPersonEx** instead of [ISocialSession::FollowPerson](isocialsession-followperson.md).</span></span> <span data-ttu-id="b3be5-117">Wenn der Anbieter **followPerson** als **true** festgelegt, die **ISocialSession2** -Schnittstelle jedoch nicht implementiert oder **FollowPersonEx** den OSC_E_NOTIMPL-Fehler zurückgibt, ruft osc **ISocialSession:: followPerson**auf.</span><span class="sxs-lookup"><span data-stu-id="b3be5-117">If the provider has set **followPerson** as **true** but does not implement the **ISocialSession2** interface, or **FollowPersonEx** returns the OSC_E_NOTIMPL error, the OSC calls **ISocialSession::FollowPerson**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="b3be5-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3be5-118">See also</span></span>

- [<span data-ttu-id="b3be5-119">ISocialSession2 : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b3be5-119">ISocialSession2 : IUnknown</span></span>](isocialsession2iunknown.md)

