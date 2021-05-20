---
title: Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Der Outlook Social Connector (OSC) kann in der Office-Visitenkarte und Outlook-Personenbereich-Aktivitäten, Status- oder Fotoupdates für einen Kollegen, Freund oder eine person angezeigt werden, der Sie zugeordnet sind.
ms.openlocfilehash: 0ee9451e64f12e8ba371c1ba91a1379cff257313
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428011"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken

Der Outlook Social Connector (OSC) kann in der Office-Visitenkarte und Outlook-Personenbereich-Aktivitäten, Status- oder Fotoupdates für einen Kollegen, Freund oder eine person angezeigt werden, der Sie zugeordnet sind. Standardmäßig zeigt das Betriebssystem die Outlook E-Mails, Anlagen und Besprechungsanfragen an, die von einer ausgewählten Person empfangen wurden. Wenn die ausgewählte Person und der Office benutzer an einer SharePoint-Website zusammenarbeiten, zeigt das OsC auch Dokumentaktualisierungen und andere Websiteaktivitäten von dieser SharePoint an. Abhängig von den Kontexten der Zuordnung, die der Office-Benutzer interessiert, kann der Office-Benutzer OSC-Anbieter für Geschäftsanwendungen, interne Unternehmenswebsites oder eine Vielzahl von professionellen und sozialen Netzwerkwebsites wie LinkedIn, Facebook und Windows Live installieren.
  
Um die Freigabe von Funktionen Office Clientanwendungen zu unterstützen, wird das OSC-Kernmodul als Teil einer freigegebenen Office-Komponente implementiert, und der Personenbereich wird als Outlook-Add-In implementiert. Für die Verwendung des OSC muss ein Office-Benutzer Outlook auf diesem Clientcomputer installiert und Outlook mit einem Profil konfiguriert haben, damit das OSC Kontakte in einem Ordner Kontakte zwischenspeichern kann. 
  
Ein OSC-Anbieter ist eine COM-DLL (Component Object Model), mit der das OSC unabhängig von den APIs der einzelnen sozialen Netzwerke auf Daten in sozialen Netzwerken zugreifen kann. Eine OSC-Anbieter-DLL muss lokal auf einem Clientcomputer installiert werden. Der OsC-Anbieter eines sozialen Netzwerks verbindet das OSC, das Teil von Outlook ist, mit dem sozialen Netzwerk im Internet.
  
Ein OSC-Anbieter muss eine Reihe von Schnittstellen implementieren, die als Teil der Erweiterbarkeit des OSC-Anbieters definiert sind, um mit dem OSC zu kommunizieren. Die Erweiterbarkeit des OSC-Anbieters ist als offene Plattform verfügbar.
  
Die Anbieterarchitektur des OSC ermöglicht es mehreren Anbietern, mit dem OSC-Kernmodul zu arbeiten und soziale Informationen wie Freunde und Aktivitäten zu aggregieren. Abbildung 1 veranschaulicht die Architektur des OSC-Anbieters.
  
**Abbildung 1. Outlook Architektur des Anbieters für sozialen Connector**

![Soziale Netzwerke, OSC-Provider, OSC und Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Begrifflichkeiten

In diesem Outlook Social Connector Provider Reference wird ein soziales Netzwerk verwendet, um auf die folgenden Arten von Websites zu verweisen: 
  
- Zusammenarbeitswebsites wie SharePoint.
    
- Websites für soziale Netzwerke wie Facebook und Windows Live.
    
- Professional Netzwerkstandorte wie LinkedIn.
    
- Andere Geschäftsanwendungen oder unternehmensinterne Websites, die für Netzwerke verwendet werden.
    
Der Begriff "Freund" wird im Allgemeinen verwendet, um Freunde, Familie, Kollegen, Verbindungen und alle anderen Personen, mit der ein Office-Benutzer in einem kollaborativen Kontext wie SharePoint verknüpft ist oder dem Konto des Benutzers für soziale Netzwerke hinzugefügt wurde. Nicht-Freunde sind Personen, auf die in den Aktivitätsupdates von Freunden verwiesen wird, aber keine Freunde, die dem Konto Office sozialen Netzwerk des Benutzers hinzugefügt wurden. Kontakte sind Personen in einem Outlook Kontaktordner. 
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

