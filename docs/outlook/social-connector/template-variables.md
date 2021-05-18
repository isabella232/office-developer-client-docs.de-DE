---
title: Vorlagenvariablen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instanzen von Vorlagenvariablen (dargestellt durch ein templateVariable-Element) geben die Daten eines Aktivitätsfeedelements in einer Aktivitätsvorlage an.
ms.openlocfilehash: 9b37665488f0f1e2bd205fb7d4a5d2201697d7c8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404372"
---
# <a name="template-variables"></a>Vorlagenvariablen

Instanzen von Vorlagenvariablen (dargestellt durch ein **templateVariable-Element)** geben die Daten eines Aktivitätsfeedelements in einer Aktivitätsvorlage an. 
  
Ein Beispiel für aktivitätsfeed-XML finden Sie unter [Activity Feed XML Example](activity-feed-xml-example.md).

Die folgende Tabelle zeigt die Typen unterstützter Vorlagenvariablen, die jeweils durch den entsprechenden XML-Enumerationswert dargestellt werden.
  
|**Typ der Vorlagenvariable**|**Beschreibung**|
|:-----|:-----|
|**entityVariable** <br/> |Eine Person, Eine Gruppe oder eine Sache.  <br/> |
|**linkVariable** <br/> |Ein Link.  <br/> |
|**listVariable** <br/> |Eine Gruppe von Objekten.  <br/> |
|**pictureVariable** <br/> |Ein Bild.  <br/> |
|**publisherVariable** <br/> |Der Herausgeber des Aktivitätsfeedelements.  <br/> |
|**textVariable** <br/> |Ein Textblock.  <br/> |
   
Jeder Typ von Vorlagenvariablen verfügt über erforderliche Elemente, um die Daten zu dieser Variablen anzugeben. Vorlagenvariablen werden wie folgt angegeben:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Vorlagenvariable auflisten

Sie können Vorlagenvariablen angeben, die in einer Liste enthalten sind (durch die **Elemente listVariable** und **listItems** getrennt) wie folgt: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Eine Vorlagenvariable des **Typs listVariable** ist ein Container für Objekte. Sie kann durch Trennzeichen getrennte Elemente (vom **Typ linkVariable** oder **textVariable)** oder Bilder (vom **Typ pictureVariable)** enthalten. Listen können bis zu fünf Linkelemente, fünf Textelemente oder fünf Bilder enthalten. 
  
Der Outlook Social Connector (OSC) lokalisiert Link- oder Textlistenelemente gemäß dem Windows-System-Locale.
  
Zum ordnungsgemäßen Analysieren und Anzeigen von Bildern in einem Aktivitätsfeedelement müssen Sie Bilder in eine Liste hinzufügen. Alle Bilder werden auf eine Höhe von 52 Pixeln geändert. Die Breite des Bilds wird nicht geändert.
  
## <a name="template-variable-elements"></a>Vorlagenvariablenelemente

In diesem Abschnitt werden die erforderlichen und optionalen Elemente behandelt, die für jeden Typ von Vorlagenvariablen unterstützt werden.
  
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
|**altText** <br/> |Der alternative Text, der für die Barrierefreiheit angezeigt werden soll und wenn der Benutzer den Mauszeiger über das Bild bewegt. Optional.  <br/> |
|**href** <br/> |Der Hyperlink, der verwendet werden soll, wenn der Benutzer auf das Bild klickt, wenn das gewünschte Ziel nicht die vom **Value-Element** angegebene Bild-URL ist. Optional.  <br/> |
   
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
|**value** <br/> |Der zu zeigende Text. Optional.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML für ein Aktivitätsfeedelement](overview-of-xml-for-an-activity-feed-item.md)  
- [activityDetails-Element](activitydetails-element.md)  
- [activityTemplateContainer-Element](activitytemplatecontainer-element.md)  
- [Richtlinien für die ordnungsgemäßen Anzeige von Aktivitäten](guidelines-for-properly-displaying-activities.md)  
- [XML für Aktivitäten](xml-for-activities.md)  
- [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

