---
title: ForeignData_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 1d9358de2f88a1b9e035ecf4966544ea935f8b2b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797065"
---
# <a name="foreigndatatype-complextype-visio-xml"></a>ForeignData_Type ComplexType ("Visio XML")

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
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

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs xsd: Double.  <br/> |
|CompressionType  <br/> |XSD:Token  <br/> |Optional  <br/> ||Werte des Typs Xsd:token.  <br/> |
|ExtentX  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs xsd: Double.  <br/> |
|ExtentY  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs xsd: Double.  <br/> |
|ForeignType  <br/> |XSD:Token  <br/> |erforderlich  <br/> ||Werte des Typs Xsd:token.  <br/> |
|MappingMode  <br/> |XSD:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs xsd: Double.  <br/> |
|ObjectType  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedInt.  <br/> |
|ObjectWidth  <br/> |XSD: Double  <br/> |Optional  <br/> ||Werte des Typs xsd: Double.  <br/> |
|ShowAsIcon  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des Typs xsd: Boolean.  <br/> |
   

