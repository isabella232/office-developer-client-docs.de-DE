---
title: Shape-Element (Shapes_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Enthält Elemente, die eine Form in einem Master-Shape, einem Seiten-oder Gruppen-Shape-Element definieren.
ms.openlocfilehash: aa7ffa539c9f82adc486bd0848dda66798bac165
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542072"
---
# <a name="shape-element-shapestype-complextype-visio-xml"></a>Shape-Element (Shapes_Type complexType) (Visio XML)

Enthält Elemente, die eine Form in einem **Master**-Shape, einem **Seiten**-oder Gruppen-Shape-Element definieren.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Seite #. XML, Master #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen an.  <br/> |
|[Shapes](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_type](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebigen Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einer Form bereitzustellen.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_type](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebigen Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einer Form bereitzustellen.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_type](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebigen Zeichenfolgenwert, der verwendet wird, um zusätzliche Informationen zu einer Form bereitzustellen.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Enthält eine MIME-codierte BLOB-Datei (Multipurpose Internet Mail Extensions) wie Windows Metafile, Bitmap oder OLE-Daten.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung verwandter Eigenschaften an.  <br/> |
|[Shapes](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen an.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_type](text_type-complextypevisio-xml.md) <br/> |Enthält den Text eines Shapes.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Ein Flag, das angibt, ob das Element lokal gelöscht wird.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|FillStyle  <br/> |XSD: unsignedInt  <br/> ||Die ID des Stylesheets, von dem dieses Shape die Füllungsformatierung erbt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Iscustomname  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der Name vom Benutzer angepasst wurde.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|IsCustomNameU  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name vom Benutzer angepasst wurde..  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|LineStyle  <br/> |XSD: unsignedInt  <br/> ||Die ID des Stylesheets, von dem dieses Shape die Linienformatierung erbt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Master  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die ID des Master-Elements, aus dem das Shape seine Daten erbt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|MasterShape  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die ID des Master-Elements, aus dem das Shape seine Daten erbt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs XSD: String.  <br/> |
|NameU  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der universelle Name des-Elements.  <br/> |Werte des Typs XSD: String.  <br/> |
|TextStyle  <br/> |XSD: unsignedInt  <br/> ||Die ID des Stylesheets, von dem dieses Shape die Textformatierung erbt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Typ  <br/> |XSD: Token  <br/> |Optional  <br/> |Der Typ eines Shapes. Es kann einer der folgenden Werte sein: Group, Shape, Guide oder Foreign.  <br/> |Werte des XSD: Token-Typs.  <br/> |
|UniqueID  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Eine GUID (Globally Unique Identifier), die dem Shape zugewiesen ist.  <br/> |Werte des Typs XSD: String.  <br/> |
   

