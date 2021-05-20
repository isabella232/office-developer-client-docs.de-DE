---
title: Shape-Element (Shapes_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8074bd07-430a-779e-ad1f-e7e3a1c748b1
description: Enthält Elemente, die ein Shape in einem Master-, Page- oder Gruppen-Shape-Element definieren.
ms.openlocfilehash: aa7ffa539c9f82adc486bd0848dda66798bac165
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542072"
---
# <a name="shape-element-shapes_type-complextype-visio-xml"></a>Shape-Element (Shapes_Type complexType) (Visio XML)

Enthält Elemente, die ein Shape in einem **Master-,** **Page-** oder Gruppenformelement definieren.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |page#.xml, master#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Shape" type="ShapeSheet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Formen](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen an.  <br/> |
|[Formen](shapes-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebigen Zeichenfolgenwert, der zum Angeben zusätzlicher Informationen zu einem Shape verwendet wird.  <br/> |
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebigen Zeichenfolgenwert, der zum Angeben zusätzlicher Informationen zu einem Shape verwendet wird.  <br/> |
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_Type](data_type-complextypevisio-xml.md) <br/> |Enthält einen beliebigen Zeichenfolgenwert, der zum Angeben zusätzlicher Informationen zu einem Shape verwendet wird.  <br/> |
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> |Enthält einen MIME(Multipurpose Internet Mail Extensions) codierten BLOB von Bilddaten, z. B. Windows Metadatei, Bitmap- oder OLE-Daten.  <br/> |
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung verwandter Eigenschaften an.  <br/> |
|[Formen](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Formen an.  <br/> |
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> |Enthält den Text einer Form.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |Optional  <br/> |Ein Flag, das angibt, ob das Element lokal gelöscht wird.  <br/> |Werte des typs xsd:boolean.  <br/> |
|FillStyle  <br/> |xsd:unsignedInt  <br/> ||Die ID des StyleSheets, von dem dieses Shape die Füllformatierung erbt.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der Name vom Benutzer angepasst wurde.  <br/> |Werte des typs xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name vom Benutzer angepasst wurde.  <br/> |Werte des typs xsd:boolean.  <br/> |
|LineStyle  <br/> |xsd:unsignedInt  <br/> ||Die ID des StyleSheets, von dem dieses Shape die Zeilenformatierung erbt.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des Master-Elements, von dem das Shape seine Daten erbt.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des Master-Elements, von dem das Shape seine Daten erbt.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|TextStyle  <br/> |xsd:unsignedInt  <br/> ||Die ID des StyleSheets, von dem dieses Shape die Textformatierung erbt.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Typ  <br/> |xsd:token  <br/> |Optional  <br/> |Der Typ einer Form. Dies kann einer der folgenden Werte sein: Group, Shape, Guide oder Foreign.  <br/> |Werte des xsd:token-Typs.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> |Eine GUID (global eindeutiger Bezeichner), die dem Shape zugewiesen ist.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

