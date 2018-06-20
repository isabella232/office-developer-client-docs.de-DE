---
title: ActivityDetails Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Das Element ActivityDetails speichert die Rohdaten für eine einzelne Aktivitätsfeed-Element. Jede Aktivitätsfeed-Element muss ein eigene ActivityDetails-Element enthalten. Daten im ActivityDetails-Element werden mithilfe der Name-Elemente in Aktivitätsvorlagen verwiesen.
ms.openlocfilehash: c326017a038dff138d690b020a98972a08212690
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795956"
---
# <a name="activitydetails-element"></a>ActivityDetails Element

Das Element **ActivityDetails** speichert die Rohdaten für eine einzelne Aktivitätsfeed-Element. Jede Aktivitätsfeed-Element muss ein eigene **ActivityDetails** -Element enthalten. Daten im **ActivityDetails** -Element werden mithilfe der **Name** -Elemente in Aktivitätsvorlagen verwiesen. Jeder Teil der Daten in das **ActivityDetails** -Element muss ein **Name** -Element enthalten. 
  
In der folgenden Tabelle werden die sechs Elemente, die das Element **ActivityDetails** erforderlich sind. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**ownerID** <br/> |Die ID des Benutzers im sozialen Netzwerk, die diese Aktivität generiert Element-feed.  <br/> |
|**objectID** <br/> |Eine eindeutige Zeichenfolge für die Aktivität zum Erkennen von doppelten Elementen feed Element-feed.  <br/> |
|**applicationId** <br/> |Eine der zwei eindeutigen IDs, mit denen die Aktivität match-Element mit der Vorlage feed. Wenn Sie mehrere Anwendungen oder andere Gruppen verfügen, kann dies als Organisator einer Vorlage der ersten Ebene verwendet werden.  <br/> |
|**templateId** <br/> |Die zweite eindeutige ID, mit der die Aktivität match-Element mit der Vorlage feed. Dies kann als Organisator einer L2-Vorlage verwendet werden.  <br/> |
|**publishDate** <br/> |Datum und Uhrzeit, die die Aktivitätsfeed Element veröffentlicht wurde.  <br/> |
|**templateVariables** <br/> |Die Daten in die Token für die Aktivität feed Vorlage verwendet werden.  <br/> |
   
Ein Beispiel der Aktivität XML-feed, finden Sie unter [Aktivität Feed XML-Beispiel](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML-Code für eine Aktivität Element-Feed](overview-of-xml-for-an-activity-feed-item.md)  
- [ActivityTemplateContainer Element](activitytemplatecontainer-element.md)  
- [Vorlagenvariablen](template-variables.md) 
- [Richtlinien für das Aktivitäten ordnungsgemäß anzeigen](guidelines-for-properly-displaying-activities.md)  
- [XML-Code für Aktivitäten](xml-for-activities.md)  
- [Outlook Connector für soziale Netzwerke Anbieter XML-Schema](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

