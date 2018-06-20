---
title: Arten von Clientanwendungen
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 52ce22a9-3ec2-481c-bb91-7a5bcca817f5
description: 'Letzte �nderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 17b55de84c38deb515dfb528e0ed01306934739d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795763"
---
# <a name="types-of-client-applications"></a>Arten von Clientanwendungen

  
  
**Betrifft**: Outlook 
  
Es gibt hauptsächlich zwei Arten von messaging-Clients:, die Nachrichten zwischen Personen (IPM) behandelt, und die Verarbeitung von Nachrichten prozessübergreifenden Kommunikation (IPK). In dieser Typen kann messaging-Clientanwendungen wie folgt kategorisiert:
  
- Zwischen Personen
    
- Person-zu-Computer
    
- Computer-zu-person
    
- Computer-zu-Computer
    
- Kombination von Personen und Computern
    
Person Applications umfassen eine Person, die den Austausch von Nachrichten und eine andere Person reagieren initiieren. Diese Kategorie von Anwendungen umfasst herkömmlichen e-Mail-Programmen sowie weitere strukturierte Austausch wie dokumentgenehmigung routing oder Ausgaben.
  
Person-zu-Computer-Applikationen umfassen eine Person, die den Austausch von Nachrichten und ein Computer reagiert initiieren. Zu dieser Kategorie gehören, e-Mail an, beispielsweise eine Datenbankabfrage übermitteln oder Abonnieren einer Mailingliste verwenden.
  
Computer-zu-Person Applications umfassen ein Computers, der den Austausch von Nachrichten und eine Person reagieren initiieren. Zu dieser Kategorie gehören Applications, von die Dokumente wie Newsfeeds und Umfragen Opinion verteilt.
  
Computer-zu-Computer-Applikationen umfassen ein Computers, der den Austausch von Nachrichten und ein Computer reagiert initiieren. Zu dieser Kategorie gehören Anwendungen wie Link Heartbeat-Überwachung und Verzeichnis und Datenbank-Replikation.
  
Die letzte Kategorie eine Kombination von Personen und Computern, umfasst ein komplexeres Szenario. Zu dieser Kategorie gehören Anwendungen, die nicht notwendigerweise Nachrichten zwischen Absender und Empfänger übertragen werden. Stattdessen können sie diese direkt in einem öffentlichen Ordner oder in einem Website Forum unterstützt durch einen Nachrichtenspeicher buchen. Die Nachrichten können von anderen Leser, ein Administrator oder ein Agent Software klicken Sie dann bei Bedarf genutzt werden.
  
Wenn Sie eine Person-Anwendung, Computer-zu-Person-Anwendung oder eine Anwendung, die Nachrichten an Öffentliche Foren zurücksendet schreiben, Entwerfen Sie Ihre Anwendung senden und Empfangen von Nachrichten IPM. Wenn Sie eine Person-zu-Computer oder Computer-zu-Computer-Anwendung schreiben, können sie für konzipiert IPK Nachrichten senden und empfangen. Eine beliebige Anwendung, die die Interaktion eines Benutzers human erfordert muss IPM-Nachrichten unterstützen. Clientanwendungen, die häufig von Benutzern und Computern in einer Vielzahl von Szenarien betreffen müssen IPM und IPK Nachrichten unterstützt. Der einzige Unterschied zwischen den zwei Klassen ist, dass IPM-Nachrichten in einen Nachrichtenspeicher für Benutzer von messaging-Clients angezeigt werden, während IPK Nachrichten in der Regel nicht an die Client-Anwendungsbenutzer sichtbar sind. 
  
Statt beschränken Ihre Nachrichten an die Funktionen von MAPI-Contain IPM und IPK, können Sie anpassen und erweitern diese Klassen, indem Sie neue IPM oder IPK Unterklassen erstellen. Erstellen von Nachricht Unterklassen umfasst gleichzeitig neue Nachrichtenklassen, die von der übergeordneten Klassen erben. Beispielsweise wenn die Person Anwendung Customer Relationship Management unterstützt, können Sie Unterklasse der IPM übergeordneten Klasse durch die Definition einer IPM. Contact.Customer-Klasse und Erstellen von Eigenschaften, die einen Kunden zu beschreiben. Zusätzlich zur Unterstützung von diese benutzerdefinierten Eigenschaften, Ihre IPM. Contact.Customer Nachrichten werden vom IPM-Nachrichten, die alle unterstützten Eigenschaften erben.
  

