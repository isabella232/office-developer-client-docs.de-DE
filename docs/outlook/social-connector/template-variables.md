---
title: Vorlagenvariablen
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6f8f6af2-c7fa-4135-9532-7af5fc643b0d
description: Instanzen von Vorlagenvariablen (dargestellt durch ein TemplateVariable-Element) angeben, die Daten von einer Aktivitätsfeed-Element in einer Aktivitätsvorlage.
ms.openlocfilehash: 99f4c2de586447fb0361e528bcd33d62b79e0fb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796106"
---
# <a name="template-variables"></a>Vorlagenvariablen

Instanzen von Vorlagenvariablen (dargestellt durch ein **TemplateVariable** -Element) angeben, die Daten von einer Aktivitätsfeed-Element in einer Aktivitätsvorlage. 
  
Ein Beispiel der Aktivität XML-feed, finden Sie unter [Aktivität Feed XML-Beispiel](activity-feed-xml-example.md).

Die folgende Tabelle zeigt den Typen von unterstützten Vorlagenvariablen, jeweils durch die entsprechende XML-Enumerationswert dargestellt.
  
|**Typ der Vorlage Variablen**|**Beschreibung**|
|:-----|:-----|
|**entityVariable** <br/> |Eine Person, eine Gruppe oder eine Sache.  <br/> |
|**linkVariable** <br/> |Eine Verknüpfung.  <br/> |
|**listVariable** <br/> |Eine Gruppe von Objekten.  <br/> |
|**pictureVariable** <br/> |Ein Bild.  <br/> |
|**publisherVariable** <br/> |Element-feed der Herausgeber der Aktivität.  <br/> |
|**textVariable** <br/> |Text-Block.  <br/> |
   
Jede Art von Vorlage Variable hat Elemente an, die Daten über diese Variable erforderlich. Vorlagenvariablen werden wie folgt angegeben:
  
`<templateVariable type="variable type">`
  
## <a name="list-template-variable"></a>Die Vorlage Listenvariable

Sie können Vorlagenvariablen angeben, die in einer Liste (getrennt durch die **ListVariable** und **ListItems** Elemente) wie folgt enthalten sind: 
  
`<simpleTemplateVariable type="variable type of text, link, or picture">`
  
Eine Vorlage Variable vom Typ **ListVariable** ist ein Container für Objekte. Sie können durch Kommas getrennte Elemente (vom Typ **LinkVariable** oder **TextVariable** ) oder Bilder (vom Typ **PictureVariable** ) enthalten. Listen können bis zu fünf Verknüpfen von Elementen, fünf Textelemente oder fünf Bilder enthalten. 
  
Outlook Social Connector (OSC) lokalisiert Link oder Text Listenelemente entsprechend des Windows-Systemgebietsschemas an.
  
Um korrekt analysiert und Anzeigen von Bildern in einer Aktivitätsfeed-Element, müssen Sie Bilder in einer Liste einbeziehen. Alle Bilder werden Größe der 52 Pixel hoch sein. Die Breite des Bilds wird nicht geändert.
  
## <a name="template-variable-elements"></a>Vorlage Variable Elemente

Dieser Abschnitt enthält die erforderlichen und optionalen Elemente für jede Art von Vorlage Variable unterstützt.
  
### <a name="entityvariable"></a>entityVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**id** <br/> |Die eindeutige ID des Benutzers. Erforderlich.  <br/> |
|**nameHint** <br/> |Der Name der feed-Element angezeigt werden. Optional.  <br/> |
|**profileUrl** <br/> |Die URL des Profils der Person, die für den Namen der Person in der feed-Element als Hyperlink verwendet wird, wenn Sie den Namen der Person vorhanden ist. Optional.  <br/> |
|**emailAddress** <br/> |Die e-Mail-Adresse, die verwendet wird, um die Kontaktinformationen dieser Person in Outlook zu aktualisieren. Optional.  <br/> |
   
### <a name="linkvariable"></a>linkVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**Value** <br/> |Die URL für diese Verknüpfung. Erforderlich.  <br/> |
|**text** <br/> |Der Linktext, anstatt die URL selbst angezeigt. Optional.  <br/> |
   
### <a name="listvariable"></a>listVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**listItems** <br/> |Ein Container für Elemente in der Liste. Erforderlich.  <br/> |
   
### <a name="picturevariable"></a>pictureVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**Value** <br/> |Die URL für das Bild. Erforderlich.  <br/> |
|**altText** <br/> |Der alternative Text für Eingabehilfen und wenn der Benutzer den Mauszeiger über das Bild bewegt angezeigt. Optional.  <br/> |
|**href** <br/> |Der Hyperlink klickt der Benutzer das Bild verwenden, wenn das gewünschte Ziel nicht die Bild-URL, die durch das **Value** -Element angegeben ist. Optional.  <br/> |
   
### <a name="publishervariable"></a>publisherVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**id** <br/> |Die eindeutige ID des Benutzers. Erforderlich.  <br/> |
|**nameHint** <br/> |Der Name der feed-Element angezeigt werden. Optional.  <br/> |
|**profileUrl** <br/> |Die URL des Profils der Person, die für den Namen der Person in der feed-Element als Hyperlink verwendet wird, wenn Sie den Namen der Person vorhanden ist. Optional.  <br/> |
|**emailAddress** <br/> |Die e-Mail-Adresse, die verwendet wird, um die Kontaktinformationen dieser Person in Outlook zu aktualisieren. Optional.  <br/> |
   
### <a name="textvariable"></a>textVariable

|**Element**|**Beschreibung**|
|:-----|:-----|
|**Name** <br/> |Der Name der Variablen. Erforderlich.  <br/> |
|**Value** <br/> |Der anzuzeigende Text. Optional.  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Übersicht über XML-Code für eine Aktivität Element-Feed](overview-of-xml-for-an-activity-feed-item.md)  
- [ActivityDetails Element](activitydetails-element.md)  
- [ActivityTemplateContainer Element](activitytemplatecontainer-element.md)  
- [Richtlinien für das Aktivitäten ordnungsgemäß anzeigen](guidelines-for-properly-displaying-activities.md)  
- [XML-Code für Aktivitäten](xml-for-activities.md)  
- [Outlook Connector für soziale Netzwerke Anbieter XML-Schema](outlook-social-connector-provider-xml-schema.md)
- [Entwickeln eines Providers mit dem OSC-XML-Schema](developing-a-provider-with-the-osc-xml-schema.md)

