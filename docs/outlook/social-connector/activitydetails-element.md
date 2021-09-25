---
title: activityDetails-Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c103d48d-53ca-4b19-b16f-2862379587ef
description: Das activityDetails-Element speichert die Rohdaten für ein einzelnes Aktivitätsfeedelement. Jedes Aktivitätsfeedelement muss über ein eigenes ActivityDetails-Element verfügen. Auf Daten im activityDetails-Element wird in Aktivitätsvorlagen mithilfe von Namenselementen verwiesen.
ms.openlocfilehash: a9249f3480d1cd72b01d52af15a843bb88b4625f
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59629172"
---
# <a name="activitydetails-element"></a>activityDetails-Element

Das **activityDetails-Element** speichert die Rohdaten für ein einzelnes Aktivitätsfeedelement. Jedes Aktivitätsfeedelement muss über ein eigenes **ActivityDetails-Element** verfügen. Auf Daten im **activityDetails-Element** wird in Aktivitätsvorlagen mithilfe von **Namenselementen** verwiesen. Jedes Datenelement im **activityDetails-Element** muss über ein **Name-Element** verfügen. 
  
In der folgenden Tabelle werden die sechs Elemente beschrieben, die für das **activityDetails-Element** erforderlich sind. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**ownerID** <br/> |Die ID des Benutzers im sozialen Netzwerk, der dieses Aktivitätsfeedelement generiert hat.  <br/> |
|**Objectid** <br/> |Eine eindeutige Zeichenfolge für das Aktivitätsfeedelement, um doppelte Feedelemente zu erkennen.  <br/> |
|**applicationId** <br/> |Eine von zwei eindeutigen IDs, die verwendet werden, um das Aktivitätsfeedelement mit seiner Vorlage zuzuordnen. Wenn Sie über mehrere Anwendungen oder andere Gruppierungen verfügen, kann dies als Vorlagenorganisation der ersten Ebene verwendet werden.  <br/> |
|**templateId** <br/> |Die zweite eindeutige ID, die verwendet wird, um das Aktivitätsfeedelement mit seiner Vorlage zuzuordnen. Dies kann als Organisator der zweiten Ebene von Vorlagen verwendet werden.  <br/> |
|**publishDate** <br/> |Datum und Uhrzeit der Veröffentlichung des Aktivitätsfeedelements.  <br/> |
|**templateVariables** <br/> |Die Daten, die in den Token für die Aktivitätsfeedelementvorlage verwendet werden sollen.  <br/> |
   
Ein Beispiel für den Aktivitätsfeed-XML-Code finden Sie unter ["Activity Feed XML Example"](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)  
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)  
- [Vorlagenvariablen](template-variables.md) 
- [Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [Outlook XML-Schema des Connectoranbieters für soziale Netzwerke](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

