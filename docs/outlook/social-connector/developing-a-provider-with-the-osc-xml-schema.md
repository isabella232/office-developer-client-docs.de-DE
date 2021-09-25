---
title: Entwickeln eines Providers mit dem OSC-XML-Schema
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Das XML-Schema Outlook OSC-Anbieters (Social Connector) definiert das Format einer erheblichen Menge von Informationen, die von einem sozialen Netzwerk über den OSC-Anbieter des Netzwerks an osc übergeben werden.
ms.openlocfilehash: 45a9fcc2aab435b4b82e42b80e6601ca2ef2f7f1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629179"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Entwickeln eines Providers mit dem OSC-XML-Schema

Das XML-Schema Outlook OSC-Anbieters (Social Connector) definiert das Format einer erheblichen Menge von Informationen, die von einem sozialen Netzwerk über den OSC-Anbieter des Netzwerks an osc übergeben werden. Das XML-Schema ermöglicht es einem OSC-Anbieter, Funktionen des Anbieters, Freunde und Aktivitätsfeed-Elemente im sozialen Netzwerk mithilfe der drei Hauptelemente, **Funktionen,** **Freunde** und **activityFeed** und deren untergeordnete Elemente anzugeben. Der OSC-Anbieter implementiert Schnittstellen und deren Methoden in der OSC-Anbietererweiterung und gibt XML-Zeichenfolgen als Ausgabeparameter zurück, die dem OSC-Anbieter-XML-Schema entsprechen. Der OSC ruft diese Methoden auf, um Informationen abzurufen, die er gemäß definition durch das XML-Schema verstehen kann.
  
> [!NOTE]
> Die OSC-Anbietererweiterung unterstützt das Debuggen von Anbietern, indem der `DebugProviders` Wert des  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` Registrierungsschlüssels auf 1 festgelegt wird. Wenn Sie das Anbieterdebugging aktivieren, überprüft osc den Anbieter-XML-Code anhand der Version des OSC-XML-Schemas, die Sie im **XML-Attribut xmlns** angeben. Geben Sie für OSC 1.1 und Versionen des OSC seit Outlook Connector für soziale Netzwerke 2013 das **xmlns-Attribut** wie folgt an:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Synchronisieren von Freunden und Aktivitäten:](synchronizing-friends-and-activities.md)Beschreibt die verschiedenen Möglichkeiten, wie OSC-Anbieter Freunde, Nicht-Freunde und Aktivitäten in einem sozialen Netzwerk synchronisieren können. 
    
- [OSC-Anbieter-XML-Beispiele:](osc-provider-xml-examples.md)Enthält XML-Beispiele, die zeigen, wie Funktionen eines OSC-Anbieters, Freunde und Aktivitätsfeedelemente in einem sozialen Netzwerk mithilfe des OSC-XML-Schemas angegeben werden.
    
- [XML für Funktionen:](xml-for-capabilities.md)Erläutert die - [ISocialProvider::GetCapabilities-Methode,](isocialprovider-getcapabilities.md) die der OSC verwendet, um Funktionsinformationen , ausgedrückt in **Funktions-XML,** vom OSC-Anbieter abzurufen. In diesem Abschnitt werden auch die XML-Elemente im OSC-Anbieter-XML-Schema beschrieben, mit denen ein OSC-Anbieter seine Funktionalität angeben kann, einschließlich der Authentifizierung von Benutzern und der Synchronisierung von Freunden und Aktivitäten. 
    
- [XML für Freunde:](xml-for-friends.md)Enthält Beispiele für die APIs, die der OSC verwendet, um informationen von Freunden , ausgedrückt in **Freunde-XML,** vom OSC-Anbieter abzurufen. In diesem Abschnitt werden auch Elemente im **FRIENDS-XML** beschrieben. 
    
- [XML für Aktivitäten:](xml-for-activities.md)Enthält Beispiele für die APIs, die der OSC zum Abrufen von Aktivitätsinformationen (in **activityFeed** XML) vom OSC-Anbieter verwendet. In diesem Abschnitt werden auch die XML-Elemente im OSC-Anbieter-XML-Schema beschrieben, mit denen ein OSC-Anbieter einen Aktivitätsfeed angeben kann. Ein Aktivitätsfeed umfasst das Netzwerk, in dem die Aktivitätsfeedelemente stammen, Details zu jedem Aktivitätsfeedelement (z. B. Besitzer, Typ und Veröffentlichungsdatum der Aktivität) und die Vorlage zum Anzeigen der Aktivität. 
    
## <a name="reference"></a>Referenz

- [Referenz zum Outlook Connector Provider für soziale Netzwerke](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)
  
- [Debuggen eines Providers](debugging-a-provider.md)
  
- [Bereitstellen eines Providers](deploying-a-provider.md)
  
- [Bewährte Methoden für die Entwicklung eines Anbieters](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Siehe auch

- [Debuggen eines Providers](debugging-a-provider.md)

