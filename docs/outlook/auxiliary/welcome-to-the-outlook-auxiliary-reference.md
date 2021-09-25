---
title: Willkommen bei der Outlook-Hilfsreferenz
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
ms.localizationpriority: medium
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Die Outlook Hilfsreferenz enthält konzeptionelle Inhalte und Referenzdokumentation für vier GRUPPEN von APIs, Codebeispiele und ein verteilbares Installationsprogramm, mit dem Entwickler Outlook erweitern und integrieren können. APIs in dieser Referenz werden von Outlook zur Erweiterbarkeit außerhalb des Outlook-Objektmodells verfügbar gemacht.
ms.openlocfilehash: 478dbf3057972b01a453d2dda105135c25517607
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59564490"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Willkommen bei der Outlook-Hilfsreferenz

Die Outlook Hilfsreferenz enthält konzeptionelle Inhalte und Referenzdokumentation für vier GRUPPEN von APIs, Codebeispiele und ein verteilbares Installationsprogramm, mit dem Entwickler Outlook erweitern und integrieren können. APIs in dieser Referenz werden von Outlook zur Erweiterbarkeit außerhalb des Outlook-Objektmodells verfügbar gemacht. 
  
Wenn Sie gerade erst mit dem Entwickeln von Lösungen für Outlook begonnen haben, finden Sie im Artikel [Auswählen einer API oder Technologie zum Entwickeln von Lösungen für Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) weitere Informationen zu den APIs und Technologien, die am besten zu Ihren Anforderungen passen. 

Spezifische Informationen zum Outlook-Objektmodell finden Sie in der [Outlook VBA-Referenz.](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx) 

Spezifische Informationen zur von Outlook unterstützten Messaging-API (MAPI) finden Sie in der [Outlook MAPI-Referenz.](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx)

## <a name="conceptual"></a>Konzeptionellen 

Die konzeptionelle Diskussion umfasst die folgenden Themen:
  
- [Anti-Spam-Einstellungen](about-anti-spam-settings.md)
    
- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)
    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [Informationen zur Konfliktbehebung für benutzerdefinierte Typen](about-conflict-resolution-for-custom-item-types.md)
    
- [Informationen zum Zeitpunkt der letzten Aktualisierung eines Offlineadressbuchs](about-the-last-update-time-of-an-offline-address-book.md)
    
- [Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [Über Besprechungsanfragen als aktualisierte Informationen und vollständige Aktualisierungen](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [Informationen zum programmgesteuerten Neubasieren von Kalendern für Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (es gibt auch ein weitervertreibbares Installationsprogramm für Kalenderumbasierungstools von Drittanbietern, das seit Outlook 2010 auch für frühere Versionen von Outlook funktioniert. Informationen zum Herunterladen des Installationsprogramms finden Sie [unter Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)
    
- [Informationen zum Beibehalten von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu übernehmen](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Referenz

Der Referenzinhalt umfasst Folgendes:
  
- Die [von Outlook exportierten APIs](about-apis-exported-by-outlook.md) enthalten Funktionen und Datenstrukturen, die ursprünglich für die interne Verwendung implementiert wurden und jetzt für die öffentliche Verwendung verfügbar gemacht werden. 
    
- Die [Kontoverwaltungs-API](about-the-account-management-api.md) bietet Zugriff auf Benutzerkontoinformationen und Benachrichtigungen über Kontoänderungen. 
    
- Die [Data Degradation Layer-API](about-the-data-degradation-layer-api.md) unterstützt Clients, die auf ein Outlook Element in einem bevorzugten Zeichenformat statt im nativen Zeichenformat des Objekts zugreifen. 
    
- Die [Frei/Gebucht-API](about-the-free-busy-api.md) stellt Frei/Gebucht-Statusinformationen zu bestimmten Benutzerkonten innerhalb eines bestimmten Zeitraums bereit. 

## <a name="sample-tasks"></a>Beispielaufgaben

Beispiele für Vorgehensweisen in der Outlook Hilfsreferenz sind:
    
- [Bestimmen Sie, ob ein Outlook-Element geändert, aber nicht gespeichert (Outlook 2013 Hilfs-Referenz) wurde](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Geben Sie an, ob das Bild eines Kontakts in Outlook (Outlook-Zusatzreferenz) angezeigt werden soll](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)
    
In der Referenz für jede API sind die Konstanten, Typdefinitionen und Schnittstellen aufgeführt, die ein Entwickler implementieren muss, um die zusätzliche Funktionalität zu verwenden.
  
> [!NOTE]
> Entwickler müssen diese APIs nur wie in dieser Referenz dokumentiert implementieren. Bestimmte Schnittstellenmember und Methodenparameter werden als Platzhalter benannt, da sie für die interne Verwendung von Outlook reserviert sind und ohne vorherige Ankündigung geändert werden können. 
  

