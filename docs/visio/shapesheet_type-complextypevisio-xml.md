---
title: ShapeSheet_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: fb394861-34d7-b7dd-1298-0c68a008528d
ms.openlocfilehash: c0086a6c2f67e6f9da62d08c195f9abfca350e5c
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59627464"
---
# <a name="shapesheet_type-complextype-visio-xml"></a>ShapeSheet_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Sheet_Type  <br/> |
   
## <a name="definition"></a>Definition

```XML
          <xs:complexType name="ShapeSheet_Type">
          
          <xs:complexContent>
          <xs:extension base="Sheet_Type">
          <xs:sequence>
    <xs:element name="Shapes"  type="Shapes_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Text"  type="Text_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data1"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data2"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Data3"  type="Data_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="ForeignData"  type="ForeignData_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="OriginalID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Del"
  type="xsd:boolean"
    />
    <xs:attribute name="MasterShape"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Master"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Type"
  type="xsd:token"
    />
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Data1](data1-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_type](data_type-complextypevisio-xml.md) <br/> ||
|[Data2](data2-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_type](data_type-complextypevisio-xml.md) <br/> ||
|[Data3](data3-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Data_type](data_type-complextypevisio-xml.md) <br/> ||
|[ForeignData](foreigndata-element-shapesheet_type-complextypevisio-xml.md) <br/> |[ForeignData_Type](foreigndata_type-complextypevisio-xml.md) <br/> ||
|[Formen](shapes-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Shapes_Type](shapes_type-complextypevisio-xml.md) <br/> ||
|[Text](text-element-shapesheet_type-complextypevisio-xml.md) <br/> |[Text_Type](text_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|Master  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|MasterShape  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|OriginalID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|Typ  <br/> |xsd:token  <br/> |Optional  <br/> ||Werte des Typs "xsd:token".  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
   

