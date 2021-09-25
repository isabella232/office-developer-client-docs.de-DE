---
title: Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f33705cc-8add-42be-9d9f-f4e9245d83f5
description: Der Outlook Connector für soziale Netzwerke (OSC) kann in der Office Visitenkarte und Outlook Personenbereich-Aktivitäten, Status- oder Fotoupdates für einen Kollegen, Freunde oder eine beliebige Person, der Sie zugeordnet sind, angezeigt werden.
ms.openlocfilehash: 4193006addd15bdc509fe14cae80c14c107685a1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59555006"
---
# <a name="relating-the-osc-with-outlook-and-social-networks"></a>Erstellen einer Beziehung zwischen dem OSC und Outlook bzw. sozialen Netzwerken

Der Outlook Connector für soziale Netzwerke (OSC) kann in der Office Visitenkarte und Outlook Personenbereich-Aktivitäten, Status- oder Fotoupdates für einen Kollegen, Freunde oder eine beliebige Person, der Sie zugeordnet sind, angezeigt werden. Standardmäßig zeigt der OSC die Outlook E-Mails, Anlagen und Besprechungsanfragen an, die von einer ausgewählten Person empfangen wurden. Wenn die ausgewählte Person und der Office Benutzer an einer SharePoint Website zusammenarbeiten, zeigt osc auch Dokumentaktualisierungen und andere Websiteaktivitäten von dieser SharePoint Website an. Abhängig vom Kontext der Zuordnung, an dem der Office Benutzer interessiert ist, kann der Office Benutzer OSC-Anbieter für Branchenanwendungen, interne Unternehmenswebsites oder eine Vielzahl von professionellen und sozialen Netzwerkwebsites wie LinkedIn, Facebook und Windows Live installieren.
  
Um die Freigabe von Funktionen über Office Clientanwendungen hinweg zu unterstützen, wird das OSC-Kernmodul als Teil einer Office freigegebenen Komponente implementiert, und der Personenbereich wird als Outlook-Add-In implementiert. Zur Verwendung des OSC muss ein Office Benutzer Outlook auf diesem Clientcomputer installiert und Outlook mit einem Profil konfiguriert haben, damit der OSC Kontakte in einem Kontaktordner zwischenspeichern kann. 
  
Ein OSC-Anbieter ist eine COM-DLL (Component Object Model), mit der OSC unabhängig von den APIs der einzelnen sozialen Netzwerke auf Daten in sozialen Netzwerken zugreifen kann. Eine OSC-Anbieter-DLL muss lokal auf einem Clientcomputer installiert werden. Der OSC-Anbieter eines sozialen Netzwerks verbindet den OSC, der Teil Outlook ist, mit dem sozialen Netzwerk im Internet.
  
Ein OSC-Anbieter muss eine Reihe von Schnittstellen implementieren, die als Teil der OSC-Anbietererweiterung definiert sind, um mit dem OSC zu kommunizieren. Die OSC-Anbietererweiterung ist als offene Plattform verfügbar.
  
Die Anbieterarchitektur des OSC ermöglicht es mehreren Anbietern, mit dem OSC-Kernmodul zu arbeiten und soziale Informationen wie Freunde und Aktivitäten zu aggregieren. Abbildung 1 zeigt die OSC-Anbieterarchitektur.
  
**Abbildung 1. Outlook Anbieterarchitektur für Connector für soziale Netzwerke**

![Soziale Netzwerke, OSC-Provider, OSC und Office](media/off15OSCRef_Architecture.gif)
  
## <a name="terminology"></a>Begrifflichkeiten

In dieser Outlook Connector-Anbieterreferenz für soziale Netzwerke wird ein soziales Netzwerk verwendet, um auf die folgenden Arten von Websites zu verweisen: 
  
- Websites für die Zusammenarbeit, z. B. SharePoint.
    
- Soziale Netzwerkwebsites wie Facebook und Windows Live.
    
- Professional Netzwerkstandorte wie LinkedIn.
    
- Andere Branchenanwendungen oder interne Unternehmenswebsites, die für Netzwerke verwendet werden.
    
Der Begriff "Freund" wird in der Regel verwendet, um Freunde, Familie, Kollegen, Verbindungen und alle anderen Personen einzuschließen, mit denen ein Office Benutzer in einem Zusammenarbeitskontext wie SharePoint verknüpft ist oder dem Konto des Benutzers im sozialen Netzwerk hinzugefügt wurde. Nicht-Freunde sind Personen, auf die in den Aktivitätsupdates von Freunden verwiesen wird, aber keine Freunde, die dem Konto des Office sozialen Netzwerks hinzugefügt wurden. Kontakte sind Personen in einem Outlook Kontaktordner. 
  
## <a name="see-also"></a>Siehe auch

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)

