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
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="5417e-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="5417e-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="5417e-104">Ruft eine Zeichenfolge ab, die eine Auflistung von Personen darstellt.</span><span class="sxs-lookup"><span data-stu-id="5417e-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="5417e-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="5417e-105">Parameters</span></span>

<span data-ttu-id="5417e-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="5417e-106">_personsCollection_</span></span>
  
> <span data-ttu-id="5417e-107">[out] Eine XML-Zeichenfolge, die eine Gruppe von Freunden der Person  darstellt und die der Definition von Freunden entspricht, die im XML-Schema für die Erweiterbarkeit des Outlook Social Connector (OSC)-Anbieters definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5417e-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="5417e-108">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5417e-108">Remarks</span></span>

<span data-ttu-id="5417e-109">Das OSC ruft **GetFriendsAndColleagues auf,** wenn der OSC-Anbieter die zwischengespeicherte oder hybride Synchronisierung von Freunden im sozialen Netzwerk unterstützt.</span><span class="sxs-lookup"><span data-stu-id="5417e-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="5417e-110">Wenn das OSC zunächst die **GetFriendsAndColleagues-Methode** für den Outlook-Benutzer aufruft, der beim sozialen Netzwerk angemeldet ist, gibt **GetFriendsAndColleagues** eine XML-Zeichenfolge zurück, die Freunde des angemeldeten Benutzers im sozialen Netzwerk darstellt.</span><span class="sxs-lookup"><span data-stu-id="5417e-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="5417e-111">Die XML-Zeichenfolge entspricht der **Friends-XML-Schemadefinition** und gibt ein Person-Element (das auch der Schemadefinition des OSC-Anbieters entspricht) für jeden Freund an. </span><span class="sxs-lookup"><span data-stu-id="5417e-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="5417e-112">Wenn **GetFriendsAndColleagues die Freundesinformationen** für den angemeldeten Benutzer zurückgibt, speichert das OSC diese Informationen in einem Kontaktordner.</span><span class="sxs-lookup"><span data-stu-id="5417e-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="5417e-113">Dieser Ordner ist spezifisch für das soziale Netzwerk und befindet sich im Standardspeicher des angemeldeten Benutzers Outlook Speicher.</span><span class="sxs-lookup"><span data-stu-id="5417e-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="5417e-114">Weitere Informationen dazu, wie das OSC die Informationen von Freunden in einem Kontaktordner zwischenspeichert, finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="5417e-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="5417e-115">Die Informationen für jeden im  _parameter personsCollection zurückgegebenen_ Freund entsprechen der XML-Schemadefinition für **Person**.</span><span class="sxs-lookup"><span data-stu-id="5417e-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="5417e-116">Das **Person-Element** unterstützt viele Informationen für jeden Freund, einschließlich der SMTP-E-Mail-Adressen (die den **Elementen emailAddress,** **emailAddress2** und **emailAddress3** zugeordnet sind), die der Freund im sozialen Netzwerk angegeben hat, und die Benutzer-ID (die dem **userID-Element** zugeordnet ist), die diesen Freund im sozialen Netzwerk identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5417e-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="5417e-117">Zum Anzeigen von Aktivitäten für Outlook Benutzer, der im Personenbereich ausgewählt ist, versucht das OSC, den Benutzer mit jedem von **GetFriendsAndColleagues** zurückgegebenen Freund zu verfeinern.</span><span class="sxs-lookup"><span data-stu-id="5417e-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="5417e-118">Das OSC führt dies durch Abgleichen der SMTP-Adresse des ausgewählten Outlook-Benutzers mit den E-Mail-Adressen aus, die jeder Freund im sozialen Netzwerk angegeben hat.</span><span class="sxs-lookup"><span data-stu-id="5417e-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="5417e-119">Wenn das OSC eine übereinstimmende SMTP-E-Mail-Adresse findet, verwendet das OSC die entsprechende **userID** des Freundes, um die [ISocialSession::GetPerson-Methode auf](isocialsession-getperson.md) aufruft.</span><span class="sxs-lookup"><span data-stu-id="5417e-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="5417e-120">Dies wird zum Abrufen eines [ISocialPerson-Objekts](isocialpersoniunknown.md) für diesen Freund verwendet, mit dem das OSC dann Aktivitäten und Bilder dieses Freundes aus dem sozialen Netzwerk abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="5417e-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="5417e-121">Wenn der ausgewählte Outlook-Benutzer jedoch nicht dieselbe SMTP-Adresse für ein Konto im sozialen Netzwerk anbeigt, oder wenn der Outlook-Benutzer kein Konto in diesem sozialen Netzwerk hat, kann das OsC keine Übereinstimmung für diesen Benutzer finden und keine Aktivitäten für diesen Benutzer im sozialen Netzwerk anzeigen.</span><span class="sxs-lookup"><span data-stu-id="5417e-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="5417e-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5417e-122">See also</span></span>

- [<span data-ttu-id="5417e-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5417e-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="5417e-124">Abrufen von Informationen zu Freunden</span><span class="sxs-lookup"><span data-stu-id="5417e-124">Getting Friends Information</span></span>](getting-friends-information.md)

