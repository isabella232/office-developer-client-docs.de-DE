---
title: Übersicht über die MAPI-Funktion
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.localizationpriority: medium
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: 4f1e4e09b6e1b200a8930ae7df7781a8e449539b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59567221"
---
# <a name="mapi-feature-overview"></a>Übersicht über die MAPI-Funktion
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
DIE MAPI verfügt über mehrere wichtige Features, mit denen sie Entwicklern eine konsistente Möglichkeit bietet, nahtlos mit verschiedenen Messagingsystemen zu arbeiten und sie zu verwenden. Diese Features umfassen eine umfassende und offene Programmierschnittstelle sowie Unterstützung für Branchenstandards. 
  
Da mapi eine offene Programmierschnittstelle ist, bietet sie Dienste auf generische Weise, sodass Benutzer alle erforderlichen Anpassungen jetzt und in zukunft hinzufügen können. Die MAPI-Programmierschnittstelle erfüllt die Anforderungen von Clientanwendungen mit unterschiedlichen Messaging-Anforderungen, z. B. eine Textverarbeitungsanwendung, die nur die Möglichkeit zum Senden von Dokumenten erfordert, oder eine Arbeitsgruppenanwendung, die die Möglichkeit zum Freigeben und Speichern verschiedener Datentypen erfordert. Tatsächlich kann jede Anwendung, die Informationen in einem bestimmten Format austauschen oder speichern muss, von der MAPI-Programmierschnittstelle profitieren. Jeder Dienstanbieter kann die Schnittstelle verwenden, um die einzigartigen Features seines Messagingsystems verfügbar zu machen, indem er die Features auswählt, die den Anwendungsbenutzern am meisten Vorteile bieten.
  
MAPI bietet eine Trennung zwischen der Programmierschnittstelle, die von den Front-End-Messaging-Clientanwendungen verwendet wird, und der Programmierschnittstelle, die von den Back-End-Dienstanbietern verwendet wird. Durch das Trennen der Clientschnittstelle vom Dienstanbieter kann eine einzelne Anwendung mehrere Messagingsysteme und mehrere Anwendungen einen einzigen Dienstanbieter verwenden. Jede Komponente funktioniert mit einer gemeinsamen Microsoft Windows-basierten Benutzeroberfläche. Dies ist ein großer Vorteil für die Benutzer. Benutzer können aus einer Vielzahl von Systemen auswählen, je nach ihren Anforderungen zu einem beliebigen Zeitpunkt, und sie können konsistent mit jedem ausgewählten System arbeiten, wodurch eine echte Unabhängigkeit von bestimmten Messagingsystemen gewährleistet wird. 
  
Beispielsweise kann eine einzelne Messagingclientanwendung Nachrichten von einem Fax, Voicemail und einem RSS-Feed empfangen. Nachrichten von allen diesen Systemen können bei der Ankunft an einem einzigen Ort oder in einem universellen Posteingang platziert werden. Eine einzige Anwendung übernimmt alle diese Systeme und verringert die Kosten für Entwicklung, Benutzerschulung und Systemverwaltung. 
  
Durch das Trennen der Clientschnittstelle von der Anbieterschnittstelle werden alle Programmierabhängigkeiten entfernt, die vom Messagingsystem auf die Anwendung angewendet werden und umgekehrt. Entwickler von Clientanwendungen und Dienstanbietern schreiben Code in eine Standardgruppe von MAPI-Features und nicht in eine Vielzahl anwendungsspezifischer oder messagingsystemspezifischer Features. Entwickler konzentrieren sich nur auf ihre Komponente, unabhängig davon, ob es sich um einen Client oder einen Dienstanbieter handelt, und MAPI übernimmt den Rest, wodurch entwicklungszeit und -kosten reduziert werden.
  
Die MAPI-Programmierschnittstelle bietet einen umfassenden Satz von Features. MAPI ist auf den leistungsstarken neuen Markt von Arbeitsgruppenanwendungen ausgerichtet– Anwendungen, die mit verschiedenen Messagingsystemen wie Fax, DEC All-In-1, Voicemail und öffentlichen Kommunikationsdiensten wie AT&T Easylink Services, CompuServe und MCI MAIL kommunizieren. Mit der MAPI-Schnittstelle können Dienstanbieter für alle diese Systeme zur Verfügung gestellt werden. 
  
MAPI-kompatible Objekte sind in ihrer Form mit COM-Objekten (Component Object Model) vergleichbar. COM-Objekte implementieren eine Reihe von Methoden, die zu einer oder mehreren Schnittstellen gehören, oder Sammlungen verwandter Funktionen, die das Verhalten und die Funktionsweise von Objekten in COM definieren. Benutzer greifen nur über Zeiger auf diese Schnittstellen auf COM-Objekte zu.
  
MAPI bietet plattformübergreifende Unterstützung durch Branchenstandards wie SMTP und X.400. Sie können MAPI-Anwendungen auf Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 und Windows XP ausführen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

