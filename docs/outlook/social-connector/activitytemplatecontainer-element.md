---
title: activityTemplateContainer-Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Ein activityTemplateContainer-Element ist eine Vorlage, mit der Sie Ihre Aktivitätsfeedelemente formatieren und XML wiederverwenden können, das ein Layout angibt.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413717"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer-Element

Ein **activityTemplateContainer-Element** ist eine Vorlage, mit der Sie Ihre Aktivitätsfeedelemente formatieren und XML wiederverwenden können, das ein Layout angibt. Verwenden Sie IDs (**applicationID** und **templateID**), um ein Feedelement (**activityDetails**) einer Vorlage (**activityTemplateContainer**) zu entsprechen. Store Layoutdaten als Teil des **activityTemplate-Elements.** Um auf Daten zu verweisen, die aus dem einzelnen Aktivitätsfeedelement gezogen werden, verwenden Sie Vorlagenvariablen als Platzhalter für Informationen wie Personen, Links und Text. 
  
In der folgenden Tabelle werden die drei Elemente beschrieben, die das **activityTemplateContainer-Element** benötigt. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**applicationID** <br/> |Eine von zwei eindeutigen IDs, die verwendet werden, um dem Feedelement mit seiner Vorlage zu entsprechen. Wenn Sie über mehrere Anwendungen oder andere Gruppierungen verfügen, kann dies als Vorlagenorganisator der ersten Ebene verwendet werden.  <br/> |
|**templateID** <br/> |Die zweite eindeutige ID, die verwendet wird, um dem Feedelement mit seiner Vorlage zu entsprechen. Dies kann als Vorlagenorganisator der zweiten Ebene verwendet werden.  <br/> |
|**activityTemplate** <br/> |Das Layout der Vorlage (**Symbol,** **Titel** und **Datenelemente)** und der Aktivitätstyp (**Type-Element).**  <br/> |
   
In der folgenden Tabelle werden die untergeordneten Elemente von **activityTemplate** beschrieben, in denen das Layout und der Typ einer Vorlage beschrieben werden.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**icon** <br/> |Ein Linktoken, das auf die URL für das Symbol für dieses Feedelement verweist.  <br/> |
|**title** <br/> |Die erforderlichen Informationen für das Feedelement.  <br/> |
|**type** <br/> |Der Typ der Aktivität, z. B. eine Aktualisierung von Status, Foto oder Dokument.  <br/> |
|**data** <br/> |Alle zusätzlichen Informationen für das Feedelement, z. B. Bilder, Text oder Links.  <br/> |
   
Ein Beispiel für Aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails-Element](activitydetails-element.md)  
- [Vorlagenvariablen](template-variables.md)  
- [Richtlinien für die ordnungsgemäßen Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [Outlook XML-Schema des Anbieters für sozialen Connector](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

