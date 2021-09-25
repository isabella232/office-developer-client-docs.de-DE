---
title: StyleSheet-Element (StyleSheets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Repräsentiert eine in einem Dokument definierte Formatvorlage.
ms.openlocfilehash: 4a05a6c2b94f8080c339f203497995ac5c72e562
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59622767"
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **StyleSheet-Elementen** für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung verwandter Eigenschaften an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements, von dem diese Formatvorlage die Füllformatierung erbt.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der Name vom Benutzer angepasst wurde.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name vom Benutzer angepasst wurde.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements, von dem diese Formatvorlage die Zeilenformatierung erbt.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs "xsd:string".  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des Typs "xsd:string".  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements, von dem diese Formatvorlage die Textformatierung erbt.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

