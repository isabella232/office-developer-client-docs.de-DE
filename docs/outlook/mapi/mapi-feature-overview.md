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
  
MAPI verfügt über mehrere wichtige Features, die es ermöglichen, Entwicklern eine konsistente Methode für die nahtlose Zusammenarbeit und Verwendung verschiedener Messagingsysteme bereitzustellen. Zu diesen Features gehören eine umfassende und offene Programmierschnittstelle sowie Unterstützung für Branchenstandards. 
  
Da MAPI eine offene Programmierschnittstelle ist, werden Dienste auf generische Weise bereitgestellt, sodass Benutzer jetzt und in Zukunft alle erforderlichen Anpassungen hinzufügen können. Die MAPI-Programmierschnittstelle erfüllt die Anforderungen von Clientanwendungen mit unterschiedlichen Messaginganforderungen, beispielsweise einer Textverarbeitungsanwendung, die nur die Möglichkeit zum Senden von Dokumenten benötigt, oder eine Arbeitsgruppenanwendung, die die Möglichkeit zum Freigeben und Speichern Sie unterschiedliche Datentypen. Tatsächlich kann jede Anwendung, die Informationen in einem bestimmten Format austauschen oder speichern muss, von der MAPI-Programmierschnittstelle profitieren. Jeder Dienstanbieter kann die-Schnittstelle verwenden, um die eindeutigen Features des Messagingsystems verfügbar zu machen, indem er diese Features auswählt, die den größten Nutzen für Anwendungsbenutzer bieten.
  
MAPI bietet eine Trennung zwischen der Programmierschnittstelle, die von den Front-End-Messaging-Clientanwendungen verwendet wird, und der Programmierschnittstelle, die von den Back-End-Dienstanbietern verwendet wird. Die Trennung der Clientschnittstelle vom Dienstanbieter ermöglicht es einer einzelnen Anwendung, mehrere Messagingsysteme und mehrere Anwendungen für die Verwendung eines einzelnen Dienstanbieters zu verwenden. Jede Komponente kann mit einer allgemeinen Microsoft Windows-basierten Benutzeroberfläche verwendet werden. Dies ist ein großer Vorteil für die Benutzer. Benutzer können je nach Ihren Anforderungen jederzeit aus einer Vielzahl von Systemen auswählen und konsistent mit jedem ausgewählten System arbeiten und so eine echte Unabhängigkeit von bestimmten Messagingsystemen gewährleisten. 
  
Eine einzelne Messaging-Clientanwendung kann beispielsweise Nachrichten von einem Fax, einer Voicemail und einem RSS-Feed empfangen. Nachrichten von allen diesen Systemen können bei der Ankunft an einem einzigen Speicherort oder in einem universellen Posteingang abgelegt werden. Wenn Sie mit einer einzigen Anwendung alle diese Systeme behandeln, werden die Kosten für die Entwicklung, die Benutzerschulung und die Systemverwaltung verringert. 
  
Die Trennung der Clientschnittstelle von der Anbieterschnittstelle entfernt alle Programmabhängigkeiten, die vom Messagingsystem auf die Anwendung übertragen werden, und umgekehrt. Entwickler von Clientanwendungen und Dienstanbietern schreiben Code in einen Standardsatz von MAPI-Features, statt auf eine Reihe von anwendungsspezifischen oder Messagingsystem spezifischen Features. Entwickler konzentrieren sich nur auf Ihre Komponente, unabhängig davon, ob es sich um einen Client-oder Dienstanbieter handelt, und MAPI verarbeitet den Rest, wodurch die Entwicklungszeiten und-Kosten gesenkt werden.
  
Die MAPI-Programmierschnittstelle bietet eine umfassende Palette an Features. MAPI richtet sich an den leistungsstarken neuen Markt von Arbeitsgruppenanwendungen – Anwendungen, die mit unterschiedlichen Messagingsystemen wie Fax, DEC all-in-1, Voicemail und öffentlichen Kommunikationsdiensten wie AT&T EasyLink-Dienste, CompuServe und MCI kommunizieren. Mail. Mit der MAPI-Schnittstelle können Dienstanbieter für alle diese Systeme zur Verfügung gestellt werden. 
  
MAPI-kompatible Objekte ähneln in Form den COM-Objekten (Component Object Model). COM-Objekte implementieren eine Reihe von Methoden, die zu einer oder mehreren Schnittstellen gehören, oder Auflistungen verwandter Funktionen, die definieren, wie Objekte in COM Verhalten und funktionieren. Benutzer greifen nur über Zeiger auf diese Schnittstellen auf COM-Objekte zu.
  
MAPI bietet plattformübergreifende Unterstützung durch Branchenstandards wie SMTP und X. 400. Sie können MAPI-Anwendungen unter Windows 7, Windows Vista, Windows Server 2008, Windows Server 2003 und Windows XP ausführen. 
  
## <a name="see-also"></a>Siehe auch

- [MAPI-Features und -Architektur](mapi-features-and-architecture.md)

