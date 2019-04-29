---
title: Vorlagenvariablen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instanzen von Vorlagenvariablen (dargestellt durch ein templateVariable-Element) geben die Daten eines Aktivitätsfeed-Elements in einer Aktivitätsvorlage an.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404372"
---
# <a name="template-variables"></a>Vorlagenvariablen

Instanzen von Vorlagenvariablen (dargestellt durch ein **templateVariable** -Element) geben die Daten eines Aktivitätsfeed-Elements in einer Aktivitätsvorlage an. 
  
Ein Beispiel für Aktivitäts-Feed-XML finden Sie unter [Activity Feed XML example](activity-feed-xml-example.md).

In der folgenden Tabelle sind die Typen der unterstützten Vorlagenvariablen aufgeführt, die jeweils durch den entsprechenden XML-Enumerationswert dargestellt werden.
  
|**Typ der Vorlagenvariablen**|**Beschreibung**|
|:-----|:-----|
|**entityVariable** <br/> |Eine Person, eine Gruppe oder ein Ding.  <br/> |
|**linkVariable** <br/> |Link.  <br/> |
|**listVariable** <br/> |Eine Gruppe von Objekten.  <br/> |
|**pictureVariable** <br/> |Ein Bild.  <br/> |
|**publisherVariable** <br/> |Der Herausgeber des Aktivitätsfeed-Elements.  <br/> |
|**Textvariable** <br/> |Ein TextBlock.  <br/> |
   
Jeder Typ von Template-Variablen verfügt über erforderliche Elemente, um die Daten zu dieser Variablen anzugeben. Vorlagenvariablen werden wie folgt festgelegt:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Listenvorlagen Variable

Sie können Vorlagenvariablen, die in einer Liste enthalten sind (durch die Elemente **listVariable** und **ListItems** getrennt) wie folgt angeben: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Eine Vorlagenvariable des **listVariable** -Typs ist ein Container für Objekte. Sie kann durch trennzeichengetrennte Elemente (vom Typ **linkVariable** oder Textvariable) oder Bilder (vom Typ **pictureVariable** ) enthalten. **** Listen können bis zu fünf Link Elemente, fünf Textelemente oder fünf Bilder enthalten. 
  
Der Outlook Connector für soziale Netzwerke (OSC) lokalisiert Verknüpfungs-oder Textlisten Elemente entsprechend dem Windows-Systemgebietsschema.
  
Um Bilder in einem Aktivitätsfeed-Element richtig zu analysieren und anzuzeigen, müssen Sie Bilder in eine Liste aufnehmen. Alle Bilder werden um 52 Pixel hoch geändert. Die Größe des Bilds wird nicht geändert.
  
## <a name="template-variable-elements"></a>Vorlagenvariable Elemente

In diesem Abschnitt werden die erforderlichen und optionalen Elemente erläutert, die für die einzelnen Vorlagenvariablen Typen unterstützt werden.
  
### <a name="entityvariable"></a>entityVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**id** <br/> |Die eindeutige ID des Benutzers. Erforderlich.  <br/> |
|**nameHint** <br/> |Der Name, der im Feedelement angezeigt werden soll. Optional.  <br/> |
|**profileUrl** <br/> |Die URL des Profils der Person, die als Hyperlink für den Namen der Person im Feedelement verwendet wird, wenn der Name der Person vorhanden ist. Optional.  <br/> |
|**emailAddress** <br/> |Die e-Mail-Adresse, die zum Aktualisieren der Kontaktinformationen dieser Person in Outlook verwendet wird. Optional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**value** <br/> |Die URL für diesen Link. Erforderlich.  <br/> |
|**text** <br/> |Der Linktext, der anstelle der URL selbst angezeigt werden soll. Optional.  <br/> |
   
### <a name="listvariable"></a>listVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**listItems** <br/> |Ein Container für Elemente in der Liste. Erforderlich.  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**value** <br/> |Die URL für das Bild. Erforderlich.  <br/> |
|**altText** <br/> |Der Alternative Text, der für die Eingabehilfen angezeigt werden soll, und beim Bewegen des Mauszeigers über das Bild. Optional.  <br/> |
|**href** <br/> |Der Hyperlink, der verwendet werden soll, wenn der Benutzer auf das Bild klickt, wenn das gewünschte Ziel nicht die vom **value** -Element angegebene Bild-URL ist. Optional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**id** <br/> |Die eindeutige ID des Benutzers. Erforderlich.  <br/> |
|**nameHint** <br/> |Der Name, der im Feedelement angezeigt werden soll. Optional.  <br/> |
|**profileUrl** <br/> |Die URL des Profils der Person, die als Hyperlink für den Namen der Person im Feedelement verwendet wird, wenn der Name der Person vorhanden ist. Optional.  <br/> |
|**emailAddress** <br/> |Die e-Mail-Adresse, die zum Aktualisieren der Kontaktinformationen dieser Person in Outlook verwendet wird. Optional.  <br/> |
   
### <a name="textvariable"></a>Textvariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**value** <br/> |Der anzuzeigende Text. Optional.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitäts Feed-Element](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails-Element](activitydetails-element.md)  
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)  
- [Richtlinien für die OrdnungsGemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [XML-Schema des Anbieters für soziale Netzwerke in Outlook](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

