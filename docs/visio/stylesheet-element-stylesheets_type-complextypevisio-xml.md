---
title: StyleSheet-Element (StyleSheets_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 323e1ccd-8ddd-46d3-1032-5d68d01cf4bd
description: Repräsentiert eine in einem Dokument definierte Formatvorlage.
ms.openlocfilehash: af1f8270be28e7edabf22d93471517531f5cc226
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384570"
---
# <a name="stylesheet-element-stylesheetstype-complextype-visio-xml"></a>StyleSheet-Element (StyleSheets_Type ComplexType) ("Visio XML")

Repräsentiert eine in einem Dokument definierte Formatvorlage.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="StyleSheet" Type="StyleSheet_Type" minOccurs="0" maxOccurs="unbounded" ></xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[StyleSheets](stylesheets-element-visiodocument_type-complextypevisio-xml.md) <br/> |[StyleSheets_Type](stylesheets_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **StyleSheet** -Elemente für das Dokument an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von verwandten Eigenschaften an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|FillStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements, das von der Formatierung ausfüllen dieses Format erbt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements in seinem übergeordneten Element.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der Name des Benutzers angepasst wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name durch den Benutzer angepasst wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements von der Formatierung von Linie dieses Format erbt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die ID des StyleSheet-Elements aus dem Text-Formatierung dieses Format erbt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

