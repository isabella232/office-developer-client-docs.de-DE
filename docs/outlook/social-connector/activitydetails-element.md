---
title: activityDetails-Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Das activityDetails-Element speichert die Rohdaten für ein einzelnes Aktivitätsfeed-Element. Jedes Activity Feed-Element muss ein eigenes activityDetails-Element aufweisen. Auf Daten im activityDetails-Element wird in Aktivitätsvorlagen mithilfe von Name-Elementen verwiesen.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32281349"
---
# <a name="activitydetails-element"></a>activityDetails-Element

Das **activityDetails** -Element speichert die Rohdaten für ein einzelnes Aktivitätsfeed-Element. Jedes Activity Feed-Element muss ein eigenes **activityDetails** -Element aufweisen. Auf Daten im **activityDetails** -Element wird in Aktivitätsvorlagen mithilfe von **Name** -Elementen verwiesen. Alle Daten im **activityDetails** -Element müssen ein **Name** -Element aufweisen. 
  
In der folgenden Tabelle werden die sechs Elemente beschrieben, die das **activityDetails** -Element benötigt. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**ownerID** <br/> |Die ID des Benutzers im sozialen Netzwerk, der dieses Aktivitätsfeed-Element generiert hat.  <br/> |
|**objectID** <br/> |Eine eindeutige Zeichenfolge für das Aktivitätsfeed-Element, um doppelte Feed-Elemente zu identifizieren.  <br/> |
|**applicationId** <br/> |Eine von zwei eindeutigen IDs, die verwendet werden, um das Aktivitäts Feedelement mit seiner Vorlage abzugleichen. Wenn Sie mehrere Anwendungen oder andere Gruppierungen haben, kann dies als eine Vorlage Organizer der ersten Ebene verwendet werden.  <br/> |
|**templateId** <br/> |Die zweite eindeutige ID, die verwendet wird, um das Aktivitäts Feedelement mit seiner Vorlage abzugleichen. Dieser kann als Organisator einer Vorlage für die zweite Ebene verwendet werden.  <br/> |
|**publishDate** <br/> |Datum und Uhrzeit des Veröffentlichungsvorgangs des Aktivitätsfeeds.  <br/> |
|**templateVariables** <br/> |Die Daten, die in den Token für die Aktivitätsfeed-Elementvorlage verwendet werden sollen.  <br/> |
   
Ein Beispiel für Aktivitäts-Feed-XML finden Sie unter [Aktivitätsfeed-XML-Beispiel](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitäts Feed-Element](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)  
- [Vorlagenvariablen](template-variables.md) 
- [Richtlinien für die OrdnungsGemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [XML-Schema des Anbieters für soziale Netzwerke in Outlook](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

