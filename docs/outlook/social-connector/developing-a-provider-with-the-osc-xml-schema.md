---
title: Entwickeln eines Providers mit dem OSC-XML-Schema
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Das XML-Schema des Outlook Social Connector-Anbieters (OSC) definiert das Format einer beträchtlichen Menge an Informationen, die von einem sozialen Netzwerk über den OSC-Anbieter des Netzwerks an OSC übergeben werden.
ms.openlocfilehash: 75809179131ce6c6b8bbe171d2670e59cebe3494
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281076"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Entwickeln eines Providers mit dem OSC-XML-Schema

Das XML-Schema des Outlook Social Connector-Anbieters (OSC) definiert das Format einer beträchtlichen Menge an Informationen, die von einem sozialen Netzwerk über den OSC-Anbieter des Netzwerks an OSC übergeben werden. Das XML-Schema ermöglicht einem OSC-Anbieter das Angeben von Funktionen der Elemente des Anbieters, der Freunde und des Aktivitätsfeeds im sozialen Netzwerk mithilfe der drei Hauptelemente, **Funktionen**, **Freunde**und **activityFeed**und des untergeordneten Elements. Elemente. Der OSC-Anbieter implementiert Schnittstellen und ihre Methoden in der OSC-Anbieter Erweiterbarkeit und gibt XML-Zeichenfolgen als Ausgabeparameter zurück, die dem OSC-Anbieter-XML-Schema entsprechen. OSC ruft diese Methoden auf, um Informationen abzurufen, die Sie im XML-Schema definieren können.
  
> [!NOTE]
> OSC-Anbietererweiterung unterstützt das Debuggen von `DebugProviders` Anbietern, indem `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` der Wert des Registrierungsschlüssels auf 1 festgelegt wird. Wenn Sie das Anbieter Debugging aktivieren, validiert OSC den Anbieter-XML-Code anhand der Version des OSC-XML-Schemas, die Sie im **xmlns** -XML-Attribut angeben. Geben Sie für OSC 1,1 und die Versionen des OSC seit Outlook Social Connector 2013 das **xmlns** -Attribut wie folgt an:`xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Synchronisieren von Freunden und Aktivitäten](synchronizing-friends-and-activities.md): Beschreibt die verschiedenen Möglichkeiten, wie osc-Anbieter Freunde, nicht-Freunde und Aktivitäten in einem sozialen Netzwerk synchronisieren können. 
    
- [Osc-Anbieter-XML-Beispiele](osc-provider-xml-examples.md): enthält XML-Beispiele, die zeigen, wie Sie Funktionen eines osc-Anbieters, von Freunden und von Aktivitätsfeed-Elementen in einem sozialen Netzwerk mithilfe des osc-XML-Schemas angeben.
    
- [XML for Capabilities](xml-for-capabilities.md): erläutert die- [ISocialProvider:: getCapabilities](isocialprovider-getcapabilities.md) -Methode, die der osc zum Abrufen von in **Capabilities** -XML enthaltenen Funktionsinformationen vom osc-Anbieter verwendet. In diesem Abschnitt werden auch die XML-Elemente im XML-Schema des OSC-Anbieters beschrieben, die es einem OSC-Anbieter ermöglichen, seine Funktionalität anzugeben, einschließlich der Authentifizierung von Benutzern und der Synchronisierung von Freunden und Aktivitäten. 
    
- [XML for friends](xml-for-friends.md): enthält Beispiele der APIs, die der osc zum Abrufen von Informationen zu Freunden verwendet, ausgedrückt in **friends** -XML vom osc-Anbieter. In diesem Abschnitt werden auch die Elemente im **friends** -XML beschrieben. 
    
- [XML for Activities](xml-for-activities.md): enthält Beispiele der APIs, die der osc zum Abrufen von Aktivitätsinformationen verwendet, ausgedrückt in **activityFeed** -XML vom osc-Anbieter. In diesem Abschnitt werden auch die XML-Elemente im XML-Schema des OSC-Anbieters beschrieben, mit denen ein OSC-Anbieter einen Aktivitätsfeed angeben kann. Ein Aktivitätsfeed enthält das Netzwerk, in dem die Aktivitätsfeed-Elemente stammen, Details zu den einzelnen Aktivitätsfeed-Elementen (wie Besitzer, Typ und Veröffentlichungsdatum der Aktivität) und die Vorlage zum Anzeigen der Aktivität. 
    
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

