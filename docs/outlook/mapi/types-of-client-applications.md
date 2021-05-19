---
title: Typen von Clientanwendungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 167710243c61a7226375b88977c94ff4a517c1c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417056"
---
# <a name="types-of-client-applications"></a>Typen von Clientanwendungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt in erster Linie zwei Arten von Messagingclients: diejenigen, die zwischenpersönliche Nachrichten (IPM) behandeln, und solche, die Interprocess Communication (IPC)-Nachrichten verarbeiten. Innerhalb dieser Typen können Messagingclientanwendungen wie folgt kategorisiert werden:
  
- Person-to-Person
    
- Person-zu-Computer
    
- Maschine-zu-Person
    
- Computer-zu-Maschine
    
- Mischung aus Personen und Computern
    
Bei den Persönlich-zu-Person-Anwendungen geht es um eine Person, die den Austausch von Nachrichten initiiert, und eine andere Person, die antwortet. Diese Kategorie von Anwendungen umfasst herkömmliche E-Mail-Anwendungen sowie strukturiertere Austauschprogramme wie Dokumentenrouting oder Spesengenehmigung.
  
Bei den Von-Computer-Zu-Computer-Anwendungen geht es um eine Person, die den Austausch von Nachrichten initiiert, und ein Computer, der reagiert. Diese Kategorie umfasst Anwendungen, die E-Mails verwenden, um z. B. eine Datenbankabfrage zu senden oder eine Mailingliste zu abonnieren.
  
Computer-zu-Person-Anwendungen umfassen einen Computer, der den Austausch von Nachrichten initiiert, und eine Person, die reagiert. Diese Kategorie umfasst Anwendungen, die Dokumente wie Newsfeeds und Meinungsumfragen verteilen.
  
Computer-zu-Computer-Anwendungen umfassen einen Computer, der den Austausch von Nachrichten initiiert, und ein Computer reagiert. Diese Kategorie umfasst Anwendungen wie die Überwachung des Takts von Links sowie die Verzeichnis- und Datenbankreplikation.
  
Die letzte Kategorie, eine Mischung aus Personen und Computern, umfasst ein komplexeres Szenario. Diese Kategorie umfasst Anwendungen, die nicht unbedingt Nachrichten zwischen Absendern und Empfängern übertragen. Stattdessen können sie sie direkt in einem öffentlichen Ordner oder in einem Websiteforum posten, das von einem Nachrichtenspeicher unterstützt wird. Die Nachrichten können dann bei Bedarf von anderen Lesern, einem Administrator oder einem Software-Agent genutzt werden.
  
Wenn Sie eine persönliche Anwendung, eine Computer-zu-Person-Anwendung oder eine Anwendung schreiben, die Nachrichten in öffentlichen Foren postet, entwerfen Sie Ihre Anwendung so, dass SIE IPM-Nachrichten sendet und erhält. Wenn Sie eine Von-Computer- oder Computer-zu-Maschine-Anwendung schreiben, kann sie für das Senden und Empfangen von IPC-Nachrichten konzipiert werden. Jede Anwendung, die die Interaktion eines menschlichen Benutzers erfordert, muss IPM-Nachrichten unterstützen. Anwendungen, die Sowohl Personen als auch Computer in einer Vielzahl von Szenarien betreffen, müssen häufig SOWOHL IPM- als auch IPC-Nachrichten unterstützen. Der einzige tatsächliche Unterschied zwischen den beiden Klassen besteht in der Sichtbar nung von IPM-Nachrichten in einem Nachrichtenspeicher für Benutzer von Messagingclients, während IPC-Nachrichten in der Regel für die Clientanwendungsbenutzer nicht sichtbar sind. 
  
Anstatt Ihre Nachrichten auf die Funktionen der MAPI-Superklassen IPM und IPC zu beschränken, können Sie diese Klassen anpassen und verbessern, indem Sie neue IPM- oder IPC-Unterklassen erstellen. Das Erstellen von Nachrichtenunterklassen umfasst das Erfinden neuer Nachrichtenklassen, die von den Übergeordneten Klassen erben. Wenn sich Ihre Persönliche-zu-Person-Anwendung beispielsweise auf die Verwaltung von Kundenbeziehungen spezialisiert hat, können Sie die IPM-Superklasse unterklassen, indem Sie ein IPM definieren. Contact.Customer-Klasse, und erstellen Sie Eigenschaften, die einen Kunden beschreiben. Zusätzlich zur Unterstützung dieser benutzerdefinierten Eigenschaften unterstützt Ihr IPM. Contact.Customer-Nachrichten erben die Eigenschaften, die von allen IPM-Nachrichten unterstützt werden.
  

