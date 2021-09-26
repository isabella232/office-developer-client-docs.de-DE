---
title: Testen von Freunden
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Anbieter des Outlook Connector für soziale Netzwerke (OSC) je nach vom Anbieter unterstütztem Synchronisierungsmodus gegebenenfalls Daten von Freunden und Nicht-Freunden zurückgibt.
ms.openlocfilehash: f882a2003675840d4096660a397f9b032a9a1e7c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608802"
---
# <a name="testing-friends"></a>Testen von Freunden

In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Anbieter des Outlook Connector für soziale Netzwerke (OSC) je nach vom Anbieter unterstütztem Synchronisierungsmodus gegebenenfalls Daten von Freunden und Nicht-Freunden zurückgibt.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Zwischengespeicherte Synchronisierung

Ein OSC-Anbieter implementiert [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), die der OSC aufruft, um zu bestimmen, ob der Anbieter die zwischengespeicherte Synchronisierung der Freundesdaten unterstützt. Nach dem Aufrufen von [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)speichert der OSC die zurückgegebenen Freundesdaten in einem Kontaktordner speziell für das soziale Netzwerk im standardmäßigen Outlook speicher des angemeldeten Benutzers. Der OSC ruft auch [ISocialSession::GetPerson](isocialsession-getperson.md) und [ISocialPerson::GetPicture](isocialperson-getpicture.md) auf, um ein Profilbild für jeden Freund abzurufen. 
  
### <a name="initiate-synchronization"></a>Initiieren der Synchronisierung

Um die Synchronisierung zu initiieren, können Sie die Debugschaltfläche **"Kontakte synchronisieren"** in der Menübandkomponente der Microsoft Office Fluent Benutzeroberfläche aktivieren und verwenden. Weitere Informationen zu OSC-Debugschaltflächen finden Sie unter [Debuggen eines Anbieters.](debugging-a-provider.md) 
  
### <a name="test-scenarios"></a>Testszenarien

Testen Sie die folgenden Elemente, um zu überprüfen, ob die Daten von Freunden richtig zwischengespeichert sind.
  
|**Zu testendes Element**|**Erwartetes Verhalten**|
|:-----|:-----|
|Kontakteordner  <br/> |Der Kontaktordner für soziale Netzwerke befindet sich im Standardmäßigen Outlook Speicher des Benutzers.  <br/> |
|Von **ISocialPerson zurückgegebene Freundesdaten::GetFriendsAndColleagues** <br/> |Jeder Freund entspricht einem Kontakt im netzwerkspezifischen Kontaktordner.  <br/> |
|Freundesdaten  <br/> |Kontaktfelder für jeden Freund haben die richtigen Daten.  <br/> |
|Von **ISocialPerson zurückgegebene Freundesprofilbilder::GetPicture** <br/> |Das Kontaktelement für jeden Freund enthält das Profilbild.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>On-Demand-Synchronisierung

Ein OSC-Anbieter implementiert **ISocialProvider::GetCapabilities**, die der OSC aufruft, um zu bestimmen, ob der Anbieter die On-Demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt. Für die im Outlook Personenbereich angezeigten Personen ruft der OSC ihre SMTP-Adressen ab und hashet diese, ruft [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)auf und speichert (im Arbeitsspeicher) die für diese Personen zurückgegebenen Daten. 
  
### <a name="determining-friends-and-non-friends"></a>Ermitteln von Freunden und Nicht-Freunden

Die an **GetPeopleDetails** übergebenen SMTP-Hashadressen sind der Schlüssel, um zu bestimmen, ob eine Person ein Freund oder kein Freund ist. Wenn eine Person diese SMTP-Adresse nicht in ihr Konto in einem sozialen Netzwerk einschließt oder selbst wenn diese Person ein Freund von einer anderen E-Mail-Adresse im sozialen Netzwerk ist, gibt **GetPeopleDetails** für diese Person weiterhin **"nonfriend"** als **friendStatus** im  _Parameter "personsCollection"_ zurück. Außerdem enthalten die zurückgegebenen Daten für eine Person, die kein Freund ist, aber die SMTP-Adresse in ihrem Konto in ihrem sozialen Netzwerk angibt, nur das, was einem Nicht-Freund gemäß den Datenschutzeinstellungen dieser Person zur Verfügung steht. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Erstellen von Testfächern für Freunde und Nicht-Freunde

Um einen Testbeantragsteller für einen Freund zu erstellen, identifizieren Sie die SMTP-Adresse einer Person, die diese Adresse in sein Konto in einem sozialen Netzwerk einschließt und die einen Freundesstatus mit dem angemeldeten Benutzer in diesem Netzwerk hat. Erstellen Sie eine E-Mail-Nachricht, die diese SMTP-Adresse enthält. Um einen Testantrag für einen Nicht-Freund zu erstellen, identifizieren Sie auch die SMTP-Adresse einer Person, die kein Freund des angemeldeten Benutzers ist, anhand dieser Adresse, und die jedoch in ihren Datenschutzeinstellungen angegeben hat, dass Nicht-Freunde ihre Aktivitäten im sozialen Netzwerk anzeigen können. Erstellen Sie eine E-Mail-Nachricht, die diese SMTP-Adresse enthält. 
  
Wenn Sie im Outlook Explorer die E-Mail-Nachricht auswählen, die einen Freund (oder einen Nicht-Freund) enthält, werden im Personenbereich die Empfänger angezeigt. Wenn Sie den Freund (oder Nicht-Freund) im Personenbereich auswählen, können Sie testen, ob der Anbieter Informationen über die Person bereitstellt.
  
### <a name="test-scenarios"></a>Testszenarien

Um zu überprüfen, ob Ihr Anbieter Informationen zu Freunden und Nicht-Freunden ordnungsgemäß bereitstellt, testen Sie die folgenden Szenarien.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Die im Personenbereich ausgewählte Person ist ein Freund des angemeldeten Benutzers im sozialen Netzwerk.  <br/> |Im Personenbereich werden die Aktivitäten dieser Person im sozialen Netzwerk angezeigt.  <br/> |
|Die im Personenbereich ausgewählte Person ist ein Nicht-Freund des angemeldeten Benutzers im sozialen Netzwerk, hat jedoch zugelassen, dass seine Aktivitäten von Nicht-Freunden angezeigt werden.  <br/> |Im Personenbereich werden die Aktivitäten dieser Person im sozialen Netzwerk angezeigt.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Hybridsynchronisierung

Wenn ein OSC-Anbieter die hybride Synchronisierung von Freunden und Nicht-Freunden unterstützt, führt osc Folgendes aus: 
  
- Der OSC speichert Informationen für Freunde des angemeldeten Benutzers im kontaktspezifischen Kontaktordner für soziale Netzwerke.
    
- Der OSC ruft Informationen für Nicht-Freunde bei Bedarf aus dem sozialen Netzwerk ab und speichert sie nur im Arbeitsspeicher, aber nicht in einem Ordner.
    
Um die Hybridsynchronisierung zu testen, befolgen Sie die Testvorschläge im Abschnitt ["Zwischengespeicherte Synchronisierung"](#olosc_TestingFriends_CachedSync) für Freunde und die Vorschläge im Abschnitt ["On-Demand-Synchronisierung"](#olosc_TestingFriends_OnDemandSync) für Nicht-Freunde. 
  
## <a name="see-also"></a>Siehe auch

- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [XML für Freunde](xml-for-friends.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

