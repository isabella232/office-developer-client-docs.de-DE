---
title: Abrufen von Informationen von Freunden
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d8a56746-4de4-4f24-af32-e85079c060b8
description: 'Der Outlook Connector für soziale Netzwerke (OSC) Ruft die ISocialProvider:: getCapabilities-Methode auf, um die Funktionen des OSC-Anbieters für ein soziales Netzwerk zu bestimmen.'
ms.openlocfilehash: 697902631b010afab015e9cfb73fac81ac427d6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428795"
---
# <a name="getting-friends-information"></a>Abrufen von Informationen von Freunden

Der Outlook Connector für soziale Netzwerke (OSC) Ruft die [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode auf, um die Funktionen des osc-Anbieters für ein soziales Netzwerk zu bestimmen. Wenn die **Getfriends** -und **cacheFriends** -Elemente in den zurückgegebenen **Capabilities** -XML-Daten darauf HINweisen, dass der osc-Anbieter unterstützt, Freunde und zwischen Speicherungs Freunde als Outlook-Kontaktelemente in einem entsprechenden Ordner "Kontakte" zu erhalten, kann osc die folgende aufrufende Sequenz. OSC ruft Methoden in dieser Reihenfolge auf, um Informationen und Bilder (wie von der [ISocialPerson](isocialpersoniunknown.md) -Schnittstelle unterstützt) für Freunde im sozialen Netzwerk zu erhalten. 
  
> [!NOTE]
> Der OSC aktualisiert den Cache in einem Standardintervall. Wenn während der Cacheaktualisierung ein Fehler auftritt, versucht der OSC bei einem anderen vordefinierten Intervall, das auch durch Angeben des **contactSyncRestartInterval** -Elements im **Capabilities** -XML gesteuert werden kann. Weitere Informationen zum Aktualisieren des Kontakte Caches finden Sie unter [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md). 
  
1. [ISocialSession:: LoggedOnUserID](isocialsession-loggedonuserid.md) – osc Ruft die Benutzer-ID des Office-Benutzers ab, der am sozialen Netzwerk angemeldet ist. 
    
2. [ISocialSession:: GetPerson](isocialsession-getperson.md) -mit der Benutzer-ID des Office-Benutzers ruft der osc ein **ISocialPerson** -Objekt für diesen Benutzer ab. 
    
3. [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md) – osc Ruft die Friend-Liste des Benutzers im sozialen Netzwerk ab. 
    
4. [ISocialSession:: GetPerson](isocialsession-getperson.md) -für jede Person in der von **GETFRIENDSANDCOLLEAGUES**zurückgegebenen XML-Code ruft der osc eine **ISocialPerson** -Schnittstelle ab. 
    
5. [ISocialPerson:: GetPicture](isocialperson-getpicture.md) – für jede Person in der von **GETFRIENDSANDCOLLEAGUES**zurückgegebenen XML-Code ruft der osc eine Bildressource ab.
    
## <a name="see-also"></a>Siehe auch

- [XML für Funktionen](xml-for-capabilities.md)
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)

