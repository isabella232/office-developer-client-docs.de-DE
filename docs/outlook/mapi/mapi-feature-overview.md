---
title: MAPI-Features (Übersicht)
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 034f3dd8bc68462348bc92a8acf2904ab66fc798
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575609"
---
# <a name="mapi-feature-overview"></a>MAPI-Features (Übersicht)
 
**Betrifft**: Outlook 2013 | Outlook 2016 
  
MAPI hat mehrere wichtige Features, mit denen sie einheitlich für Entwickler zu arbeiten mit verschiedenen Messagingsystemen nahtlos Weise bereitstellen. Diese Features enthalten einen umfassenden und Programmierschnittstelle öffnen und Unterstützung für Industriestandards. 
  
Da MAPI eine Programmierschnittstelle geöffnet ist, bietet es Dienste in eine generische Möglichkeit, Benutzern ermöglichen, alle erforderlichen Anpassung jetzt und in Zukunft hinzuzufügen. Die MAPI-Programmierschnittstelle erfüllt die Anforderungen von Clientanwendungen mit unterschiedlichen Messaginganforderungen, beispielsweise ein Textverarbeitungsdokument-Anwendung, die nur die Möglichkeit zum Senden von Dokumenten erfordert oder eine Arbeitsgruppe-Anwendung, die Möglichkeit zur Freigabe erfordert, und unterschiedliche Arten von Daten zu speichern. Tatsächlich kann jede Anwendung, die entweder austauschen oder Speichern von Informationen in einem bestimmten Format muss die MAPI-Programmierschnittstelle nutzen. Die Schnittstelle können alle Dienstanbieter verfügbar machen einzigartigen Merkmale der messaging-System Diese Features, die den Benutzern am meisten profitieren bereitstellen auswählen.
  
MAPI bietet Trennung zwischen der Programmierschnittstelle von den Front-End-messaging-Clientanwendungen verwendet und die Programmierschnittstelle Anbietern Back-End-Dienst verwendet wird. Trennen die Client-Schnittstelle von der Dienstanbieter ermöglicht eine Anwendung zu mehreren Messagingsystemen verwenden und mehrere Clientanwendungen auf einen einzelnen Dienstanbieter verwenden. Jede Komponente funktioniert mit einer gemeinsamen Microsoft Windows-basierten-Benutzeroberfläche. Dies ist ein großer Vorteil für Benutzer. Benutzer können aus einer Vielzahl von Systemen, je nach ihren Anforderungen können Sie jederzeit eine, auswählen und können arbeiten ständig mit jedem ausgewählten System, wodurch true Unabhängigkeit von bestimmten messaging-Systeme. 
  
Eine einzelne messaging Clientanwendung kann beispielsweise Nachrichten von Fax, Voicemail und einen RSS-Feed erhalten. Nachrichten von allen Systemen können in einem einzigen Speicherort oder universelle Posteingang auf hinzukommen platziert werden. Mit einer einzigen Anwendung, die alle diese Systeme behandeln verringert die Kosten für die Entwicklung, benutzerschulungen und Systemadministration. 
  
Trennen die Client-Benutzeroberfläche von Anbieterschnittstelle entfernt programming Abhängigkeiten für die Anwendung von messaging-System und umgekehrt platziert. Entwickler von Clientanwendungen und Dienstanbieter schreiben Sie Code eine Reihe von MAPI-Features, sondern eine Reihe von anwendungsspezifischen oder messaging-System-spezifischen Features. Entwickler konzentrieren Sie sich nur auf ihre Komponente, ob es ein Client oder Dienstanbieter ist und MAPI behandelt die restlichen Reduzieren der Entwicklungszeit und Kosten.
  
Die MAPI-Programmierschnittstelle bietet einen umfassenden Satz an Funktionen. MAPI richtet sich an die leistungsstarken neuen Markt Arbeitsgruppe Anwendungstypen – Anwendungen, die Kommunikation mit solchen verschiedenen Messagingsystemen als Fax, Dez All-In-1, Voicemail, und öffentliche Kommunikationsdienste wie AT & T Easylink Dienste, CompuServe und MCI E-MAIL-NACHRICHTEN. Die MAPI-Schnittstelle ermöglicht Dienstanbieter für alle diese Systeme zur Verfügung gestellt werden. 
  
MAPI-kompatible Objekte ähneln im Formular an Component Object Model (COM)-Objekten. COM-Objekten implementieren, eine Reihe von Methoden, die eine oder mehrere Schnittstellen angehören, oder Sammlungen verwandter Funktionen, die definieren, wie Objekte Verhalten und Betrieb in COM. Benutzer greifen COM-Objekte nur über Zeiger auf diese Schnittstellen auf.
  
MAPI bietet plattformübergreifende Unterstützung durch eine solche Branchenstandards als SMTP- und x. 400. Sie können die MAPI-Anwendungen auf Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 und Windows XP ausführen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

