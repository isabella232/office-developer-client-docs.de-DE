---
title: Arten von Client Anwendungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 167710243c61a7226375b88977c94ff4a517c1c3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356560"
---
# <a name="types-of-client-applications"></a>Arten von Client Anwendungen

  
  
**Gilt für**: Outlook 2013 | Outlook 2016 
  
Es gibt in erster Linie zwei Arten von Messagingclients: solche, die zwischenmenschliche Nachrichten (IPM) und die Interprocess Communication (IPC)-Nachrichten verarbeiten. Innerhalb dieser Typen können Messaging-Clientanwendungen wie folgt kategorisiert werden:
  
- Person-zu-Person
    
- Person-zu-Maschine
    
- Computer-zu-Person
    
- Machine-to-Machine
    
- Kombination aus Personen und Maschinen
    
Bei der Person-zu-Person-Anwendung handelt es sich um eine Person, die den Austausch von Nachrichten initiiert und eine andere Person reagiert. Diese Anwendungskategorie umfasst herkömmliche e-Mail-Anwendungen sowie strukturiertere Exchange-Dokumente wie Dokumentweiterleitung oder Spesen Genehmigung.
  
Bei der Person-zu-Machine-Anwendung handelt es sich um eine Person, die den Austausch von Nachrichten initiiert und eine Maschine reagiert. Diese Kategorie enthält Anwendungen, die e-Mails verwenden, um beispielsweise eine Datenbankabfrage zu übermitteln oder eine Mailingliste zu abonnieren.
  
Computer-zu-Person-Anwendungen umfassen einen Computer, der den Austausch von Nachrichten initiiert und eine Person reagiert. Diese Kategorie enthält Anwendungen, die Dokumente wie Nachrichten Feeds und Meinungsumfragen verteilen.
  
Machine-to-Machine-Anwendungen umfassen einen Computer, der den Austausch von Nachrichten initiiert, und eine Maschine reagiert. Diese Kategorie umfasst Anwendungen wie die Überwachung von Link Takten und die Verzeichnis-und Datenbankreplikation.
  
Die letzte Kategorie, eine Kombination aus Personen und Maschinen, beinhaltet ein komplexeres Szenario. Diese Kategorie enthält Anwendungen, die nicht notwendigerweise Nachrichten zwischen Absendern und Empfängern übertragen. Stattdessen können Sie diese direkt in einem öffentlichen Ordner oder in einem von einem Nachrichtenspeicher unterstützten Website-Forum veröffentlichen. Die Nachrichten können dann bei Bedarf von anderen Lesern, einem Administrator oder einem Software-Agent verwendet werden.
  
Wenn Sie eine Person-zu-Person-Anwendung, eine Computer-zu-Person-Anwendung oder eine Anwendung schreiben, die Nachrichten in öffentliche Foren übermittelt, entwerfen Sie Ihre Anwendung, um IPM-Nachrichten zu senden und zu empfangen. Wenn Sie eine Person-zu-Maschine-oder Maschine-zu-Maschine-Anwendung schreiben, kann Sie zum Senden und empfangen von IPC-Nachrichten entwickelt werden. Jede Anwendung, die die Interaktion eines menschlichen Benutzers erfordert, muss IPM-Nachrichten unterstützen. Anwendungen, die sowohl Personen als auch Computer in einer Vielzahl von Szenarien einbeziehen, müssen häufig sowohl IPM-als auch IPC-Nachrichten unterstützen. Der einzige wirkliche Unterschied zwischen den beiden Klassen besteht darin, dass IPM-Nachrichten in einem Nachrichtenspeicher für Benutzer von Messagingclients sichtbar sind, während IPC-Nachrichten für die Client Anwendungsbenutzer normalerweise nicht sichtbar sind. 
  
Anstatt Ihre Nachrichten auf die von der MAPI und IPC bereitgestellten Funktionen einzuschränken, können Sie diese Klassen anpassen und erweitern, indem Sie neue IPM-oder IPC-Unterklassen erstellen. Das Erstellen von Nachrichten Unterklassen umfasst das erfinden neuer Nachrichtenklassen, die von den SuperClasses erben. Wenn sich Ihre Person-zu-Person-Anwendung beispielsweise auf die Verwaltung von Kundenbeziehungen spezialisiert hat, können Sie die IPM-Oberklasse durch Definieren einer IPM-Klasse Unterklassen. Contact. Customer-Klasse und Erstellen von Eigenschaften, die einen Kunden beschreiben. Zusätzlich zur Unterstützung dieser benutzerdefinierten Eigenschaften kann Ihre IPM. Contact. Customer-Nachrichten erben die von allen IPM-Nachrichten unterstützten Eigenschaften.
  

