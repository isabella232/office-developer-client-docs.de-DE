---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.
ms.openlocfilehash: f755476f66ab2f91471b88c74baff899f31b83e3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407655"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="aba21-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="aba21-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="aba21-104">Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.</span><span class="sxs-lookup"><span data-stu-id="aba21-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="aba21-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="aba21-105">Parameters</span></span>

<span data-ttu-id="aba21-106">_personencollection_</span><span class="sxs-lookup"><span data-stu-id="aba21-106">_personsCollection_</span></span>
  
> <span data-ttu-id="aba21-107">Out Eine XML-Zeichenfolge, die eine Gruppe von Freunden der Person darstellt und der Definition der **Freunde** entspricht, die in der Erweiterbarkeit des XML-Schemas für Outlook Social Connector (OSC)-Anbieter definiert sind.</span><span class="sxs-lookup"><span data-stu-id="aba21-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="aba21-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aba21-108">Remarks</span></span>

<span data-ttu-id="aba21-109">OSC ruft **GetFriendsAndColleagues** auf, wenn der osc-Anbieter die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt.</span><span class="sxs-lookup"><span data-stu-id="aba21-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="aba21-110">Wenn der OSC anfänglich die **GetFriendsAndColleagues** -Methode für den Outlook-Benutzer aufruft, der am sozialen Netzwerk angemeldet ist, gibt **GETFRIENDSANDCOLLEAGUES** eine XML-Zeichenfolge zurück, die Freunde des angemeldeten Benutzers im sozialen Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="aba21-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="aba21-111">Die XML-Zeichenfolge entspricht der XML-Schema Definition von **friends** und gibt ein **Person** -Element (das auch der osc-Anbieter Schema Definition entspricht) für jeden Freund an.</span><span class="sxs-lookup"><span data-stu-id="aba21-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="aba21-112">Wenn **GetFriendsAndColleagues** die Freundes Informationen für den angemeldeten Benutzer zurückgibt, speichert der osc diese Informationen in einem Ordner Kontakte.</span><span class="sxs-lookup"><span data-stu-id="aba21-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="aba21-113">Dieser Ordner ist spezifisch für das soziale Netzwerk und befindet sich im standardmäßigen Outlook-Speicher des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="aba21-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="aba21-114">Weitere Informationen dazu, wie der OSC Freundes Informationen in einem Ordner Kontakte speichert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="aba21-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="aba21-115">Die Informationen zu jedem im Parameter persons zurückgegebenen Friend entsprechen der XML-Schema Definition für **Person**. __</span><span class="sxs-lookup"><span data-stu-id="aba21-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="aba21-116">Das **Person** -Element unterstützt viele Informationen für jeden Freund, einschließlich der SMTP-e-Mail-Adressen ( \*\*\*\* die den Elementen "Email Address", " **emailAddress2**" und " **emailAddress3** " zugeordnet sind), die der Freund im Soziales Netzwerk und die Benutzer-ID (die dem **UserID** -Element zugeordnet wird), die diesen Freund im sozialen Netzwerk identifiziert.</span><span class="sxs-lookup"><span data-stu-id="aba21-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="aba21-117">Um Aktivitäten für einen Outlook-Benutzer anzuzeigen, der im Personen Bereich ausgewählt ist, versucht der OSC, den Benutzer mit jedem von **GetFriendsAndColleagues**zurückgegebenen Freund zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="aba21-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="aba21-118">OSC verwendet hierzu die SMTP-Adresse des ausgewählten Outlook-Benutzers mit den e-Mail-Adressen, die jeder Freund im sozialen Netzwerk angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="aba21-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="aba21-119">Wenn OSC eine entsprechende SMTP-e-Mail-Adresse findet, verwendet der OSC die entsprechende **UserID** des Freundes, um die [ISocialSession:: GetPerson](isocialsession-getperson.md) -Methode aufzurufen.</span><span class="sxs-lookup"><span data-stu-id="aba21-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="aba21-120">Dies dient dazu, ein [ISocialPerson](isocialpersoniunknown.md) -Objekt für diesen Freund abzurufen, das dem osc dann ermöglicht, Aktivitäten und Bilder dieses Freundes aus dem sozialen Netzwerk abzurufen.</span><span class="sxs-lookup"><span data-stu-id="aba21-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="aba21-121">Wenn der ausgewählte Outlook-Benutzer jedoch nicht dieselbe SMTP-Adresse für ein Konto im sozialen Netzwerk angibt oder wenn der Outlook-Benutzer kein Konto in diesem sozialen Netzwerk hat, kann der OSC keine Übereinstimmung für diesen Benutzer finden und zeigt keine Aktivitäten an. es für diesen Benutzer im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="aba21-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="aba21-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aba21-122">See also</span></span>

- [<span data-ttu-id="aba21-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="aba21-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="aba21-124">Informationen zu Freunden erhalten</span><span class="sxs-lookup"><span data-stu-id="aba21-124">Getting Friends Information</span></span>](getting-friends-information.md)

