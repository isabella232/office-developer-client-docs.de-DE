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
# <a name="getting-friends-information"></a>Abrufen von Informationen von Freunden

Das Outlook Social Connector (OSC) ruft die [ISocialProvider::GetCapabilities-Methode](isocialprovider-getcapabilities.md) auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu ermitteln. Wenn die **Elemente getFriends** und **cacheFriends** im zurückgegebenen Funktionen-XML  angeben, dass der OSC-Anbieter das Abrufen von Freunden und das Zwischenspeichern von Freunden als Outlook Kontaktelemente in einem entsprechenden Kontaktordner unterstützt, kann das OSC die folgende Aufrufsequenz erstellen. Das OSC ruft Methoden in dieser Sequenz auf, um Informationen und Bilder (wie von der [ISocialPerson-Schnittstelle](isocialpersoniunknown.md) unterstützt) für Freunde im sozialen Netzwerk zu erhalten. 
  
> [!NOTE]
> Das OSC aktualisiert den Cache in einem Standardintervall. Wenn während der Cacheaktualisierung ein Fehler auftritt, wird der OSC in einem anderen voreingestellten Intervall erneut gestartet, das auch durch Angeben des **contactSyncRestartInterval-Elements** in der Xml-Funktion **gesteuert** werden kann. Weitere Informationen zum Aktualisieren des Kontaktecaches finden Sie [unter Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) – Das OSC ruft die Benutzer-ID des Office ab, der beim sozialen Netzwerk angemeldet ist. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) – Mithilfe der Benutzer-ID des Office-Benutzers ruft das OSC ein **ISocialPerson-Objekt** für den Benutzer ab. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) – Das OSC ruft die Freundesliste des Benutzers im sozialen Netzwerk ab. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) – Für jede Person in der von **GetFriendsAndColleagues** zurückgegebenen XML ruft das OSC eine **ISocialPerson-Schnittstelle** ab. 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) – Für jede Person in der von **GetFriendsAndColleagues** zurückgegebenen XML ruft das OSC eine Bildressource ab.
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

