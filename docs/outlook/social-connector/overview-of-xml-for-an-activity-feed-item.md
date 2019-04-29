---
title: Überblick über XML für ein Aktivitätsfeedelement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten, die in einem sozialen Netzwerk auftreten. Jeder Aktivitätsfeed wird durch ein activityFeed-Element dargestellt und zeichnet sich durch diese drei Informationselemente aus:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439947"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Überblick über XML für ein Aktivitätsfeedelement

Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten, die in einem sozialen Netzwerk auftreten. Jeder Aktivitätsfeed wird durch ein **activityFeed** -Element dargestellt und zeichnet sich durch diese drei Informationselemente aus: 
  
- **Netzwerk**– Name des sozialen Netzwerks, von dem die Aktivitäten stammten.
    
- **Aktivitäten**– Container für Aktivitäten, die im Konto des angemeldeten Benutzers in diesem sozialen Netzwerk stattfindet.
    
- **Vorlagen**– Container für Vorlagen, die verwendet werden, um das entsprechende Aktivitätselement in **Aktivitäten**anzuzeigen.
    
Zum Erstellen eines Aktivitätsfeed-Elements müssen Sie dem XML-Schema für die Erweiterbarkeit von Outlook Social Connector (OSC) entsprechen. Abbildung 1 zeigt die XML-Struktur des Aktivitätsfeeds.
  
**Abbildung 1. XML-Struktur des Aktivitätsfeeds**

![Aktivitäts-XML-Struktur](media/odc_ol14_ta_OSC_Fig06.gif)
  
Für jedes Aktivitätsfeed-Element sind die beiden wichtigsten Teile dieses Schemas die Elemente **activityDetails** und **activityTemplateContainer** : 
  
- Das **activityDetails** -Element speichert bestimmte Informationen für jedes Aktivitätsfeed-Element, beispielsweise den Namen des Aktivitäts Besitzers oder die URL für die hochgeladenen Bilder. 
    
- Das **activityTemplateContainer** -Element speichert das Format oder Layout für jedes Aktivitätsfeed-Element. Sie besteht aus Vorlagen, dargestellt durch einzelne **activityTemplate** -Elemente, die für mehrere Feed-Elemente wieder verwendet werden können. 
    
Bei einem einzelnen Aktivitätsfeed-Element gibt das **activityTemplate** -Element die folgenden vier Informationen an: 
  
- **Symbol**– gibt die URL für das Symbol an, um das Aktivitäts Feedelement anzuzeigen.
    
- **Title**– Beschreibung des Aktivitätsfeed-Elements.
    
- **Typ**– gibt den Aktivitätstyp an, beispielsweise ein Status-, Foto-oder Dokument Update.
    
- **Data**– gibt alle zusätzlichen Informationen an, die mit Activity Feed Item angezeigt werden.
    
> [!TIP]
> Das im Aktivitätsfeed angezeigte Symbol ist immer identisch mit dem Anbieter Symbol, das von der **ISocialProvider:: SocialNetworkIcon** -Eigenschaft zurückgegeben wird. 
  
In den folgenden Themen finden Sie weitere Informationen zum **activityDetails** -Element, dem **activityTemplateContainer** -Element, Vorlagen Token und Vorlagenvariablen: 
  
- [activityDetails-Element](activitydetails-element.md)
    
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
- [Richtlinien für die OrdnungsGemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)
    
Ein Beispiel für Aktivitäts-Feed-XML finden Sie unter [Activity Feed XML example](activity-feed-xml-example.md).
  
## <a name="see-also"></a>Siehe auch

- [XML für Aktivitäten](xml-for-activities.md) 
- [XML-Schema des Anbieters für soziale Netzwerke in Outlook](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

