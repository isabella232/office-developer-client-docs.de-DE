---
title: Abrufen von Informationen von Freunden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Der Outlook Social Connector (OSC) ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428795"
---
# <a name="getting-friends-information"></a><span data-ttu-id="5d864-103">Abrufen von Informationen von Freunden</span><span class="sxs-lookup"><span data-stu-id="5d864-103">Getting friends information</span></span>

<span data-ttu-id="5d864-104">Das Outlook Social Connector (OSC) ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="5d864-104">The Outlook Social Connector (OSC) calls the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method to determine the capabilities of the OSC provider for a social network.</span></span> <span data-ttu-id="5d864-105">Wenn die **Elemente getFriends** und **cacheFriends** im zurückgegebenen Funktionen-XML  angeben, dass der OSC-Anbieter das Abrufen von Freunden und das Zwischenspeichern von Freunden als Outlook Kontaktelemente in einem entsprechenden Kontaktordner unterstützt, kann das OSC die folgende Aufrufsequenz erstellen.</span><span class="sxs-lookup"><span data-stu-id="5d864-105">If the **getFriends** and **cacheFriends** elements in the returned **capabilities** XML indicate that the OSC provider supports getting friends and caching friends as Outlook contact items in a corresponding contacts folder, the OSC can make the following calling sequence.</span></span> <span data-ttu-id="5d864-106">Das OSC ruft Methoden in dieser Sequenz auf, um Informationen und Bilder (wie von der [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) unterstützt) für Freunde im sozialen Netzwerk zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="5d864-106">The OSC calls methods in this sequence to get information and pictures (as supported by the [ISocialPerson](isocialpersoniunknown.md) interface) for friends on the social network.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="5d864-107">Das OSC aktualisiert den Cache in einem Standardintervall.</span><span class="sxs-lookup"><span data-stu-id="5d864-107">The OSC refreshes the cache at a default interval.</span></span> <span data-ttu-id="5d864-108">Wenn während der Cacheaktualisierung ein Fehler auftritt, wird der OSC in einem anderen voreingestellten Intervall erneut gestartet, das auch durch Angeben des **contactSyncRestartInterval-Elements** in der Xml-Funktion **gesteuert** werden kann.</span><span class="sxs-lookup"><span data-stu-id="5d864-108">If an error occurs during cache refresh, the OSC retries at another preset interval, which can also be controlled by specifying the **contactSyncRestartInterval** element in the **capabilities** XML.</span></span> <span data-ttu-id="5d864-109">Weitere Informationen zum Aktualisieren des Kontaktecaches finden Sie [unter Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md).</span><span class="sxs-lookup"><span data-stu-id="5d864-109">For more information about refreshing the contacts cache, see [Synchronizing Friends and Activities](synchronizing-friends-and-activities.md).</span></span> 
  
1. <span data-ttu-id="5d864-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) – Das OSC ruft die Benutzer-ID des Office ab, der beim sozialen Netzwerk angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="5d864-110">[ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) —The OSC gets the user ID of the Office user who is logged onto the social network.</span></span> 
    
2. <span data-ttu-id="5d864-111">[ISocialSession::GetPerson](isocialsession-getperson.md) – Mithilfe der Benutzer-ID des Office-Benutzers ruft das OSC ein **ISocialPerson-Objekt** für den Benutzer ab.</span><span class="sxs-lookup"><span data-stu-id="5d864-111">[ISocialSession::GetPerson](isocialsession-getperson.md) —Using the user ID of the Office user, the OSC gets an **ISocialPerson** object for that user.</span></span> 
    
3. <span data-ttu-id="5d864-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) – Das OSC ruft die Freundesliste des Benutzers im sozialen Netzwerk ab.</span><span class="sxs-lookup"><span data-stu-id="5d864-112">[ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) —The OSC gets the user's friend list on the social network.</span></span> 
    
4. <span data-ttu-id="5d864-113">[ISocialSession::GetPerson](isocialsession-getperson.md) – Für jede Person in der von **GetFriendsAndColleagues** zurückgegebenen XML ruft das OSC eine **ISocialPerson-Schnittstelle** ab.</span><span class="sxs-lookup"><span data-stu-id="5d864-113">[ISocialSession::GetPerson](isocialsession-getperson.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets an **ISocialPerson** interface.</span></span> 
    
5. <span data-ttu-id="5d864-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) – Für jede Person in der von **GetFriendsAndColleagues** zurückgegebenen XML ruft das OSC eine Bildressource ab.</span><span class="sxs-lookup"><span data-stu-id="5d864-114">[ISocialPerson::GetPicture](isocialperson-getpicture.md) —For each person in the XML returned by **GetFriendsAndColleagues**, the OSC gets a picture resource.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="5d864-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d864-115">See also</span></span>

- [<span data-ttu-id="5d864-116">XML für Funktionen</span><span class="sxs-lookup"><span data-stu-id="5d864-116">XML for Capabilities</span></span>](xml-for-capabilities.md)
- [<span data-ttu-id="5d864-117">OSC - Typische Aufrufsequenzen</span><span class="sxs-lookup"><span data-stu-id="5d864-117">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)

