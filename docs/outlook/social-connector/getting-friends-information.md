---
title: Abrufen von Informationen von Freunden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: Der Outlook Connector für soziale Netzwerke (OSC) ruft die ISocialProvider::GetCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln.
ms.openlocfilehash: 807a71dbb009a9dd34884c77d6d74c9729a5adc3
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563252"
---
# <a name="getting-friends-information"></a>Abrufen von Informationen von Freunden

Der Outlook Connector für soziale Netzwerke (OSC) ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln. Wenn die **Elemente "getFriends"** und **"cacheFriends"** in den zurückgegebenen **Funktionen** xml angeben, dass der OSC-Anbieter das Abrufen von Freunden und das Zwischenspeichern von Freunden als Outlook Kontaktelemente in einem entsprechenden Kontaktordner unterstützt, kann der OSC die folgende Aufrufsequenz vornehmen. Der OSC ruft Methoden in dieser Sequenz auf, um Informationen und Bilder (wie von der [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) unterstützt) für Freunde im sozialen Netzwerk abzurufen. 
  
> [!NOTE]
> Der OSC aktualisiert den Cache in einem Standardintervall. Wenn während der Cacheaktualisierung ein Fehler auftritt, versucht osc erneut, in einem anderen voreingestellten Intervall zu suchen, das auch durch Angeben des **contactSyncRestartInterval-Elements** in der **Funktions-XML** gesteuert werden kann. Weitere Informationen zum Aktualisieren des Kontaktcaches finden Sie unter ["Synchronisieren von Freunden und Aktivitäten".](synchronizing-friends-and-activities.md) 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) - Der OSC ruft die Benutzer-ID des Office Benutzers ab, der beim sozialen Netzwerk angemeldet ist. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) - Mithilfe der Benutzer-ID des Office Benutzers ruft osc ein **ISocialPerson** -Objekt für diesen Benutzer ab. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) - Der OSC ruft die Freundesliste des Benutzers im sozialen Netzwerk ab. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) - Für jede Person in dem von **GetFriendsAndColleagues zurückgegebenen** XML-Code ruft osc eine **ISocialPerson-Schnittstelle** ab. 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) -Für jede Person in dem von **GetFriendsAndColleagues zurückgegebenen** XML-Code ruft osc eine Bildressource ab.
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

