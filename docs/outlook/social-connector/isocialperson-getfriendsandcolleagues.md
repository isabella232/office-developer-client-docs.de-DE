---
title: ISocialPersonGetFriendsAndColleagues
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 62d5b815-f199-499e-85eb-2dff21a8216e
description: Ruft eine Zeichenfolge, die eine Auflistung von Personen darstellt.
ms.openlocfilehash: 36482a6068c592eb0ff07603b6458e8415c3586f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795971"
---
# <a name="isocialpersongetfriendsandcolleagues"></a><span data-ttu-id="a85e8-103">ISocialPerson::GetFriendsAndColleagues</span><span class="sxs-lookup"><span data-stu-id="a85e8-103">ISocialPerson::GetFriendsAndColleagues</span></span>

<span data-ttu-id="a85e8-104">Ruft eine Zeichenfolge, die eine Auflistung von Personen darstellt.</span><span class="sxs-lookup"><span data-stu-id="a85e8-104">Gets a string that represents a collection of people.</span></span>
  
```cpp
HRESULT _stdcall GetFriendsAndColleagues([out, retval] BSTR* personsCollection);
```

## <a name="parameters"></a><span data-ttu-id="a85e8-105">Parameter</span><span class="sxs-lookup"><span data-stu-id="a85e8-105">Parameters</span></span>

<span data-ttu-id="a85e8-106">_personsCollection_</span><span class="sxs-lookup"><span data-stu-id="a85e8-106">_personsCollection_</span></span>
  
> <span data-ttu-id="a85e8-107">[out] Eine XML-Zeichenfolge, die eine Reihe von Freunde der Person darstellt, und gemäß Definition im XML-Schema für die Erweiterbarkeit des Outlook Social Connector (OSC)-Anbieter mit der Definition des **Freunde** entspricht.</span><span class="sxs-lookup"><span data-stu-id="a85e8-107">[out] An XML string that represents a set of friends of the person, and that complies with the definition of **friends** as defined in the XML schema for Outlook Social Connector (OSC) provider extensibility.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a85e8-108">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a85e8-108">Remarks</span></span>

<span data-ttu-id="a85e8-109">Die OSC-Aufrufe **GetFriendsAndColleagues** , wenn der OSC-Anbieter unterstützt zwischengespeichert oder Hybrid Synchronisierung von Freunde im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a85e8-109">The OSC calls **GetFriendsAndColleagues** if the OSC provider supports cached or hybrid synchronization of friends on the social network.</span></span> <span data-ttu-id="a85e8-110">Wenn die OSC zunächst die **GetFriendsAndColleagues** -Methode für den Outlook-Benutzer aufruft, der für das soziale Netzwerk **GetFriendsAndColleagues** angemeldet ist, gibt eine XML-Zeichenfolge, die Freunde des angemeldeten Benutzers im sozialen Netzwerk darstellt zurück.</span><span class="sxs-lookup"><span data-stu-id="a85e8-110">When the OSC initially calls the **GetFriendsAndColleagues** method for the Outlook user who is logged on to the social network, **GetFriendsAndColleagues** returns an XML string that represents friends of the logged-on user on the social network.</span></span> <span data-ttu-id="a85e8-111">Die XML-Zeichenfolge die **Freunde** XML-Schemadefinition entspricht und gibt ein **Person** -Element (das auch die OSC-Anbieter-Schemadefinition entspricht) für jeden Friend.</span><span class="sxs-lookup"><span data-stu-id="a85e8-111">The XML string complies with the **friends** XML schema definition and specifies a **person** element (which also complies with the OSC provider schema definition) for each friend.</span></span> 
  
<span data-ttu-id="a85e8-112">Wenn **GetFriendsAndColleagues** den Freunden, die Informationen für den angemeldeten Benutzer zurückgibt, speichert die OSC, die betreffenden Informationen in einem Kontakteordner.</span><span class="sxs-lookup"><span data-stu-id="a85e8-112">When **GetFriendsAndColleagues** returns the friends information for the logged-on user, the OSC stores that information in a contacts folder.</span></span> <span data-ttu-id="a85e8-113">Dieser Ordner ist speziell für das soziale Netzwerk und befindet sich im Outlook-Standardspeicher des angemeldeten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="a85e8-113">This folder is specific to the social network and resides in the logged-on user's default Outlook store.</span></span> <span data-ttu-id="a85e8-114">Weitere Informationen dazu, wie die OSC Informationen in einem Kontakteordner Freunde zwischenspeichert finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="a85e8-114">For more information about how the OSC caches friends' information in a contacts folder, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span>
  
