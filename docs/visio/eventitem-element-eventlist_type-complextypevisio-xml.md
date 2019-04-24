---
title: EventItem-Element (EventList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b347117-a1c1-d090-0d71-ea8528ac70c6
description: Kapselt einen Ereigniscode.
ms.openlocfilehash: 6ed539bd6cb4524b2498b636295442bed917c72a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337198"
---
# <a name="eventitem-element-eventlisttype-complextype-visio-xml"></a>EventItem-Element (EventList_Type complexType) (' Visio XML ')

Kapselt einen Ereigniscode.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[EventItem_Type](eventitem_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="EventItem" type="EventItem_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[EventList](eventlist-element-visiodocument_type-complextypevisio-xml.md) <br/> |[EventList_Type](eventlist_type-complextypevisio-xml.md) <br/> |Enthält ein **EventItem** -Element für jedes Ereignis, auf das ein Objekt reagieren soll.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Aktion  <br/> |XSD: unsignedShort abgeleitet  <br/> |erforderlich  <br/> |Gibt den Aktionscode des übergeordneten **EventItem** -Elements an.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Aktiviert  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Stellt ein Flag dar, das angibt, ob das Ereignis aktiviert oder deaktiviert ist.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|EventCode  <br/> |XSD: unsignedShort abgeleitet  <br/> |erforderlich  <br/> |Ein Code, der das Ereignis angibt, das das Add-on auslöst.  <br/> |Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die ID des Ereignisses.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Ziel  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt das Ziel eines Ereignisses an.  <br/> |Werte des XSD: String-Typs.  <br/> |
|TargetArgs  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt eine Zeichenfolge mit Argumenten an, die an das Ziel eines Ereignisses gesendet werden sollen.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

