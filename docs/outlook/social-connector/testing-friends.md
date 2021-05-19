---
title: Testen von Freunden
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Outlook Social Connector (OSC)-Anbieter abhängig vom vom Anbieter unterstützten Synchronisierungsmodus daten von Freunden und Nicht-Freunden entsprechend zurückgibt.
ms.openlocfilehash: 1c97342fd5b219b15b1f58dbc065fc268f8e81d7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433668"
---
# <a name="testing-friends"></a>Testen von Freunden

In diesem Thema werden Tests und Szenarien beschrieben, um zu überprüfen, ob der Outlook Social Connector (OSC)-Anbieter abhängig vom vom Anbieter unterstützten Synchronisierungsmodus daten von Freunden und Nicht-Freunden entsprechend zurückgibt.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Zwischengespeicherte Synchronisierung

Ein OSC-Anbieter implementiert [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), das vom OSC aufruft, um zu bestimmen, ob der Anbieter die zwischengespeicherte Synchronisierung der Freundesdaten unterstützt. Nach dem Aufruf von [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md)speichert das OSC die zurückgegebenen Freundesdaten in einem kontaktspezifischen Ordner für das soziale Netzwerk im Standardspeicher des angemeldeten Benutzers Outlook. Das OSC ruft außerdem [ISocialSession::GetPerson](isocialsession-getperson.md) und [ISocialPerson::GetPicture](isocialperson-getpicture.md) auf, um ein Profilbild für jeden Freund zu erhalten. 
  
### <a name="initiate-synchronization"></a>Initiieren der Synchronisierung

Zum Initiieren der Synchronisierung können Sie die Debugschaltfläche Kontakte **synchronisieren** in der Menübandkomponente der Microsoft Office Verwenden. Weitere Informationen zu OSC-Debugschaltflächen finden Sie unter [Debuggen eines Anbieters](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Testszenarien

Testen Sie die folgenden Elemente, um zu überprüfen, ob die Daten von Freunden richtig zwischengespeichert wurden.
  
|**Zu testende Elemente**|**Erwartetes Verhalten**|
|:-----|:-----|
|Ordner "Kontakte"  <br/> |Der ordner für das soziale Netzwerk spezifische Kontakte ist im Standardspeicher des Benutzers Outlook vorhanden.  <br/> |
|Von **ISocialPerson zurückgegebene Freundesdaten::GetFriendsAndColleagues** <br/> |Jeder Freund entspricht einem Kontakt im netzwerkspezifischen Kontaktordner.  <br/> |
|Freundesdaten  <br/> |Kontaktfelder für jeden Freund verfügen über die richtigen Daten.  <br/> |
|Von ISocialPerson zurückgegebene Profilbilder von **Freunden::GetPicture** <br/> |Das Kontaktelement für jeden Freund enthält das Profilbild.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>On-Demand-Synchronisierung

Ein OSC-Anbieter implementiert **ISocialProvider::GetCapabilities**, das vom OSC aufruft, um zu bestimmen, ob der Anbieter die On-Demand-Synchronisierung von Freunden und Nicht-Freunden unterstützt. Für die Personen, die im Outlook-Personenbereich angezeigt werden, ruft das OSC seine #A0 ab und hasht sie, ruft [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)auf und speichert (im Arbeitsspeicher) die für diese Personen zurückgegebenen Daten. 
  
### <a name="determining-friends-and-non-friends"></a>Ermitteln von Freunden und Nicht-Freunden

Die hashierten SMTP-Adressen, die **an GetPeopleDetails** übergeben werden, sind der Schlüssel, um zu bestimmen, ob eine Person ein Freund oder ein Nichtfreund ist. Wenn eine Person diese #A0 nicht in ihr Konto für soziale Netzwerke einbegibt oder auch wenn es sich  bei dieser Person um einen Freund handelt, der über eine andere E-Mail-Adresse im sozialen Netzwerk verfügt, gibt **GetPeopleDetails** als **friendStatus im** _parameter personsCollection_ immer noch keine Freunde für diese Person zurück. Außerdem enthalten die zurückgegebenen Daten für eine Person, die kein Freund ist, aber die SMTP-Adresse in ihrem Konto für soziale Netzwerke angibt, nur das, was einem Nicht-Freund zur Verfügung steht, wie von den Datenschutzeinstellungen dieser Person zulässig. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Erstellen von Testthemen für Freunde und Nicht-Freunde

Um einen Testsubjekt für einen Freund zu erstellen, identifizieren Sie die SMTP-Adresse einer Person, die diese Adresse in ihr Konto für soziale Netzwerke ein schließt und über einen Freundesstatus mit dem angemeldeten Benutzer in diesem Netzwerk verfügt. Erstellen Sie eine E-Mail-Nachricht, die diese SMTP-Adresse enthält. Um einen Testbearbeiter für einen Nichtfreund zu erstellen, identifizieren Sie die SMTP-Adresse einer Person, die kein Freund des angemeldeten Benutzers ist, und die in ihren Datenschutzeinstellungen angegeben hat, dass Nicht-Freunde ihre Aktivitäten im sozialen Netzwerk anzeigen können. Erstellen Sie eine E-Mail-Nachricht, die diese SMTP-Adresse enthält. 
  
Wenn Sie Outlook E-Mail-Nachricht auswählen, die einen Freund (oder einen Nicht-Freund) enthält, zeigt der Personenbereich die Empfänger an. Wenn Sie den Freund (oder den Nicht-Freund) im Personenbereich auswählen, können Sie testen, ob der Anbieter Informationen über die Person zur Verfügung stellt.
  
### <a name="test-scenarios"></a>Testszenarien

Um sicherzustellen, dass Ihr Anbieter Informationen zu Freunden und Nicht-Freunden entsprechend zur Verfügung stellt, testen Sie die folgenden Szenarien.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Die im Personenbereich ausgewählte Person ist ein Freund des angemeldeten Benutzers im sozialen Netzwerk.  <br/> |Im Bereich Personen werden die Aktivitäten dieser Person im sozialen Netzwerk angezeigt.  <br/> |
|Die im Personenbereich ausgewählte Person ist ein Nichtfreund des angemeldeten Benutzers im sozialen Netzwerk, hat jedoch zugelassen, dass seine Aktivitäten von Nicht-Freunden angezeigt werden.  <br/> |Im Bereich Personen werden die Aktivitäten dieser Person im sozialen Netzwerk angezeigt.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Hybridsynchronisierung

Wenn ein OSC-Anbieter die Hybridsynchronisierung von Freunden und Nicht-Freunden unterstützt, führt das OSC die folgenden Schritte aus: 
  
- Das OSC speichert Informationen für Freunde des angemeldeten Benutzers im kontaktspezifischen Kontaktordner für soziale Netzwerke.
    
- Das OSC ruft Informationen für Nicht-Freunde bei Bedarf aus dem sozialen Netzwerk ab und speichert sie nur im Speicher, aber nicht in einem Ordner.
    
Befolgen Sie zum Testen der Hybridsynchronisierung [](#olosc_TestingFriends_CachedSync) die Testvorschläge im Abschnitt Zwischengespeicherte Synchronisierung für Freunde und die im Abschnitt [On-Demand Synchronization](#olosc_TestingFriends_OnDemandSync) für Nicht-Freunde. 
  
## <a name="see-also"></a>Siehe auch

- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md) 
- [XML für Freunde](xml-for-friends.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