<span data-ttu-id="a85e8-115">Die XML-Schemadefinition für **Person**erfüllt Informationen für jede Freund, die in der _PersonsCollection_ -Parameter zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a85e8-115">Information for each friend returned in the  _personsCollection_ parameter complies with the XML schema definition for **person**.</span></span> <span data-ttu-id="a85e8-116">Das **Person** -Element unterstützt viele Teile der Informationen für einen Freund, einschließlich der SMTP-e-Mail-Adressen (, die die Elemente **EmailAddress**, **emailAddress2**und **emailAddress3** zugeordnet sind), dass die Friend angegeben wurde, auf die soziale Netzwerke und die Benutzer-ID (die **UserID** -Element zugeordnet ist), die dieser Adresse im sozialen Netzwerk identifiziert.</span><span class="sxs-lookup"><span data-stu-id="a85e8-116">The **person** element supports many pieces of information for each friend, including the SMTP email addresses (which map to the **emailAddress**, **emailAddress2**, and **emailAddress3** elements) that the friend has specified on the social network, and the user ID (which maps to the **userID** element) that identifies that friend on the social network.</span></span> 
  
<span data-ttu-id="a85e8-117">Zum Anzeigen von Aktivitäten für ein Outlook-Benutzer im Bereich Personen ausgewählt, versucht das osc bilden den Benutzer mit jeder Freund von **GetFriendsAndColleagues**zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a85e8-117">To show activities for an Outlook user selected in the People Pane, the OSC tries to match the user with each friend returned from **GetFriendsAndColleagues**.</span></span> <span data-ttu-id="a85e8-118">Die OSC wird durch den Abgleich der SMTP-Adresse des ausgewählten Outlook-Benutzers mit der e-Mail-Adressen, die jeder Freund im sozialen Netzwerk angegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="a85e8-118">The OSC does this by matching the SMTP address of the selected Outlook user with the email addresses that each friend has specified on the social network.</span></span> <span data-ttu-id="a85e8-119">Findet die OSC entsprechende SMTP-e-Mail-Adresse, verwendet das osc bilden die entsprechenden **Benutzer-ID** des der Freund die [ISocialSession::GetPerson](isocialsession-getperson.md) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="a85e8-119">If the OSC finds a matching SMTP email address, the OSC uses the corresponding **userID** of the friend to call the [ISocialSession::GetPerson](isocialsession-getperson.md) method.</span></span> <span data-ttu-id="a85e8-120">Wird diese Option, damit ein [ISocialPerson](isocialpersoniunknown.md) -Objekt für diese Friend abzurufen, die dann die OSC Aktivitäten und Bilder von dieser Adresse aus dem sozialen Netzwerk abgerufen wird aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a85e8-120">It does this to obtain an [ISocialPerson](isocialpersoniunknown.md) object for that friend, which then enables the OSC to get activities and pictures of that friend from the social network.</span></span> 
  
<span data-ttu-id="a85e8-121">Jedoch, wenn der ausgewählte Outlook-Benutzer keine der gleichen SMTP-Adresse eines Kontos im sozialen Netzwerk angegeben wird, oder wenn der Outlook-Benutzer nicht über ein Konto für das soziale Netzwerk verfügt, die OSC ist nicht möglich, eine Übereinstimmung für diesen Benutzer zu erhalten und zeigt keine activiti es für diesen Benutzer für das soziale Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="a85e8-121">However, if the selected Outlook user does not specify that same SMTP address on an account on the social network, or if the Outlook user does not have an account on that social network, the OSC will not be able to find a match for that user and will not display any activities for that user on the social network.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a85e8-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a85e8-122">See also</span></span>

- [<span data-ttu-id="a85e8-123">ISocialPerson : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a85e8-123">ISocialPerson : IUnknown</span></span>](isocialpersoniunknown.md)
- [<span data-ttu-id="a85e8-124">Abrufen von Informationen von Freunden</span><span class="sxs-lookup"><span data-stu-id="a85e8-124">Getting Friends Information</span></span>](getting-friends-information.md)

