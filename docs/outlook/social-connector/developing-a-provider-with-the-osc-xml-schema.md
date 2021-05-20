---
title: Entwickeln eines Providers mit dem OSC-XML-Schema
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Das Outlook Social Connector (OSC)-Anbieter-XML-Schema definiert das Format einer erheblichen Menge von Informationen, die von einem sozialen Netzwerk über den OSC-Anbieter des Netzwerks an das OSC übergeben werden.
ms.openlocfilehash: 2346e23beb2de1664ec90263a8f5db5d46c54e6f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539255"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Entwickeln eines Providers mit dem OSC-XML-Schema

Das Outlook Social Connector (OSC)-Anbieter-XML-Schema definiert das Format einer erheblichen Menge von Informationen, die von einem sozialen Netzwerk über den OSC-Anbieter des Netzwerks an das OSC übergeben werden. Das XML-Schema ermöglicht es einem OSC-Anbieter, Funktionen des Anbieters, der Freunde und der Aktivitätsfeedelemente im sozialen Netzwerk anzugeben, indem die drei Hauptelemente, Funktionen, **Freunde** und **activityFeed** und deren untergeordnete Elemente verwendet werden. Der OSC-Anbieter implementiert Schnittstellen und deren Methoden in der Erweiterbarkeit des OSC-Anbieters und gibt XML-Zeichenfolgen als Ausgabeparameter zurück, die dem XML-Schema des OSC-Anbieters entsprechen. Die OSC ruft diese Methoden auf, um Informationen zu erhalten, die sie gemäß der Definition durch das XML-Schema verstehen kann.
  
> [!NOTE]
> Die Erweiterbarkeit des OSC-Anbieters unterstützt Debuganbieter, indem der Wert `DebugProviders` des  `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` Registrierungsschlüssels auf 1 festlegen wird. Wenn Sie das Anbieterdebuding aktivieren, überprüft die OSC die Anbieter-XML mit der Version des OSC-XML-Schemas, das Sie im **xmlns-XML-Attribut** angeben. Geben Sie für OSC 1.1 und Versionen der OSC seit Outlook Social Connector 2013 das **xmlns-Attribut** wie folgt an:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Synchronisieren von Freunden und Aktivitäten:](synchronizing-friends-and-activities.md)Beschreibt die verschiedenen Möglichkeiten, wie OSC-Anbieter Freunde, Nicht-Freunde und Aktivitäten in einem sozialen Netzwerk synchronisieren können. 
    
- [OSC-Anbieter-XML-Beispiele:](osc-provider-xml-examples.md)Enthält XML-Beispiele, die zeigen, wie Funktionen eines OSC-Anbieters, von Freunden und Aktivitätsfeedelementen in einem sozialen Netzwerk mithilfe des OSC-XML-Schemas angegeben werden.
    
- [XML for Capabilities](xml-for-capabilities.md): Erläutert die - [ISocialProvider::GetCapabilities-Methode,](isocialprovider-getcapabilities.md) die vom OSC zum Abrufen von Funktioneninformationen verwendet wird, ausgedrückt **in** Funktionen-XML, vom OSC-Anbieter. In diesem Abschnitt werden auch die XML-Elemente im OSC-Anbieter-XML-Schema beschrieben, mit denen ein OSC-Anbieter seine Funktionalität angeben kann, einschließlich der Authentifizierung von Benutzern und der Synchronisierung von Freunden und Aktivitäten. 
    
- [XML für Freunde](xml-for-friends.md): Enthält Beispiele für apIs, die das OSC verwendet, um Freundesinformationen, ausgedrückt in **Friends** XML, vom OSC-Anbieter zu erhalten. In diesem Abschnitt werden auch Elemente in der **friends-XML** beschrieben. 
    
- [XML for Activities](xml-for-activities.md): Enthält Beispiele für apIs, die das OSC zum Abrufen von Aktivitäteninformationen verwendet, ausgedrückt in **activityFeed** XML, vom OSC-Anbieter. In diesem Abschnitt werden auch die XML-Elemente im XML-Schema des OSC-Anbieters beschrieben, mit denen ein OSC-Anbieter einen Aktivitätsfeed angeben kann. Ein Aktivitätsfeed enthält das Netzwerk, in dem die Aktivitätsfeedelemente stammen, Details zu den einzelnen Aktivitätsfeedelementen (z. B. Besitzer, Typ und Veröffentlichungsdatum der Aktivität) und die Vorlage zum Anzeigen der Aktivität. 
    
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

