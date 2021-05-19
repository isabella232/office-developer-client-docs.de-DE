---
title: StyleSheet-Element (StyleSheets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Repräsentiert eine in einem Dokument definierte Formatvorlage.
ms.openlocfilehash: 939180d24972ae68d01b2a707e7806380b706d14
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541939"
---
# <a name="stylesheet-element-stylesheets_type-complextype-visio-xml"></a>StyleSheet-Element (StyleSheets_Type complexType) (Visio XML)

Repräsentiert eine in einem Dokument definierte Formatvorlage.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **StyleSheet-Elementen** für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung verwandter Eigenschaften an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements, von dem diese Formatvorlage die Füllformatierung erbt.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der Name vom Benutzer angepasst wurde.  <br/> |Werte des typs xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name vom Benutzer angepasst wurde.  <br/> |Werte des typs xsd:boolean.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements, von dem diese Formatvorlage die Zeilenformatierung erbt.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements, von dem diese Formatvorlage die Textformatierung erbt.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
   

