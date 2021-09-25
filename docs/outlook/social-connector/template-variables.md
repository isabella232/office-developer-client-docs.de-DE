---
title: Vorlagenvariablen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instanzen von Vorlagenvariablen (dargestellt durch ein templateVariable-Element) geben die Daten eines Aktivitätsfeedelements in einer Aktivitätsvorlage an.
ms.openlocfilehash: da52859ac8e1bc598ea517bf92d7530fced4f468
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59583002"
---
# <a name="template-variables"></a>Vorlagenvariablen

Instanzen von Vorlagenvariablen (dargestellt durch ein **templateVariable-Element)** geben die Daten eines Aktivitätsfeedelements in einer Aktivitätsvorlage an. 
  
Ein Beispiel für aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md).

In der folgenden Tabelle sind die Typen der unterstützten Vorlagenvariablen aufgeführt, die jeweils durch den entsprechenden XML-Enumerationswert dargestellt werden.
  
|**Typ der Vorlagenvariablen**|**Beschreibung**|
|:-----|:-----|
|**entityVariable** <br/> |Eine Person, gruppe oder Ding.  <br/> |
|**linkVariable** <br/> |Ein Link.  <br/> |
|**listVariable** <br/> |Eine Gruppe von Objekten.  <br/> |
|**pictureVariable** <br/> |Ein Bild.  <br/> |
|**publisherVariable** <br/> |Der Herausgeber des Aktivitätsfeedelements.  <br/> |
|**textVariable** <br/> |Ein Textblock.  <br/> |
   
Jeder Vorlagenvariablentyp verfügt über erforderliche Elemente, um die Daten zu dieser Variablen anzugeben. Vorlagenvariablen werden wie folgt angegeben:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Listenvorlagenvariable

Sie können Vorlagenvariablen, die in einer Liste enthalten sind (durch die Elemente **listVariable** und **listItems** getrennt), wie folgt angeben: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Eine Vorlagenvariable des typs **listVariable** ist ein Container für Objekte. Sie kann durch Trennzeichen getrennte Elemente (vom Typ **"linkVariable"** oder **"textVariable")** oder Bilder (vom Typ **"pictureVariable")** enthalten. Listen können bis zu fünf Linkelemente, fünf Textelemente oder fünf Bilder enthalten. 
  
Der Outlook Connector für soziale Netzwerke (OSC) lokalisiert Link- oder Textlistenelemente gemäß dem Windows Systemgebietsschema.
  
Um Bilder in einem Aktivitätsfeedelement richtig zu analysieren und anzuzeigen, müssen Sie Bilder in eine Liste einschließen. Alle Bilder werden auf eine Höhe von 52 Pixeln angepasst. Die Breite des Bilds wird nicht geändert.
  
## <a name="template-variable-elements"></a>Vorlagenvariablenelemente

In diesem Abschnitt werden die erforderlichen und optionalen Elemente behandelt, die für jeden Vorlagenvariablentyp unterstützt werden.
  
### <a name="entityvariable"></a>entityVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**id** <br/> |Die eindeutige ID des Benutzers. Erforderlich.  <br/> |
|**nameHint** <br/> |Der Name, der im Feedelement angezeigt werden soll. Optional.  <br/> |
|**profileUrl** <br/> |Die URL des Profils der Person, die als Hyperlink für den Namen der Person im Feedelement verwendet wird, wenn der Name der Person vorhanden ist. Optional.  <br/> |
|**emailAddress** <br/> |Die E-Mail-Adresse, die zum Aktualisieren der Kontaktinformationen dieser Person in Outlook verwendet wird. Optional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**value** <br/> |Die URL für diesen Link. Erforderlich.  <br/> |
|**text** <br/> |Der anzuzeigende Linktext anstelle der URL selbst. Optional.  <br/> |
   
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
|**altText** <br/> |Der alternative Text, der zur Barrierefreiheit angezeigt werden soll und wenn der Benutzer den Mauszeiger über das Bild bewegt. Optional.  <br/> |
|**href** <br/> |Der Hyperlink, der verwendet werden soll, wenn der Benutzer auf das Bild klickt, wenn das gewünschte Ziel nicht die vom **Wertelement** angegebene Bild-URL ist. Optional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**id** <br/> |Die eindeutige ID des Benutzers. Erforderlich.  <br/> |
|**nameHint** <br/> |Der Name, der im Feedelement angezeigt werden soll. Optional.  <br/> |
|**profileUrl** <br/> |Die URL des Profils der Person, die als Hyperlink für den Namen der Person im Feedelement verwendet wird, wenn der Name der Person vorhanden ist. Optional.  <br/> |
|**emailAddress** <br/> |Die E-Mail-Adresse, die zum Aktualisieren der Kontaktinformationen dieser Person in Outlook verwendet wird. Optional.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**value** <br/> |Der anzuzeigende Text. Optional.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails-Element](activitydetails-element.md)  
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)  
- [Richtlinien für die ordnungsgemäße Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [Outlook XML-Schema des Connectoranbieters für soziale Netzwerke](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

