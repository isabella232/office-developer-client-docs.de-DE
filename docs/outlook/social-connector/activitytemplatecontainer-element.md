---
title: ActivityTemplateContainer Element
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 74662f25-5e18-4d0b-999c-a144427ad9e3
description: Ein ActivityTemplateContainer-Element ist eine Vorlage, mit dem Sie Ihre Aktivitätsfeed Elemente formatieren und Wiederverwendung von XML, das ein Layout angibt.
ms.openlocfilehash: e744bb1bdb828003cdda7086468533b32b4bf20f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19795959"
---
# <a name="activitytemplatecontainer-element"></a>ActivityTemplateContainer Element

Ein **ActivityTemplateContainer** -Element ist eine Vorlage, mit dem Sie Ihre Aktivitätsfeed Elemente formatieren und Wiederverwendung von XML, das ein Layout angibt. Verwenden Sie IDs (**ApplicationID** und **TemplateID**), der ein feed-Element (**ActivityDetails**) zu einer Vorlage (**ActivityTemplateContainer**) entspricht. Speichern Sie die Layoutdaten als Teil des **ActivityTemplate** -Elements. Verwenden von Vorlagenvariablen Daten verweisen möchten, die von den einzelnen Aktivitätsfeed-Element abgerufen wird, als Platzhalter für Informationen wie Personen, Links und Text. 
  
In der folgenden Tabelle werden die drei Elemente, die das **ActivityTemplateContainer** -Element muss beschrieben. 
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**applicationID** <br/> |Einer der beiden eindeutigen IDs, Abgleich mit dem feed Element mit der Vorlage verwendet werden. Wenn Sie mehrere Anwendungen oder andere Gruppen verfügen, kann dies als Organisator einer Vorlage der ersten Ebene verwendet werden.  <br/> |
|**templateID** <br/> |Die zweite eindeutige ID, die entsprechend das feed Element mit der Vorlage verwendet wird. Dies kann als Organisator einer L2-Vorlage verwendet werden.  <br/> |
|**activityTemplate** <br/> |Das Layout der Vorlage (**Symbol**, **Titel**und **Daten** Elemente) und den Typ der Aktivität (**Type** -Element).  <br/> |
   
In der folgenden Tabelle werden die untergeordneten Elemente des **ActivityTemplate**, die beschreiben, die das Layout und den Typ einer Vorlage beschrieben.
  
|**Element**|**Beschreibung**|
|:-----|:-----|
|**icon** <br/> |Ein Link-Token, die die URL für das Symbol für den feed Artikel verweist.  <br/> |
|**title** <br/> |Die erforderlichen Informationen für den feed Artikel.  <br/> |
|**type** <br/> |Der Typ der Aktivität, wie etwa die Aktualisierung von Status, Foto oder Dokument.  <br/> |
|**data** <br/> |Zusätzliche Informationen für den feed Artikel, wie Bilder, Text oder Links.  <br/> |
   
Ein Beispiel der Aktivität XML-feed, finden Sie unter [Aktivität Feed XML-Beispiel](activity-feed-xml-example.md)
  
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML-Code für eine Aktivität Element-Feed](overview-of-xml-for-an-activity-feed-item.md)  
- [ActivityDetails Element](activitydetails-element.md)  
- [Vorlagenvariablen](template-variables.md)  
- [Richtlinien für das Aktivitäten ordnungsgemäß anzeigen](guidelines-for-properly-displaying-activities.md)  
- [XML-Code für Aktivitäten](xml-for-activities.md)  
- [Outlook Connector für soziale Netzwerke Anbieter XML-Schema](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

