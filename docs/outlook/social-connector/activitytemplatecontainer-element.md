---
title: activityTemplateContainer-Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Ein activityTemplateContainer-Element ist eine Vorlage, mit der Sie Aktivitätsfeedelemente formatieren und XML wiederverwenden können, das ein Layout angibt.
ms.openlocfilehash: 7b0d8e8d995721e3a58b3b0db1bb7b403be445dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583051"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer-Element

Ein **activityTemplateContainer-Element** ist eine Vorlage, mit der Sie Aktivitätsfeedelemente formatieren und XML wiederverwenden können, das ein Layout angibt. Verwenden Sie IDs (**applicationID** und **templateID**), um ein Feedelement (**activityDetails**) mit einer Vorlage (**activityTemplateContainer**) zuzuordnen. Store die Layoutdaten als Teil des **activityTemplate-Elements.** Um auf Daten zu verweisen, die aus dem einzelnen Aktivitätsfeedelement abgerufen werden, verwenden Sie Vorlagenvariablen als Platzhalter für Informationen wie Personen, Links und Text. 
  
In der folgenden Tabelle werden die drei Elemente beschrieben, die für das **activityTemplateContainer-Element** erforderlich sind. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**Applicationid** <br/> |Eine von zwei eindeutigen IDs, die verwendet werden, um das Feedelement mit seiner Vorlage zuzuordnen. Wenn Sie über mehrere Anwendungen oder andere Gruppierungen verfügen, kann dies als Vorlagenorganisation der ersten Ebene verwendet werden.  <br/> |
|**templateID** <br/> |Die zweite eindeutige ID, die verwendet wird, um das Feedelement mit seiner Vorlage zuzuordnen. Dies kann als Organisator der zweiten Ebene von Vorlagen verwendet werden.  <br/> |
|**activityTemplate** <br/> |Das Layout der Vorlage (**Symbol,** **Titel** und **Datenelemente)** und der Aktivitätstyp (**Typelement).**  <br/> |
   
In der folgenden Tabelle werden die untergeordneten Elemente von **activityTemplate** beschrieben, die das Layout und den Typ einer Vorlage beschreiben.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**icon** <br/> |Ein Linktoken, das auf die URL für das Symbol für dieses Feedelement verweist.  <br/> |
|**title** <br/> |Die erforderlichen Informationen für das Feedelement.  <br/> |
|**type** <br/> |Der Typ der Aktivität, z. B. eine Aktualisierung von Status, Foto oder Dokument.  <br/> |
|**data** <br/> |Alle zusätzlichen Informationen für das Feedelement, z. B. Bilder, Text oder Links.  <br/> |
   
Ein Beispiel für den Aktivitätsfeed-XML-Code finden Sie unter ["Activity Feed XML Example"](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails-Element](activitydetails-element.md)  
- [Vorlagenvariablen](template-variables.md)  
- [Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [Outlook XML-Schema des Connectoranbieters für soziale Netzwerke](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

