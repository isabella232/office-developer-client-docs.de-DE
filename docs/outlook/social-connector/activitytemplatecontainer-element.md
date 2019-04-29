---
title: activityTemplateContainer-Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Ein activityTemplateContainer-Element ist eine Vorlage, mit der Sie Ihre Aktivitätsfeed-Elemente formatieren und XML wieder verwenden können, das ein Layout angibt.
ms.openlocfilehash: c2540b1d871e440e8f8f343a1788194c32d7dcc2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413717"
---
# <a name="activitytemplatecontainer-element"></a>activityTemplateContainer-Element

Ein **activityTemplateContainer** -Element ist eine Vorlage, mit der Sie Ihre Aktivitätsfeed-Elemente formatieren und XML wieder verwenden können, das ein Layout angibt. Verwenden Sie IDs (**applicationID** und **Template**-ID), um ein Feedelement (**ActivityDetails**) einer Vorlage (**activityTemplateContainer**) zuzuordnen. Speichern Sie die Layoutdaten als Teil des **activityTemplate** -Elements. Wenn Sie auf Daten verweisen möchten, die aus dem einzelnen Aktivitäts Feedelement abgerufen werden, verwenden Sie Vorlagenvariablen als Platzhalter für Informationen wie Personen, Links und Text. 
  
In der folgenden Tabelle werden die drei Elemente beschrieben, die das **activityTemplateContainer** -Element benötigt. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**applicationID** <br/> |Eine von zwei eindeutigen IDs, die verwendet werden, um das Feedelement mit seiner Vorlage abzugleichen. Wenn Sie mehrere Anwendungen oder andere Gruppierungen haben, kann dies als eine Vorlage Organizer der ersten Ebene verwendet werden.  <br/> |
|**templateID** <br/> |Die zweite eindeutige ID, die verwendet wird, um das Feedelement mit seiner Vorlage abzugleichen. Dieser kann als Organisator einer Vorlage für die zweite Ebene verwendet werden.  <br/> |
|**activityTemplate** <br/> |Das Layout der Vorlage (**Symbol**-, **Titel**-und **Daten** Elemente) und der Aktivitätstyp (**Type** -Element).  <br/> |
   
In der folgenden Tabelle werden die untergeordneten Elemente von **activityTemplate**beschrieben, die das Layout und den Typ einer Vorlage beschreiben.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**icon** <br/> |Ein Link-Token, das die URL für das Symbol für dieses Feed-Element referenziert.  <br/> |
|**title** <br/> |Die erforderlichen Informationen für das Feedelement.  <br/> |
|**Typ** <br/> |Der Aktivitätstyp, beispielsweise eine Aktualisierung des Status, des Fotos oder Dokuments.  <br/> |
|**data** <br/> |Alle zusätzlichen Informationen für das Feed-Element, wie Bilder, Text oder Links.  <br/> |
   
Ein Beispiel für Aktivitäts-Feed-XML finden Sie unter [Aktivitätsfeed-XML-Beispiel](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitäts Feed-Element](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails-Element](activitydetails-element.md)  
- [Vorlagenvariablen](template-variables.md)  
- [Richtlinien für die OrdnungsGemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [XML-Schema des Anbieters für soziale Netzwerke in Outlook](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

