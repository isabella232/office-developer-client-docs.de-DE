---
title: Testen von Freunden
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Outlook-Anbieter für soziale Netzwerke (OSC) entsprechend der vom Anbieter unterstützten Synchronisierungsmodus Daten von Freunden und nicht-Freunden zurückgibt.
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433668"
---
# <a name="testing-friends"></a>Testen von Freunden

In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Outlook-Anbieter für soziale Netzwerke (OSC) entsprechend der vom Anbieter unterstützten Synchronisierungsmodus Daten von Freunden und nicht-Freunden zurückgibt.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Zwischengespeicherte Synchronisierung

Ein OSC-Anbieter implementiert [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md), die von OSC aufgerufen werden, um zu bestimmen, ob der Anbieter die zwischengespeicherte Synchronisierung von Freunden-Daten unterstützt. Nach dem Aufruf von [ISocialPerson:: GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)speichert osc die Daten der zurückgegebenen Freunde in einem für das soziale netzwerkspezifischen Kontakteordner im Outlook-Standardspeicher des angemeldeten Benutzers. OSC ruft auch [ISocialSession:: GetPerson](isocialsession-getperson.md) und [ISocialPerson:: GetPicture](isocialperson-getpicture.md) auf, um ein Profilbild für jeden Freund abzurufen. 
  
### <a name="initiate-synchronization"></a>Initiieren der Synchronisierung

Um die Synchronisierung zu initiieren, können Sie die Schaltfläche " **** Debuggen" in der Menüband-Komponente der Microsoft Office Fluent-Benutzeroberfläche aktivieren und verwenden. Weitere Informationen zu OSC-Debug-Schaltflächen finden Sie unter [Debuggen eines Anbieters](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Testszenarien

Testen Sie die folgenden Elemente, um sicherzustellen, dass die Daten von Freunden korrekt zwischengespeichert werden.
  
|**Zu testendes Element**|**Erwartetes Verhalten**|
|:-----|:-----|
|Ordner "Kontakte"  <br/> |Der soziale netzwerkspezifische Kontakteordner ist im Outlook-Standardspeicher des Benutzers vorhanden.  <br/> |
|Von ISocialPerson zurückgegebene Daten von Freunden **:: GetFriendsAndColleagues** <br/> |Jeder Freund entspricht einem Kontakt im netzwerkspezifischen Ordner Kontakte.  <br/> |
|Freundes Daten  <br/> |Kontaktfelder für jeden Freund haben die richtigen Daten.  <br/> |
|Von **ISocialPerson:: GetPicture** zurückgegebene Profil Bilder von Freunden <br/> |Das Kontaktelement für jeden Freund enthält das Profilbild.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Bedarfsgesteuerte Synchronisierung

Ein OSC-Anbieter implementiert **ISocialProvider:: getCapabilities**, die von OSC aufgerufen werden, um zu bestimmen, ob der Anbieter die bedarfsgesteuerte Synchronisierung von Freunden und nicht-Freunden unterstützt. Für die Personen, die im Outlook-Personen Bereich angezeigt werden, ruft OSC Ihre SMTP-Adressen ab, hasht Sie [ISocialSession2:: GetPeopleDetails](isocialsession2-getpeopledetails.md)und speichert (im Arbeitsspeicher) die für diese Personen zurückgegebenen Daten. 
  
### <a name="determining-friends-and-non-friends"></a>Bestimmen von Freunden und nicht-Freunden

Die an **GetPeopleDetails** übergebenen Hash-SMTP-Adressen sind der Schlüssel, um zu bestimmen, ob eine Person ein Freund oder nicht Freund ist. Wenn eine Person diese SMTP-Adresse nicht in Ihrem sozialen Netzwerkkonto einschließt oder wenn diese Person ein Freund mit einer anderen e-Mail-Adresse im sozialen Netzwerk ist, gibt **GetPeopleDetails** für diese Person noch keinen **Friend** als ** friendStatus** im persons-Parameter. __ Auch für eine Person, die kein Freund ist, aber die SMTP-Adresse in seinem sozialen Netzwerkkonto angibt, enthält die zurückgegebenen Daten nur die Verfügbarkeit eines nicht-Freundes, wie in den Datenschutzeinstellungen dieser Person zulässig. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Erstellen von Testthemen für Freunde und nicht-Freunde

Wenn Sie einen Test Betreff für einen Freund erstellen möchten, identifizieren Sie die SMTP-Adresse einer Person, die diese Adresse in Ihrem sozialen Netzwerkkonto einschließt und die über einen Friend-Status mit dem angemeldeten Benutzer in diesem Netzwerk verfügt. Erstellen Sie eine e-Mail-Nachricht, die diese SMTP-Adresse enthält. Auf ähnliche Weise können Sie einen Test Betreff für einen nicht-Freund erstellen, indem Sie die SMTP-Adresse einer Person identifizieren, die von dieser Adresse nicht als Freund des angemeldeten Benutzers verwendet wird, und doch wer in seinen Datenschutzeinstellungen angegeben hat, dass nicht-Freunde ihre Aktivitäten im sozialen Networ anzeigen können. k. Erstellen Sie eine e-Mail-Nachricht, die diese SMTP-Adresse enthält. 
  
Wenn Sie im Outlook-Explorer die e-Mail-Nachricht auswählen, die einen Freund (oder nicht-Freund) enthält, werden im Bereich Personen die Empfänger angezeigt. Durch Auswählen des Freundes (oder nicht-Freundes) im Personen Bereich können Sie testen, ob der Anbieter Informationen zur Person bereitstellt.
  
### <a name="test-scenarios"></a>Testszenarien

Um zu überprüfen, ob Ihr Anbieter entsprechende Informationen zu Freunden und nicht-Freunden bereitstellt, testen Sie die folgenden Szenarien.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Person, die im Personen Bereich ausgewählt ist, ist ein Freund des angemeldeten Benutzers im sozialen Netzwerk.  <br/> |Im Bereich Personen werden die Aktivitäten dieser Person im sozialen Netzwerk angezeigt.  <br/> |
|Person, die im Personen Bereich ausgewählt ist, ist ein nicht-Freund des angemeldeten Benutzers im sozialen Netzwerk, hat jedoch zugelassen, dass seine Aktivitäten von nicht-Freunden angezeigt werden.  <br/> |Im Bereich Personen werden die Aktivitäten dieser Person im sozialen Netzwerk angezeigt.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Hybrid Synchronisierung

Wenn ein OSC-Anbieter die Hybrid Synchronisierung von Freunden und nicht-Freunden unterstützt, führt der OSC folgende Aktionen aus: 
  
- OSC speichert Informationen für Freunde des angemeldeten Benutzers im sozialen netzwerkspezifischen Kontaktordner.
    
- OSC Ruft Informationen für nicht-Freunde bei Bedarf aus dem sozialen Netzwerk ab und speichert Sie nur im Arbeitsspeicher, jedoch nicht in einem Ordner.
    
Führen Sie zum Testen der Hybrid Synchronisierung die Testvorschläge im Abschnitt [zwischengespeicherte Synchronisierung](#olosc_TestingFriends_CachedSync) für Freunde und die im Abschnitt [on-Demand-Synchronisierung](#olosc_TestingFriends_OnDemandSync) für nicht-Freunde aus. 
  
## <a name="see-also"></a>Siehe auch

- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [XML für Freunde](xml-for-friends.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

