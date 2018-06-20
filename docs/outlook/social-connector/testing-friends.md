---
title: Testen der Freunde
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 109c34b6-911b-4dfc-9799-aadf47172e84
description: In diesem Thema wird beschrieben, Tests und Szenarien, um sicherzustellen, dass der Anbieter Outlook Social Connector (OSC) entsprechend Daten des Freunde und nicht-Freunde, zurückgibt, sofern zutreffend, je nach den vom Anbieter unterstützten Synchronisierungsmodus.
ms.openlocfilehash: 232977836833a9ef981ebef38c9ee243ea2dd2ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796104"
---
# <a name="testing-friends"></a>Testen der Freunde

In diesem Thema wird beschrieben, Tests und Szenarien, um sicherzustellen, dass der Anbieter Outlook Social Connector (OSC) entsprechend Daten des Freunde und nicht-Freunde, zurückgibt, sofern zutreffend, je nach den vom Anbieter unterstützten Synchronisierungsmodus.

<a name="olosc_TestingFriends_CachedSync"> </a>

## <a name="cached-synchronization"></a>Cache-Synchronisierung

Ein OSC-Anbieter implementiert [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md), die die OSC aufruft, um zu bestimmen, ob der Anbieter zwischengespeicherten Synchronisierung Freunde Daten unterstützt. Nach dem Aufruf von [ISocialPerson::GetFriendsAndColleagues](isocialperson-getfriendsandcolleagues.md), speichert das osc bilden die zurückgegebene Freunde Daten in einem Kontakteordner speziell für das soziale Netzwerke in Outlook-Standardspeicher des angemeldeten Benutzers. Die OSC ruft auch [ISocialSession::GetPerson](isocialsession-getperson.md) und [ISocialPerson::GetPicture](isocialperson-getpicture.md) , um ein Profilbild für jede Friend erhalten. 
  
### <a name="initiate-synchronization"></a>Initiieren Sie die Synchronisierung

Um die Synchronisierung einzuleiten können Sie aktivieren und die Schaltfläche Debuggen **Kontakte synchronisieren** in der Menübandkomponente der Microsoft Office Fluent-Benutzeroberfläche verwenden. Weitere Informationen zu OSC Debug Schaltflächen finden Sie unter [Debuggen eines Providers](debugging-a-provider.md). 
  
### <a name="test-scenarios"></a>Testszenarien

Testen Sie die folgenden Elemente, um sicherzustellen, dass Freunde Daten ordnungsgemäß zwischengespeichert werden.
  
|**Zu überprüfende Element**|**Erwartetes Verhalten**|
|:-----|:-----|
|Ordner "Kontakte"  <br/> |Der Ordner sozialen Netzwerk-spezifischen Kontakte in Outlook-Standardspeicher des Benutzers vorhanden ist.  <br/> |
|Freunde von **ISocialPerson::GetFriendsAndColleagues** zurückgegebenen Daten <br/> |Jeder Freund entspricht einem Kontakt in den Kontakteordner von Netzwerk-spezifische.  <br/> |
|Freunde Daten  <br/> |Für jede Friend Kontaktfelder haben die richtigen Daten.  <br/> |
|Freunde Profilbilder zurückgegebene **ISocialPerson::GetPicture** <br/> |Das Kontaktelement für jede Friend enthält das Profilbild.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="on-demand-synchronization"></a>Bedarfsgesteuerte Synchronisierung

Ein OSC-Anbieter implementiert **ISocialProvider::GetCapabilities**, die die OSC aufruft, um zu bestimmen, ob der Anbieter bedarfsgesteuerten Synchronisierung von Freunde und Freunde-nicht unterstützt. Für die Personen, die im Bereich Personen Outlook angezeigt wird erhält der OSC und Hashes, die Ihre SMTP-Adressen, ruft [ISocialSession2::GetPeopleDetails](isocialsession2-getpeopledetails.md)und speichert (im Arbeitsspeicher) die Daten, für diese Personen zurückgegeben. 
  
### <a name="determining-friends-and-non-friends"></a>Bestimmen der Freunde und nicht-Freunde

