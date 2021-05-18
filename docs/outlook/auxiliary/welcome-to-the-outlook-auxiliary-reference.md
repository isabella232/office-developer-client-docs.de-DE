---
title: Willkommen bei der Outlook-Hilfsreferenz
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Die Outlook-Hilfsreferenz enthält konzeptionelle Inhalts- und Referenzdokumentationen für vier Gruppen von APIs, Codebeispiele und ein umverteiltes Installationsprogramm, das Entwicklern die Erweiterung und Integration in Outlook. APIs in diesem Verweis werden von Outlook zur Erweiterbarkeit außerhalb des Outlook verfügbar gemacht.
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328981"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Willkommen bei der Outlook-Hilfsreferenz

Die Outlook-Hilfsreferenz enthält konzeptionelle Inhalts- und Referenzdokumentationen für vier Gruppen von APIs, Codebeispiele und ein umverteiltes Installationsprogramm, das Entwicklern die Erweiterung und Integration in Outlook. APIs in diesem Verweis werden von Outlook zur Erweiterbarkeit außerhalb des Outlook verfügbar gemacht. 
  
Wenn Sie gerade erst mit dem Entwickeln von Lösungen für Outlook begonnen haben, finden Sie im Artikel [Auswählen einer API oder Technologie zum Entwickeln von Lösungen für Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) weitere Informationen zu den APIs und Technologien, die am besten zu Ihren Anforderungen passen. 

Spezifische Informationen zum Outlook finden Sie unter [Outlook VBA-Referenz](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx). 

Spezifische Informationen zur messaging API (MAPI), die von Outlook unterstützt wird, finden Sie [unter Outlook MAPI Reference](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).

## <a name="conceptual"></a>Konzeptionell 

Die konzeptionelle Diskussion umfasst die folgenden Themen:
  
- [Anti-Spam-Einstellungen](about-anti-spam-settings.md)
    
- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)
    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [Informationen zur Konfliktbehebung für benutzerdefinierte Typen](about-conflict-resolution-for-custom-item-types.md)
    
- [Informationen zur letzten Aktualisierungszeit eines Offlineadressbuchs](about-the-last-update-time-of-an-offline-address-book.md)
    
- [Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [Über Besprechungsanfragen als aktualisierte Informationen und vollständige Aktualisierungen](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [Informationen zum](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) programmgesteuerten Neubasieren von Kalendern für Sommerzeit (Es gibt auch ein umverteiltes Installationsprogramm für Tools zum Neubasieren von Kalendern von Drittanbietern, das auch für frühere Versionen von Outlook funktioniert, seit Outlook 2010. Informationen zum Herunterladen des Installationsprogramms finden Sie [unter Outlook 2010: Auxiliary Reference Redistributable Installer and Header File for Rebasing Calendars](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b).)
    
- [Informationen zum Beibehalten von TZDEFINITION in einem Stream, um eine binäre Eigenschaft zu übernehmen](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Referenz

Der Referenzinhalt umfasst Folgendes:
  
- Die [apIs,](about-apis-exported-by-outlook.md) die von Outlook exportiert werden, enthalten Funktionen und Datenstrukturen, die ursprünglich für die interne Verwendung implementiert wurden und jetzt für die öffentliche Verwendung verfügbar gemacht werden. 
    
- Die [Kontoverwaltungs-API](about-the-account-management-api.md) bietet Zugriff auf Benutzerkontoinformationen und Benachrichtigungen über Kontoänderungen. 
    
- Die [Data Degradation Layer-API](about-the-data-degradation-layer-api.md) unterstützt Clients, die auf ein Outlook in einem bevorzugten Zeichenformat zugreifen und nicht auf das systemeigene Zeichenformat des Objekts. 
    
- Die [Frei/Gebucht-API](about-the-free-busy-api.md) stellt Frei/Gebucht-Statusinformationen zu bestimmten Benutzerkonten innerhalb eines bestimmten Zeitbereichs bereit. 

## <a name="sample-tasks"></a>Beispielaufgaben

Beispiele für How-to-Aufgaben in Outlook-Hilfsreferenz sind:
    
- [Bestimmen Sie, ob ein Outlook-Element geändert, aber nicht gespeichert (Outlook 2013 Hilfs-Referenz) wurde](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Geben Sie an, ob das Bild eines Kontakts in Outlook (Outlook-Zusatzreferenz) angezeigt werden soll](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)
    
Der Verweis für jede API enthält die Konstanten, Typdefinitionen und Schnittstellen, die ein Entwickler implementieren muss, um die zusätzlichen Funktionen nutzen zu können.
  
> [!NOTE]
> Entwickler müssen diese APIs nur so implementieren, wie in diesem Verweis dokumentiert. Bestimmte Schnittstellenm member und Methodenparameter werden als Platzhalter bezeichnet, da sie für die interne Verwendung von Outlook reserviert sind und ohne vorherige Ankündigung geändert werden können. 
  

