---
title: EventItem-Element (EventList_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Einen Ereigniscode kapselt.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394398"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>EventItem-Element (EventList_Type ComplexType) ("Visio XML")

Einen Ereigniscode kapselt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Enthält ein Element **EventItem** für jedes Ereignis, der ein Objekt Antworten sollen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Aktion  <br/> |XSD:unsignedShort  <br/> |erforderlich  <br/> |Gibt an, der Aktionscode des übergeordneten Elements **EventItem** .  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|Aktiviert  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Stellt ein Flag gibt an, ob das Ereignis aktiviert oder deaktiviert ist.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|Ereigniscode  <br/> |XSD:unsignedShort  <br/> |erforderlich  <br/> |Ein Code, der das Ereignis, das das Add-on angibt.  <br/> |Werte des Typs Xsd:unsignedShort.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die ID des Ereignisses.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Ziel  <br/> |XSD: String  <br/> |erforderlich  <br/> |Gibt das Ziel eines Ereignisses an.  <br/> |Werte des Typs xsd: String.  <br/> |
|TargetArgs  <br/> |XSD: String  <br/> |erforderlich  <br/> |Gibt eine Zeichenfolge mit Argumenten, die an das Ziel eines Ereignisses gesendet werden.  <br/> |Werte des Typs xsd: String.  <br/> |
   

