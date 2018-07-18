---
title: Abrufen von Informationen von Freunden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Outlook Social Connector (OSC) die ISocialProvider::GetCapabilities-Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen.
ms.openlocfilehash: 68443992351f4c83e8e560a753941e97bf91de67
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795952"
---
# <a name="getting-friends-information"></a><span data-ttu-id="7ba03-103">Abrufen von Informationen von Freunden</span><span class="sxs-lookup"><span data-stu-id="7ba03-103">Getting friends information</span></span>

<span data-ttu-id="7ba03-104">Outlook Social Connector (OSC) die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen.</span><span class="sxs-lookup"><span data-stu-id="7ba03-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="7ba03-105">Die **GetFriends** und **CacheFriends** -Elemente in der zurückgegebenen **Funktionen** XML angeben, dass der OSC-Anbieter erste Freunde unterstützt und Zwischenspeichern Freunde als Outlook im entsprechenden Kontakteordner Kontaktelemente, kann die OSC vornehmen. die folgenden aufrufende Sequenz.</span><span class="sxs-lookup"><span data-stu-id="7ba03-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="7ba03-106">Die OSC ruft Methoden in der aufgeführten Reihenfolge aus, um Informationen und Bilder erhalten (wie durch die [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle unterstützt) für Freunde im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7ba03-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7ba03-107">Die OSC wird der Cache standardmäßig in Abständen aktualisiert.</span><span class="sxs-lookup"><span data-stu-id="7ba03-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="7ba03-108">Wenn ein Fehler auftritt, während der Cache aktualisieren Sie, die OSC-Wiederholungsversuche in einer anderen vordefinierten Intervall aus, die auch gesteuert werden können, indem Sie das **ContactSyncRestartInterval** -Element in **Funktionen** XML angeben.</span><span class="sxs-lookup"><span data-stu-id="7ba03-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="7ba03-109">Weitere Informationen zum Aktualisieren des Caches für Kontakte finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="7ba03-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="7ba03-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) – die OSC Ruft die Benutzer-ID des Office-Benutzers, der dem sozialen Netzwerk angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="7ba03-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="7ba03-111">[ISocialSession::GetPerson](isocialsession-getperson.md) – verwenden die Benutzer-ID des Office-Benutzers, der OSC Ruft ein Objekt **ISocialPerson** für diesen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="7ba03-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="7ba03-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) – die OSC dient zum Abrufen der Liste des Benutzers Friend im sozialen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="7ba03-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="7ba03-113">[ISocialSession::GetPerson](isocialsession-getperson.md) – für jede Person in der XML-Code durch den **GetFriendsAndColleagues**zurückgegeben, ruft das osc bilden eine **ISocialPerson** -Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7ba03-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="7ba03-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) – für jede Person in der XML-Code durch den **GetFriendsAndColleagues**zurückgegeben, ruft das osc bilden eine Bildressource ab.</span><span class="sxs-lookup"><span data-stu-id="7ba03-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7ba03-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ba03-115">See also</span></span>

- [<span data-ttu-id="7ba03-116">XML-Code für Funktionen</span><span class="sxs-lookup"><span data-stu-id="7ba03-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="7ba03-117">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="7ba03-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