Hash SMTP-Adressen an **GetPeopleDetails** übergeben werden die Taste, um zu bestimmen, ob eine Person ein Freund oder nicht Friend ist. Wenn eine Person die SMTP-Adresse nicht in seinem für soziale Netzwerkkonto enthalten ist, oder, auch wenn diese Person einen Freund durch eine andere e-Mail-Adresse im sozialen Netzwerk ist, gibt **GetPeopleDetails** noch **Nonfriend** für diese Person als der ** FriendStatus** im _PersonsCollection_ -Parameter. Darüber hinaus enthält für eine Person, ist nicht mit einem Freund, gibt die SMTP-Adresse im sozialen Netzwerk-Konto, die zurückgegebenen Daten nur an einen nicht-Freund, wie durch die datenschutzeinstellungen der betreffenden Person zugelassen verfügbar sind. 
  
### <a name="creating-test-subjects-for-friends-and-non-friends"></a>Erstellen von Test-Themen für Freunde und nicht Freunde

So erstellen Sie einen Test Betreff für einen Freund, identifizieren Sie die SMTP-Adresse einer Person, die diese Adresse enthält, in Konto für soziale Netzwerke und wer hat einen Freund Status mit der angemeldete Benutzer auf das Netzwerk. Erstellen Sie eine e-Mail-Nachricht, die diese SMTP-Adresse enthält. Identifizieren Sie entsprechend um einen Test Betreff für einen Freund zu erstellen, die SMTP-Adresse einer Person, die keinen Freund des angemeldeten Benutzers von dieser Adresse, und angegeben, die noch in seinem datenschutzeinstellungen auf nicht-Freunde deren Aktivitäten auf die soziale Netzwerke anzeigen zulassen k. Erstellen Sie eine e-Mail-Nachricht, die diese SMTP-Adresse enthält. 
  
Wenn Sie die e-Mail-Nachricht auswählen, die ein Friend (oder nicht Friend) enthält, zeigt den Bereich Personen im Outlook-Explorer die Empfänger an. Auswählen der Friend (oder nicht Friend) im Bereich Personen können Sie testen, dass der Anbieter, Informationen über die Person bereitstellt.
  
### <a name="test-scenarios"></a>Testszenarien

Testen Sie um zu überprüfen, dass der Anbieter Informationen über Freunde und nicht-Freunde entsprechend bereitstellt, für die folgenden Szenarien.
  
|**Szenario**|**Erwartetes Verhalten**|
|:-----|:-----|
|Person, die Sie im Bereich Personen ausgewählt ist ein Freund mit dem angemeldeten Benutzer im sozialen Netzwerk.  <br/> |Bereich Personen diese Person Aktivitäten auf dem sozialen Netzwerk angezeigt.  <br/> |
|Person, die Sie im Bereich Personen ausgewählt ist ein nicht-Freund des angemeldeten Benutzers im sozialen Netzwerk, jedoch hat seine Aktivitäten aus, die von nicht-Freunde angezeigt werden zulässig.  <br/> |Bereich Personen diese Person Aktivitäten auf dem sozialen Netzwerk angezeigt.  <br/> |

<a name="olosc_TestingFriends_OnDemandSync"> </a>

## <a name="hybrid-synchronization"></a>Hybrid-Synchronisierung

Wenn ein OSC-Anbieter Hybrid Synchronisierung von Freunde und Freunde-nicht unterstützt, führt der OSC Folgendes aus: 
  
- Die OSC speichert Informationen für Freunde des angemeldeten Benutzers in der sozialen Netzwerk-spezifische Kontaktordner.
    
- Die OSC Ruft Informationen für nicht-Freunde auf Abruf aus dem sozialen Netzwerk und nur im Arbeitsspeicher, aber nicht in einem Ordner gespeichert.
    
Führen Sie zum Testen der Synchronisierung Hybrid testing Vorschläge im Abschnitt [Synchronisierung Cache](#olosc_TestingFriends_CachedSync) für Freunde und die in den Abschnitt [Bedarfsgesteuerten Synchronisierung](#olosc_TestingFriends_OnDemandSync) für nicht-Freunde aus. 
  
## <a name="see-also"></a>Siehe auch

- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md) 
- [XML-Code für Freunde](xml-for-friends.md)
- [Vorbereitung der Freigabe eines OSC-Providers](getting-ready-to-release-an-osc-provider.md)

