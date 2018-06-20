---
title: Abrufen von Informationen Freunde
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
# <a name="getting-friends-information"></a>Abrufen von Informationen Freunde

Outlook Social Connector (OSC) die [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode aufgerufen, um die Funktionen des OSC-Anbieter für soziale Netzwerke bestimmen. Die **GetFriends** und **CacheFriends** -Elemente in der zurückgegebenen **Funktionen** XML angeben, dass der OSC-Anbieter erste Freunde unterstützt und Zwischenspeichern Freunde als Outlook im entsprechenden Kontakteordner Kontaktelemente, kann die OSC vornehmen. die folgenden aufrufende Sequenz. Die OSC ruft Methoden in der aufgeführten Reihenfolge aus, um Informationen und Bilder erhalten (wie durch die [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle unterstützt) für Freunde im sozialen Netzwerk. 
  
> [!NOTE]
> Die OSC wird der Cache standardmäßig in Abständen aktualisiert. Wenn ein Fehler auftritt, während der Cache aktualisieren Sie, die OSC-Wiederholungsversuche in einer anderen vordefinierten Intervall aus, die auch gesteuert werden können, indem Sie das **ContactSyncRestartInterval** -Element in **Funktionen** XML angeben. Weitere Informationen zum Aktualisieren des Caches für Kontakte finden Sie unter [Synchronisieren Freunde und Aktivitäten](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession::LoggedOnUserID](isocialsession-loggedonuserid.md) – die OSC Ruft die Benutzer-ID des Office-Benutzers, der dem sozialen Netzwerk angemeldet ist. 
    
2. [ISocialSession::GetPerson](isocialsession-getperson.md) – verwenden die Benutzer-ID des Office-Benutzers, der OSC Ruft ein Objekt **ISocialPerson** für diesen Benutzer. 
    
3. [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) – die OSC dient zum Abrufen der Liste des Benutzers Friend im sozialen Netzwerk. 
    
4. [ISocialSession::GetPerson](isocialsession-getperson.md) – für jede Person in der XML-Code durch den **GetFriendsAndColleagues**zurückgegeben, ruft das osc bilden eine **ISocialPerson** -Schnittstelle. 
    
5. [ISocialPerson::GetPicture](isocialperson-getpicture.md) – für jede Person in der XML-Code durch den **GetFriendsAndColleagues**zurückgegeben, ruft das osc bilden eine Bildressource ab.
    
## <a name="see-also"></a>Siehe auch

- [XML-Code für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

