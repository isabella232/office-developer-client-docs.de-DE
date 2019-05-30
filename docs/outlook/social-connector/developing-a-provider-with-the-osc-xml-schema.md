---
title: Entwickeln eines Providers mit dem OSC-XML-Schema
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Das Connector für soziale Netzwerke (OSC)-Anbieter-XML-Schema definiert das Format einer bedeutenden Menge an Informationen, die von einem sozialen Netzwerk über den osc-Anbieter des Netzwerks an den osc übergeben wird.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539255"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Entwickeln eines Providers mit dem OSC-XML-Schema

Das Connector für soziale Netzwerke (OSC)-Anbieter-XML-Schema definiert das Format einer bedeutenden Menge an Informationen, die von einem sozialen Netzwerk über den osc-Anbieter des Netzwerks an den osc übergeben wird. Mit dem XML-Schema kann ein osc-Anbieter Funktionen des Anbieters, der Freunde und der Aktivitätsfeed-Elemente im sozialen Netzwerk mithilfe der drei Hauptelemente, **Funktionen**, **Freunde**und **activityFeed**und ihres untergeordneten Elements angeben. Elemente. Der osc-Anbieter implementiert Schnittstellen und deren Methoden in der Erweiterbarkeit des osc-Anbieters und gibt XML-Zeichenfolgen als Ausgabeparameter zurück, die dem XML-Schema des osc-Anbieters entsprechen. Der osc ruft diese Methoden auf, um Informationen zu erhalten, die er gemäß Definition des XML-Schemas verstehen kann.
  
> [!NOTE]
> OSC-Anbieter Erweiterbarkeit unterstützt das Debuggen `DebugProviders` von Anbietern, `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` indem der Wert des Registrierungsschlüssels auf 1 festgesetzt wird. Wenn Sie das Anbieter Debugging aktivieren, überprüft der osc den Anbieter-XML-Code anhand der Version des osc-XML-Schemas, das Sie im **xmlns** XML-Attribut angeben. Geben Sie für osc 1,1 und Versionen von OSC seit Outlook Connector für soziale Netzwerke 2013 das **xmlns** -Attribut wie folgt an:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md): Beschreibt die verschiedenen Möglichkeiten, mit denen osc-Anbieter Freunde, nicht-Freunde und Aktivitäten in einem sozialen Netzwerk synchronisieren können. 
    
- [Osc-Anbieter-XML-Beispiele](osc-provider-xml-examples.md): enthält XML-Beispiele, in denen gezeigt wird, wie Funktionen eines osc-Anbieters, von Freunden und von Aktivitätsfeed-Elementen in einem sozialen Netzwerk mithilfe des osc-XML-Schemas angegeben werden.
    
- [XML für Funktionen](xml-for-capabilities.md): erläutert die- [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode, mit der die osc-Funktionen Informationen abrufen, die in **Capabilities** XML vom osc-Anbieter ausgedrückt werden. In diesem Abschnitt werden außerdem die XML-Elemente im XML-Schema des osc-Anbieters beschrieben, mit denen ein osc-Anbieter seine Funktionalität angeben kann, einschließlich der Authentifizierung von Benutzern und der Synchronisierung von Freunden und Aktivitäten. 
    
- [XML für Freunde](xml-for-friends.md): enthält Beispiele der APIs, die die osc verwendet, um Freundes Informationen, ausgedrückt in **friends** XML, vom osc-Anbieter zu erhalten. In diesem Abschnitt werden auch Elemente im **friends** -XML-Code beschrieben. 
    
- [XML for Activities](xml-for-activities.md): enthält Beispiele der APIs, die die osc zum Abrufen von Aktivitätsinformationen verwendet, ausgedrückt in **activityFeed** XML, vom osc-Anbieter. In diesem Abschnitt werden außerdem die XML-Elemente im XML-Schema des osc-Anbieters beschrieben, mit denen ein osc-Anbieter einen Aktivitätsfeed angeben kann. Ein Aktivitätsfeed umfasst das Netzwerk, in dem die Aktivitätsfeed-Elemente stammen, Details zu den einzelnen Aktivitätsfeed-Elementen (wie Besitzer, Typ und Veröffentlichungsdatum der Aktivität) und die Vorlage zum Anzeigen der Aktivität. 
    
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

