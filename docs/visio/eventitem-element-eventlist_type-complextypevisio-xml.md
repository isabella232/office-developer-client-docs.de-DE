---
title: EventItem-Element (EventList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Kapselt einen Ereigniscode.
ms.openlocfilehash: 7a7c1c3ba86971f0711ef01173f8704fb6989430
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582763"
---
# <a name="eventitem-element-eventlist_type-complextype-visio-xml"></a>EventItem-Element (EventList_Type complexType) (Visio XML)

Kapselt einen Ereigniscode.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Enthält ein **EventItem-Element** für jedes Ereignis, auf das ein Objekt reagieren soll.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Aktion  <br/> |xsd:unsignedShort  <br/> |Erforderlich  <br/> |Gibt den Aktionscode des übergeordneten **EventItem-Elements** an.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|Aktiviert  <br/> |xsd:boolean  <br/> |Optional  <br/> |Stellt ein Flag dar, das angibt, ob das Ereignis aktiviert oder deaktiviert ist.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|EventCode  <br/> |xsd:unsignedShort  <br/> |Erforderlich  <br/> |Ein Code, der das Ereignis angibt, das das Add-On auslöst.  <br/> |Werte des Typs "xsd:unsignedShort".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Die ID des Ereignisses.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Ziel  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt das Ziel eines Ereignisses an.  <br/> |Werte des Typs "xsd:string".  <br/> |
|TargetArgs  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt eine Zeichenfolge mit Argumenten an, die an das Ziel eines Ereignisses gesendet werden sollen.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

