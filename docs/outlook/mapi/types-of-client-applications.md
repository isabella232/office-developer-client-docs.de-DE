---
title: Typen von Clientanwendungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4e3aaf8de7726ca75816105fbe81b2019fcaa107
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578452"
---
# <a name="types-of-client-applications"></a>Typen von Clientanwendungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt in erster Linie zwei Arten von Messagingclients: diejenigen, die zwischenmenschliche Nachrichten (Interpersonal Messages, IPM) behandeln, und diejenigen, die IPC-Nachrichten (Interprocess Communication) verarbeiten. Innerhalb dieser Typen können Messagingclientanwendungen wie folgt kategorisiert werden:
  
- Von Person zu Person
    
- Person-zu-Computer
    
- Computer-zu-Person
    
- Computer-zu-Computer
    
- Kombination aus Personen und Computern
    
Personen-zu-Person-Anwendungen umfassen eine Person, die den Austausch von Nachrichten initiiert, und eine andere Person reagiert. Diese Kategorie von Anwendungen umfasst herkömmliche E-Mail-Anwendungen sowie strukturierteren Austausch, z. B. Dokumentrouting oder Spesengenehmigung.
  
Bei Anwendungen zwischen Personen handelt es sich um eine Person, die den Austausch von Nachrichten initiiert, und ein Computer reagiert. Diese Kategorie umfasst Anwendungen, die E-Mails verwenden, um z. B. eine Datenbankabfrage zu übermitteln oder eine Mailingliste zu abonnieren.
  
Computer-zu-Person-Anwendungen umfassen einen Computer, der den Austausch von Nachrichten initiiert, und eine Person, die antwortet. Diese Kategorie umfasst Anwendungen, die Dokumente verteilen, z. B. Newsfeeds und Meinungsumfragen.
  
Computer-zu-Computer-Anwendungen umfassen einen Computer, der den Austausch von Nachrichten initiiert, und ein Computer reagiert. Diese Kategorie umfasst Anwendungen wie die Überwachung des Verbindungstakts sowie die Verzeichnis- und Datenbankreplikation.
  
Die letzte Kategorie, eine Mischung aus Personen und Computern, umfasst ein komplexeres Szenario. Diese Kategorie umfasst Anwendungen, die nicht notwendigerweise Nachrichten zwischen Absendern und Empfängern übertragen. Stattdessen können sie sie direkt in einem öffentlichen Ordner oder in einem Websiteforum veröffentlichen, das von einem Nachrichtenspeicher unterstützt wird. Die Nachrichten können dann bei Bedarf von anderen Lesern, einem Administrator oder einem Software-Agent genutzt werden.
  
Wenn Sie eine Persönliche-zu-Person-Anwendung, eine Computer-zu-Person-Anwendung oder eine Anwendung schreiben, die Nachrichten in öffentlichen Foren sendet, entwerfen Sie Ihre Anwendung so, dass IPM-Nachrichten gesendet und empfangen werden. Wenn Sie eine Computer-zu-Computer- oder Computer-zu-Computer-Anwendung schreiben, kann sie so konzipiert werden, dass IPC-Nachrichten gesendet und empfangen werden. Jede Anwendung, die die Interaktion eines menschlichen Benutzers erfordert, muss IPM-Nachrichten unterstützen. Anwendungen, an denen Personen und Computer in einer Vielzahl von Szenarien beteiligt sind, müssen häufig SOWOHL IPM- als auch IPC-Nachrichten unterstützen. Der einzige echte Unterschied zwischen den beiden Klassen besteht darin, dass IPM-Nachrichten in einem Nachrichtenspeicher für Benutzer von Messagingclients sichtbar sind, während IPC-Nachrichten in der Regel für die Benutzer der Clientanwendung nicht sichtbar sind. 
  
Anstatt Ihre Nachrichten auf die Von den MAPI-Superklassen, IPM und IPC bereitgestellten Funktionen zu beschränken, können Sie diese Klassen anpassen und verbessern, indem Sie neue IPM- oder IPC-Unterklassen erstellen. Das Erstellen von Nachrichtenunterklassen umfasst das Erfinden neuer Nachrichtenklassen, die von den Oberklassen erben. Wenn Ihre Persönliche-zu-Person-Anwendung beispielsweise auf die Verwaltung von Kundenbeziehungen spezialisiert ist, können Sie die IPM-Oberklasse unterstufen, indem Sie ein IPM definieren. Contact.Customer-Klasse und Erstellen von Eigenschaften, die einen Kunden beschreiben. Zusätzlich zur Unterstützung dieser benutzerdefinierten Eigenschaften unterstützt Ihr IPM. Contact.Customer-Nachrichten erben die Eigenschaften, die von allen IPM-Nachrichten unterstützt werden.
  

