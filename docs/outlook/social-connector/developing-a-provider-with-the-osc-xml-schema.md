---
title: Entwickeln eines Providers mit dem OSC-XML-Schema
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0872b1b9-c21f-4bba-8cf1-4b010d8d7fb6
description: Outlook Social Connector (OSC) Provider-XML-Schemas definiert das Format einer beträchtlichen Anzahl von Informationen, die von einem sozialen Netzwerk an die OSC über das Netzwerk OSC-Anbieter übergeben wird.
ms.openlocfilehash: 93df682751146b501a316be62641b8cfd47a74a8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795969"
---
# <a name="developing-a-provider-with-the-osc-xml-schema"></a>Entwickeln eines Providers mit dem OSC-XML-Schema

Outlook Social Connector (OSC) Provider-XML-Schemas definiert das Format einer beträchtlichen Anzahl von Informationen, die von einem sozialen Netzwerk an die OSC über das Netzwerk OSC-Anbieter übergeben wird. Das XML-Schema ermöglicht einen OSC-Anbieter an Funktionen der Anbieter, Freunde und Elementen im sozialen Netzwerk, mithilfe der drei Hauptelemente, **Funktionen**, **Freunde**, und **ActivityFeed**und ihre untergeordneten Aktivitätsfeed Elemente. Der OSC-Anbieter implementiert Schnittstellen und deren Methoden in die Erweiterbarkeit des OSC-Providers Rückgabe von XML-Zeichenfolgen als Output-Parameter, die mit dem OSC-Anbieter XML-Schema entsprechen. Die OSC ruft diese Methoden zum Abrufen von Informationen, die durch das XML-Schema definierten verarbeitet werden kann.
  
> [!NOTE]
> Erweiterbarkeit des OSC-Providers debugging Anbieter unterstützt, durch Festlegen der `DebugProviders` Wert der `HKEY_CURRENT_USER\Software\Microsoft\Office\Outlook\SocialConnector` Registrierungsschlüssel auf 1. Wenn Sie das Debuggen Anbieter aktivieren, überprüft die OSC den XML-Anbieter für die Version des OSC-XML-Schemas, die Sie im XML- **Xmlns** -Attribut angeben. Geben Sie das **Xmlns** -Attribut OSC 1.1 und die OSC seit Outlook Social Connector 2013-Versionen wie folgt:`xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd"`
  
## <a name="in-this-section"></a>Inhalt dieses Abschnitts

- [Synchronisieren von Freunde und Aktivitäten](synchronizing-friends-and-activities.md): Beschreibt die verschiedenen Methoden, OSC-Anbieter Freunde, nicht Freunde und Aktivitäten in einem sozialen Netzwerk synchronisieren können. 
    
- [OSC-Anbieter-XML-Beispielen](osc-provider-xml-examples.md): enthält XML-Beispielen, die zeigen, wie Funktionen von einem OSC-Anbieter, Freunde und Aktivität angegeben feed Elemente in einem sozialen Netzwerk mit dem OSC-XML-Schema.
    
- [XML-Code für Funktionen](xml-for-capabilities.md): erläutert die - [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) -Methode, die die OSC wird verwendet, um Funktionsinformationen zu, der im **Funktionen** XML, aus der OSC-Anbieter zu erhalten. In diesem Abschnitt wird auch die XML-Elemente im XML-Schema von OSC-Anbieter, mit denen einen OSC-Anbieter an seine Funktionalität, einschließlich wie es Benutzer authentifiziert und synchronisiert Freunde und Aktivitäten. 
    
- [XML-Code für Freunde](xml-for-friends.md): enthält Beispiele für die APIs, die die OSC wird verwendet, um Informationen zu Freunde, der im **Freunde** XML, aus der OSC-Anbieter zu erhalten. In diesem Abschnitt wird auch die Elemente in der **Freunde** XML. 
    
- [XML-Code für Aktivitäten](xml-for-activities.md): enthält Beispiele für die APIs, die die OSC wird verwendet, um Aktivitätsinformationen zu, der im **ActivityFeed** XML, aus der OSC-Anbieter zu erhalten. In diesem Abschnitt wird auch die XML-Elemente im XML-Schema von OSC-Anbieter, mit die einen OSC-Anbieter eine Aktivitätsfeed angeben können. Ein Aktivitätsfeed umfasst das Netzwerk, in dem die Aktivitäts--Elemente stammt Feed, Details der einzelnen Elemente Aktivitätsfeed (z. B. Besitzer, eingeben und Veröffentlichungsdatum der Aktivität), und die Vorlage aus, um die Aktivität anzuzeigen. 
    
## <a name="reference"></a>Referenz

- [Referenz zum Outlook Connector Provider für soziale Netzwerke](outlook-social-connector-provider-reference-0.md)
  
## <a name="related-sections"></a>Verwandte Abschnitte

- [Erste Schritte zum Entwickeln eines Outlook Connector Providers für soziale Netzwerke](getting-started-with-developing-an-outlook-social-connector-provider.md)
  
- [Über den OSC-Beispielvorlagen](osc-sample-templates.md)
  
- [OSC - Typische Aufrufsequenzen](osc-typical-calling-sequences.md)
  
- [Debuggen eines Providers](debugging-a-provider.md)
  
- [Bereitstellen eines Providers](deploying-a-provider.md)
  
- [Bewährte Methoden für das Entwickeln eines Providers](best-practices-for-developing-a-provider.md)
  
## <a name="see-also"></a>Siehe auch

- [Debuggen eines Providers](debugging-a-provider.md)

