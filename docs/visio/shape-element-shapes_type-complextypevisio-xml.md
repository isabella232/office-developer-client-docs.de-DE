---
title: FormElement (Shapes_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Enthält Elemente, die ein Shape in einen Master, eine Seite oder eine Gruppe Form-Element definieren.
ms.openlocfilehash: 8c0a288858e2aaccbd3afadcdc1b057565dd30ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798022"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>FormElement (Shapes_Type ComplexType) ("Visio XML")

Enthält Elemente, die ein Shape in einen **Master**, eine **Seite**oder eine Gruppe Form-Element definieren.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Seite # .xml, Gestaltungsvorlagen # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Datentyp](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebiger Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einem Shape bereitzustellen.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Datentyp](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebiger Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einem Shape bereitzustellen.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Datentyp](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebiger Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einem Shape bereitzustellen.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |MIME (Multipurpose Internet Mail Extensions) codierten BLOB von Bilddaten wie Windows-Metadatei, Bitmap oder OLE-Daten enthält.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von verwandten Eigenschaften an.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Enthält den Text eines Shapes.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ENTF  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Ein Flag zurück, der angibt, ob das Element lokal gelöscht wird.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|FillStyle  <br/> |XSD:unsignedInt  <br/> ||Die ID des Stylesheets, die von der Formatierung ausfüllen dieses Shape erbt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements in seinem übergeordneten Element.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der Name des Benutzers angepasst wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|IsCustomNameU  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name durch den Benutzer angepasst wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|LineStyle  <br/> |XSD:unsignedInt  <br/> ||Die ID des Stylesheets, die von der Formatierung von Linie dieses Shape erbt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Master  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die ID des Master-Shapes Element von der Form seine Daten erbt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|MasterShape  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Die ID des Master-Shapes Element von der Form seine Daten erbt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|NameU  <br/> |XSD: String  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des Typs xsd: String.  <br/> |
|TextStyle  <br/> |XSD:unsignedInt  <br/> ||Die ID des Stylesheets, von denen dieses Shape-Text-Formatierung erbt.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Typ  <br/> |XSD:Token  <br/> |Optional  <br/> |Der Typ eines Shapes. Es kann einen der folgenden Werte sein: Gruppe, der Form, Handbuch oder Fremd.  <br/> |Werte des Typs Xsd:token.  <br/> |
|UniqueID  <br/> |XSD: String  <br/> |Optional  <br/> |Eine GUID (globally unique Identifier), mit dem Shape zugewiesen ist.  <br/> |Werte des Typs xsd: String.  <br/> |
   

