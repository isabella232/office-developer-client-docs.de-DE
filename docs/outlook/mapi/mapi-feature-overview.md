---
title: Übersicht über das MAPI-Feature
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 22cf56c5-2804-40a8-99e6-a6d127897720
description: 'Letzte Änderung: Samstag, 23. Juli 2011'
ms.openlocfilehash: b1087f5156ad79b20eb31ef55c0388ffd82e1601
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416923"
---
# <a name="mapi-feature-overview"></a>Übersicht über das MAPI-Feature
 
**Gilt für**: Outlook 2013 | Outlook 2016 
  
MAPI verfügt über mehrere Schlüsselfeatures, die es Entwicklern ermöglichen, nahtlos mit verschiedenen Messagingsystemen zu arbeiten und diese zu verwenden. Diese Features umfassen eine umfassende und offene Programmierschnittstelle sowie Unterstützung für Branchenstandards. 
  
Da MAPI eine offene Programmierschnittstelle ist, stellt sie Dienste auf generische Weise bereit, sodass Benutzer jetzt und in Zukunft alle erforderlichen Anpassungen hinzufügen können. Die MAPI-Programmierschnittstelle erfüllt die Anforderungen von Clientanwendungen mit unterschiedlichen Messaginganforderungen, z. B. einer Textverarbeitungsanwendung, die nur die Möglichkeit zum Senden von Dokumenten erfordert, oder einer Arbeitsgruppenanwendung, die die Möglichkeit zum Freigeben und Speichern verschiedener Datentypen erfordert. Tatsächlich kann jede Anwendung, die Informationen in einem bestimmten Format austauschen oder speichern muss, von der MAPI-Programmierschnittstelle profitieren. Jeder Dienstanbieter kann die Schnittstelle verwenden, um die einzigartigen Features seines Messagingsystems verfügbar zu machen, indem er die Features aus wählt, die den Anwendungsbenutzern den größten Nutzen bieten.
  
MAPI bietet eine Trennung zwischen der Programmierschnittstelle, die von den Front-End-Messaging-Clientanwendungen verwendet wird, und der Programmierschnittstelle, die von den Back-End-Dienstanbietern verwendet wird. Durch das Trennen der Clientschnittstelle vom Dienstanbieter kann eine einzelne Anwendung mehrere Messagingsysteme und mehrere Anwendungen verwenden, um einen einzelnen Dienstanbieter zu verwenden. Jede Komponente funktioniert mit einer Windows basierten Benutzeroberfläche von Microsoft. Dies ist ein großer Vorteil für Benutzer. Benutzer können je nach Ihren Anforderungen jederzeit aus einer Vielzahl von Systemen auswählen und konsistent mit jedem ausgewählten System zusammenarbeiten, wodurch eine echte Unabhängigkeit von bestimmten Messagingsystemen ermöglicht wird. 
  
Beispielsweise kann eine einzelne Messagingclientanwendung Nachrichten von einem Fax, Voicemail und einem RSS-Feed empfangen. Nachrichten von allen diesen Systemen können bei der Ankunft an einem einzigen Ort oder an einem universellen Posteingang platziert werden. Wenn sie alle diese Systeme mit einer einzigen Anwendung behandeln, werden die Kosten für Entwicklung, Benutzerschulung und Systemverwaltung geringer. 
  
Durch das Trennen der Clientschnittstelle von der Anbieterschnittstelle werden alle Programmierabhängigkeiten entfernt, die von dem Messagingsystem auf die Anwendung gesetzt werden, und umgekehrt. Entwickler von Clientanwendungen und Dienstanbietern schreiben Code in einen Standardsatz von MAPI-Features und nicht in eine Vielzahl anwendungsspezifischer oder messagingsystemspezifischer Features. Entwickler konzentrieren sich nur auf ihre Komponente, unabhängig davon, ob es sich um einen Client oder Dienstanbieter handelt, und MAPI übernimmt den Rest, wodurch Entwicklungszeit und -kosten reduziert werden.
  
Die MAPI-Programmierschnittstelle bietet eine umfassende Reihe von Features. MAPI richtet sich an den leistungsstarken neuen Markt von Arbeitsgruppenanwendungen – Anwendungen, die mit so unterschiedlichen Messagingsystemen wie Fax, DEC All-In-1, Voicemail und öffentlichen Kommunikationsdiensten wie AT&T Easylink Services, CompuServe und MCI MAIL kommunizieren. Mit der MAPI-Schnittstelle können Dienstanbieter für alle diese Systeme verfügbar gemacht werden. 
  
MAPI-kompatible Objekte ähneln in der Form den Objekten des Component Object Model (COM). COM-Objekte implementieren eine Reihe von Methoden, die zu einer oder mehreren Schnittstellen gehören, oder Auflistungen verwandter Funktionen, die definieren, wie objekte sich in COM verhalten und funktionieren. Benutzer greifen nur über Zeiger auf diese Schnittstellen auf COM-Objekte zu.
  
MAPI bietet plattformübergreifende Unterstützung durch Branchenstandards wie SMTP und X.400. Sie können MAPI-Anwendungen auf Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 und Windows XP ausführen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

