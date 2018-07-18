---
title: Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Outlook Social Connector (OSC) können in die Office-Visitenkarte und Outlook Personenbereich Aktivitäten, Status oder Foto Updates anzeigen, für einen Kollegen, Friend oder Personen, denen Sie zugeordnet sind.
ms.openlocfilehash: 6dc6221b89eca5303e7cf6a201927659d4ac9107
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796085"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken

Outlook Social Connector (OSC) können in die Office-Visitenkarte und Outlook Personenbereich Aktivitäten, Status oder Foto Updates anzeigen, für einen Kollegen, Friend oder Personen, denen Sie zugeordnet sind. In der Standardeinstellung der OSC zeigt die Outlook-e-Mails, Anlagen, und Besprechungsanfragen von eine ausgewählte Person erhalten. Wenn die ausgewählte Person und der Office-Benutzer auf einer SharePoint-Website arbeiten, zeigt die OSC auch Dokument Updates und andere Website Aktivitäten aus dieser SharePoint-Website. Je nach dem Kontext der Zuordnung, die der Benutzer Office interessiert ist, kann der Benutzer Office OSC-Anbieter für Line-of-Business Applications, interne Unternehmenswebsites oder eine Vielzahl von professional und sozialen Netzwerk-Websites, wie beispielsweise LinkedIn installieren, Facebook und Windows Live.
  
Zur Unterstützung der Freigabe von der Funktionalität der Office-Clientanwendungen OSC zentralen Modul als Teil eines gemeinsam genutzte Office-Komponente implementiert ist, und den Personenbereich als Outlook-add-in implementiert wird. Für die Verwendung der OSC muss Benutzer in einem Office-Version von Outlook auf dem Clientcomputer und Outlook mit einem Profil so konfiguriert, dass die OSC-Kontakte im Kontakteordner cache kann haben. 
  
Ein OSC-Provider ist eine DLL-Datei, mit der die OSC für soziale Netzwerke Zugriff auf Daten in eine Möglichkeit, die unabhängig von den einzelnen sozialen Netzwerk-APIs kann, Component Object Model (COM). Ein OSC-Anbieter-DLL muss lokal auf einem Clientcomputer installiert sein. Ein social Network OSC-Anbieter verbindet das osc bilden, die Bestandteil von Outlook ist, mit dem sozialen Netzwerk im Internet.
  
Ein OSC-Anbieter muss eine Reihe von Schnittstellen, die als Teil der Erweiterbarkeit des OSC-Anbieter, Kommunikation mit dem OSC definiert implementieren. Erweiterbarkeit des OSC-Providers ist als eine offene Plattform verfügbar.
  
Die Architektur der die OSC kann mehrere Anbieter zum Arbeiten mit dem OSC zentralen Modul und aggregierte für soziale Netzwerke Informationen wie Freunde und Aktivitäten. Abbildung 1 zeigt die Architektur der OSC-Anbieter.
  
**Abbildung 1. Outlook Connector für soziale Netzwerke-Architektur**

![Soziale Netzwerke, OSC-Provider, OSC und Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Terminologie

In dieser Outlook Social Connector Provider Referenz wird ein social Network verweisen auf die folgenden Arten von Websites verwendet: 
  
- Zusammenarbeit wie SharePoint-Websites.
    
- -Websites für soziale Netzwerke wie Facebook und Windows Live.
    
- Professional Netzwerkstandorten wie LinkedIn.
    
- Andere Line-of-Business Applications oder interne Unternehmenswebsites für Netzwerke verwendet.
    
Der Begriff Friend wird im Allgemeinen umfassen Freunde, Familie, Kollegen, Verbindungen und anderer Benutzer ein Office-Benutzer in einem gemeinsamen Kontext wie SharePoint zugeordnet ist oder das Konto des Benutzers für soziale Netzwerke hinzugefügt hat. Nicht-Freunde Personen in Freunde Aktivität Updates verwiesen werden jedoch nicht Freunde, die das Office Konto des Benutzers für soziale Netzwerke hinzugefügt wurden. Kontakte sind Personen in einer Outlook-Kontaktordner. 
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

