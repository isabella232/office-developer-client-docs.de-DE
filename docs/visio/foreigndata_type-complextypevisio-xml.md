---
title: ForeignData_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 6630c8b33dc1c4c7cbb12bb9727d4f0b1e1b19d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32346011"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ForeignData_Type complexType (' Visio XML ')

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
          <xs:complexType name="ForeignData_Type">
          
          <xs:sequence>
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:sequence>
    <xs:attribute name="ForeignType"
  type="xsd:token"
     use="required"
    />
    <xs:attribute name="ObjectType"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ShowAsIcon"
  type="xsd:boolean"
    />
    <xs:attribute name="ObjectWidth"
  type="xsd:double"
    />
    <xs:attribute name="ObjectHeight"
  type="xsd:double"
    />
    <xs:attribute name="MappingMode"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="ExtentX"
  type="xsd:double"
    />
    <xs:attribute name="ExtentY"
  type="xsd:double"
    />
    <xs:attribute name="CompressionType"
  type="xsd:token"
    />
    <xs:attribute name="CompressionLevel"
  type="xsd:double"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs XSD: Double.  <br/> |
|CompressionType  <br/> |XSD: Token  <br/> |Optional  <br/> ||Werte des XSD: Token-Typs.  <br/> |
|ExtentX  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs XSD: Double.  <br/> |
|Umfang  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs XSD: Double.  <br/> |
|ForeignType  <br/> |XSD: Token  <br/> |erforderlich  <br/> ||Werte des XSD: Token-Typs.  <br/> |
|MappingMode  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> ||Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|ObjectHeight  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs XSD: Double.  <br/> |
|ObjectType  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
|ObjectWidth  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs XSD: Double.  <br/> |
|ShowAsIcon  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
   

