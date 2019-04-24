---
title: Willkommen bei der Outlook-hilfsReferenz
manager: soliver
ms.date: 09/10/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 2e48a625-b3f7-9fd0-253e-fe12a1aca446
description: Die Outlook-hilfsReferenz enthält konzeptionelle Inhalte und Referenzdokumentation für vier Gruppen von APIs, Codebeispielen und einem Redistributable Installer, mit denen Entwickler Outlook erweitern und integrieren können. APIs in dieser Referenz werden von Outlook zur Erweiterbarkeit außerhalb des Outlook-Objektmodells zur Verfügung gestellt.
ms.openlocfilehash: 445d35c12e4c8984d47adcef3ecf50ebd881875b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328981"
---
# <a name="welcome-to-the-outlook-auxiliary-reference"></a>Willkommen bei der Outlook-hilfsReferenz

Die Outlook-hilfsReferenz enthält konzeptionelle Inhalte und Referenzdokumentation für vier Gruppen von APIs, Codebeispielen und einem Redistributable Installer, mit denen Entwickler Outlook erweitern und integrieren können. APIs in dieser Referenz werden von Outlook zur Erweiterbarkeit außerhalb des Outlook-Objektmodells zur Verfügung gestellt. 
  
Wenn Sie gerade erst mit dem Entwickeln von Lösungen für Outlook begonnen haben, finden Sie im Artikel [Auswählen einer API oder Technologie zum Entwickeln von Lösungen für Outlook](../selecting-an-api-or-technology-for-developing-solutions-for-outlook.md) weitere Informationen zu den APIs und Technologien, die am besten zu Ihren Anforderungen passen. 

Spezifische Informationen zum Outlook-Objektmodell finden Sie in der [Outlook-VBA-Referenz](https://msdn.microsoft.com/library/75e4ad96-62a2-49d2-bc51-48ceab50634c%28Office.15%29.aspx). 

Spezifische Informationen zur Messaging-API (MAPI), die von Outlook unterstützt werden, finden Sie in der [Outlook-MAPI-Referenz](https://msdn.microsoft.com/library/3d980b86-7001-4869-9780-121c6bfc7275%28Office.15%29.aspx).

## <a name="conceptual"></a>Konzeptionellen 

Die konzeptionelle Diskussion umfasst die folgenden Themen:
  
- [Anti-Spam-Einstellungen](about-anti-spam-settings.md)
    
- [Verwalten des Nachrichtendownloads für POP3-Konten](managing-message-downloads-for-pop3-accounts.md)
    
- [Suchen den Nachrichten-Downloadverlauf für ein POP3-Konto](locating-the-message-download-history-for-a-pop3-account.md)
    
- [Analysieren den Nachrichten-Downloadverlauf für ein POP3-Konto](parsing-the-message-download-history-for-a-pop3-account.md)
    
- [Informationen zur Konfliktbehebung für benutzerdefinierte Typen](about-conflict-resolution-for-custom-item-types.md)
    
- [Informationen zum letzten Aktualisierungszeitpunkt eines Offline Adressbuchs](about-the-last-update-time-of-an-offline-address-book.md)
    
- [Informationen zum Registrieren einer neuen Domäne für die automatische Konfiguration](about-registering-a-new-domain-for-automatic-configuration.md)
    
- [Über Besprechungsanfragen als aktualisierte Informationen und vollständige Aktualisierungen](about-meeting-requests-as-informational-updates-and-full-updates.md)
    
- [Informationen zum programmgesteuerten Kalender für Sommerzeit](about-rebasing-calendars-programmatically-for-daylight-saving-time.md) (Es gibt auch einen Redistributable Installer für Drittanbieter-Kalender-Tools, die für frühere Versionen von Outlook auch funktioniert, seit Outlook 2010. Informationen zum Herunterladen des Installationsprogramms finden Sie unter [Outlook 2010: Auxiliary Reference redistributAble Installer and Header File for](https://www.microsoft.com/downloads/details.aspx?FamilyID=77748863-4352-4b99-ae57-1d4ae803983b)rePlaning Calendars.)
    
- [Zum Speichern von TZDEFINITION in einen Stream zu einer binären Eigenschaft anvertrauen](about-persisting-tzdefinition-to-a-stream-to-commit-to-a-binary-property.md)

## <a name="reference"></a>Referenz

Der Referenzinhalt umfasst Folgendes:
  
- Zu den [von Outlook exportiertEn APIs](about-apis-exported-by-outlook.md) gehören Funktionen und Datenstrukturen, die ursprünglich für die interne Verwendung implementiert wurden und nun für die öffentliche Verwendung verfügbar gemacht werden. 
    
- Die [Account Management-API](about-the-account-management-api.md) bietet Zugriff auf Benutzerkontoinformationen und Benachrichtigungen über Kontoänderungen. 
    
- Die [API für die Daten Degradations Schicht](about-the-data-degradation-layer-api.md) unterstützt Clients, die auf ein Outlook-Element in einem bevorzugten Zeichenformat und nicht auf das systemeigene Zeichenformat des Objekts zugreifen. 
    
- Die [Frei/Gebucht-API](about-the-free-busy-api.md) bietet frei/gebucht-Statusinformationen zu bestimmten Benutzerkonten innerhalb eines bestimmten Zeitintervalls. 

## <a name="sample-tasks"></a>Beispielaufgaben

Beispiele für Vorgehensweise in der Outlook-hilfsReferenz:
    
- [Bestimmen Sie, ob ein Outlook-Element geändert, aber nicht gespeichert (Outlook 2013 Hilfs-Referenz) wurde](how-to-determine-if-outlook-item-has-been-modified-but-not-saved.md)
    
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZDEFINITION-Struktur](how-to-parse-stream-from-binary-property-to-read-tzdefinition-structure.md)
    
- [Analysieren eines Streams aus einer binären Eigenschaft zum Lesen der TZREG-Struktur](how-to-parse-a-stream-from-a-binary-property-to-read-the-tzreg-structure.md)
    
- [Lesen von Zeitzoneneigenschaften aus einem Termin](how-to-read-time-zone-properties-from-an-appointment.md)
    
- [Geben Sie an, ob das Bild eines Kontakts in Outlook (Outlook-Zusatzreferenz) angezeigt werden soll](https://msdn.microsoft.com/library/office/gg262879.aspx)
    
- [Verwenden von relativer Zeit zum Zugriff auf Frei/Gebucht-Daten](how-to-use-relative-time-to-access-free-busy-data.md)
    
Die Referenz für jede API listet die Konstanten, Typdefinitionen und Schnittstellen auf, die ein Entwickler implementieren muss, um die zusätzliche Funktionalität zu verwenden.
  
> [!NOTE]
> Entwickler müssen diese APIs nur wie in dieser Referenz beschrieben implementieren. Bestimmte Schnittstellenmember und Methodenparameter werden als Platzhalter bezeichnet, da Sie für die interne Verwendung von Outlook reserviert sind und ohne vorherige Ankündigung geändert werden können. 
  

