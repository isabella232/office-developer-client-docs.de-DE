---
title: activityDetails-Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Das activityDetails-Element speichert die Rohdaten für ein einzelnes Aktivitätsfeedelement. Jedes Aktivitätsfeedelement muss über ein eigenes activityDetails-Element verfügen. Auf Daten im activityDetails-Element wird in Aktivitätsvorlagen mithilfe von Name-Elementen verwiesen.
ms.openlocfilehash: fd9c2136e8e2b687fa281ecda71039809848f63c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434872"
---
# <a name="activitydetails-element"></a>activityDetails-Element

Das **activityDetails-Element** speichert die Rohdaten für ein einzelnes Aktivitätsfeedelement. Jedes Aktivitätsfeedelement muss über ein eigenes **activityDetails-Element** verfügen. Auf Daten im **activityDetails-Element** wird in Aktivitätsvorlagen mithilfe von **Name-Elementen** verwiesen. Jedes Datenelement im **activityDetails-Element** muss über ein **Name-Element** verfügen. 
  
In der folgenden Tabelle werden die sechs Elemente beschrieben, die für **das activityDetails-Element** erforderlich sind. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**ownerID** <br/> |Die ID des Benutzers im sozialen Netzwerk, der dieses Aktivitätsfeedelement generiert hat.  <br/> |
|**objectID** <br/> |Eine eindeutige Zeichenfolge für das Aktivitätsfeedelement zum Erkennen doppelter Feedelemente.  <br/> |
|**applicationId** <br/> |Eine von zwei eindeutigen IDs, die verwendet werden, um dem Aktivitätsfeedelement mit seiner Vorlage zu entsprechen. Wenn Sie über mehrere Anwendungen oder andere Gruppierungen verfügen, kann dies als Vorlagenorganisator der ersten Ebene verwendet werden.  <br/> |
|**templateId** <br/> |Die zweite eindeutige ID, die verwendet wird, um dem Aktivitätsfeedelement mit seiner Vorlage zu entsprechen. Dies kann als Vorlagenorganisator der zweiten Ebene verwendet werden.  <br/> |
|**publishDate** <br/> |Datum und Uhrzeit der Veröffentlichung des Aktivitätsfeedelements.  <br/> |
|**templateVariables** <br/> |Die Daten, die in den Token für die Aktivitätsfeedelementvorlage verwendet werden sollen.  <br/> |
   
Ein Beispiel für Aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)  
- [Vorlagenvariablen](template-variables.md) 
- [Richtlinien für die ordnungsgemäßen Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [Outlook XML-Schema des Anbieters für sozialen Connector](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

