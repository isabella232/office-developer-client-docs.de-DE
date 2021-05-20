---
title: Überblick über XML für ein Aktivitätsfeedelement
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 366550fa-e787-4ca0-bfe1-a7890dfc27c6
description: 'Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten in einem sozialen Netzwerk. Jeder Aktivitätsfeed wird durch ein activityFeed-Element dargestellt und durch die drei folgenden Informationen gekennzeichnet:'
ms.openlocfilehash: 971c54cf69a65bebbe4fd04e8608e88b89145bb4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439947"
---
# <a name="overview-of-xml-for-an-activity-feed-item"></a>Überblick über XML für ein Aktivitätsfeedelement

Ein Aktivitätsfeed besteht aus einer oder mehreren Aktivitäten in einem sozialen Netzwerk. Jeder Aktivitätsfeed wird durch ein **activityFeed-Element** dargestellt und durch die drei folgenden Informationen gekennzeichnet: 
  
- **network**– Name des sozialen Netzwerks, aus dem die Aktivitäten stammen.
    
- **activities**– Container für Aktivitäten, die im Konto des angemeldeten Benutzers in diesem sozialen Netzwerk geschehen.
    
- **templates**– Container für Vorlagen, die zum Anzeigen des entsprechenden Aktivitätselements in Aktivitäten **verwendet werden.**
    
Zum Erstellen eines Aktivitätsfeedelements müssen Sie das xml-Schema Outlook Social Connector (OSC) des Anbieters für die Erweiterbarkeit erfüllen. Abbildung 1 zeigt die XML-Struktur des Aktivitätsfeeds.
  
**Abbildung 1. Aktivitätsfeed-XML-Struktur**

![Aktivitäts-XML-Struktur](media/odc_ol14_ta_OSC_Fig06.gif)
  
Für jedes Aktivitätsfeedelement sind die beiden wichtigsten Teile dieses Schemas **die Elemente activityDetails** und **activityTemplateContainer:** 
  
- Das **activityDetails-Element** speichert spezifische Informationen für jedes Aktivitätsfeedelement, z. B. den Namen des Aktivitätsbesitzers oder die URL für die hochgeladenen Bilder. 
    
- Das **activityTemplateContainer-Element** speichert das Format oder Layout für jedes Aktivitätsfeedelement. Es besteht aus Vorlagen, dargestellt durch einzelne **activityTemplate-Elemente,** die für mehrere Feedelemente wiederverwendet werden können. 
    
Für ein einzelnes Aktivitätsfeedelement gibt das **activityTemplate-Element** die folgenden vier Informationen an: 
  
- **icon**– Gibt die URL für das Symbol an, das das Aktivitätsfeedelement anzeigen soll.
    
- **title**– Beschreibt das Aktivitätsfeedelement.
    
- **type**– Gibt den Typ der Aktivität an, z. B. Status, Foto oder Dokumentaktualisierung.
    
- **data**– Gibt alle zusätzlichen Informationen an, die mit dem Aktivitätsfeedelement angezeigt werden.
    
> [!TIP]
> Das im Aktivitätsfeed angezeigte Symbol ist immer identisch mit dem Anbietersymbol, das von der **ISocialProvider::SocialNetworkIcon-Eigenschaft zurückgegeben** wird. 
  
Weitere Informationen zum **activityDetails-Element,** dem **activityTemplateContainer-Element,** Vorlagentoken und Vorlagenvariablen finden Sie in den folgenden Themen: 
  
- [activityDetails-Element](activitydetails-element.md)
    
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)
    
- [Vorlagenvariablen](template-variables.md)
    
- [Richtlinien für die ordnungsgemäßen Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)
    
Ein Beispiel für aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md).
  
## <a name="see-also"></a>Siehe auch

- [XML für Aktivitäten](xml-for-activities.md) 
- [Outlook XML-Schema des Anbieters für sozialen Connector](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

