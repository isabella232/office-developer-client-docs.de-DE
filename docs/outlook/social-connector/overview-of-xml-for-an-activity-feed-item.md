---
title: Überblick über XML für ein Aktivitätsfeedelement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten, die in einem sozialen Netzwerk auftreten. Jeder Aktivitätsfeed wird durch ein activityFeed-Element dargestellt und zeichnet sich durch die folgenden drei Informationen aus:'
ms.openlocfilehash: 528a7e2c32c7a5c4c2947bfad864accd92fcc419
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59566115"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Überblick über XML für ein Aktivitätsfeedelement

Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten, die in einem sozialen Netzwerk auftreten. Jeder Aktivitätsfeed wird durch ein **activityFeed-Element** dargestellt und zeichnet sich durch die folgenden drei Informationen aus: 
  
- **Netzwerk**– Name des sozialen Netzwerks, aus dem die Aktivitäten stammen.
    
- **-Container** für Aktivitäten, die auf dem Konto des angemeldeten Benutzers in diesem sozialen Netzwerk stattfinden.
    
- **Vorlagen**– Container für Vorlagen, die zum Anzeigen des entsprechenden Aktivitätselements in **Aktivitäten** verwendet werden.
    
Um ein Aktivitätsfeedelement zu erstellen, müssen Sie dem XML-Schema für die Erweiterbarkeit des Outlook Osc-Anbieters (Social Connector) entsprechen. Abbildung 1 zeigt die XML-Struktur des Aktivitätsfeeds.
  
**Abbildung 1. Aktivitätsfeed-XML-Struktur**

![Aktivitäts-XML-Struktur](media/odc_ol14_ta_OSC_Fig06.gif)
  
Für jedes Aktivitätsfeedelement sind die beiden wichtigsten Teile dieses Schemas die **ActivityDetails-** und **activityTemplateContainer-Elemente:** 
  
- Das **ActivityDetails-Element** speichert spezifische Informationen für jedes Aktivitätsfeedelement, z. B. den Namen des Aktivitätsbesitzers oder die URL für die hochgeladenen Bilder. 
    
- Das **activityTemplateContainer-Element** speichert das Format oder Layout für jedes Aktivitätsfeedelement. Es besteht aus Vorlagen, dargestellt durch einzelne **activityTemplate-Elemente,** die für mehrere Feedelemente wiederverwendet werden können. 
    
Für ein einzelnes Aktivitätsfeedelement gibt das **activityTemplate-Element** die folgenden vier Informationen an: 
  
- **-Gibt** die URL für das Symbol an, um das Aktivitätsfeedelement anzuzeigen.
    
- **title**- Beschreibt das Aktivitätsfeedelement.
    
- **type**- Gibt den Typ der Aktivität an, z. B. status, foto oder dokumentaktualisierung.
    
- **-Gibt** alle zusätzlichen Informationen an, die mit dem Aktivitätsfeedelement angezeigt werden.
    
> [!TIP]
> Das im Aktivitätsfeed angezeigte Symbol entspricht immer dem Anbietersymbol, das von der **ISocialProvider::SocialNetworkIcon-Eigenschaft** zurückgegeben wird. 
  
Weitere Informationen zum **activityDetails-Element,** zum **activityTemplateContainer-Element,** zu Vorlagentoken und Vorlagenvariablen finden Sie in den folgenden Themen: 
  
- [activityDetails-Element](activitydetails-element.md)
    
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
- [Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)
    
Ein Beispiel für aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md).
  
## <a name="see-also"></a>Siehe auch

- [XML für Aktivitäten](xml-for-activities.md) 
- [Outlook XML-Schema des Connectoranbieters für soziale Netzwerke](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

