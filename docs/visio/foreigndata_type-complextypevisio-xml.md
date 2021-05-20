---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 39396ef0db5b78d6f32d8828103eecd105f8b91d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539863"
---
# <a name="foreigndata_type-complextype-visio-xml"></a>ForeignData_Type complexType (Visio XML)

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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des xsd:double-Typs.  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |Optional  <br/> ||Werte des xsd:token-Typs.  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des xsd:double-Typs.  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des xsd:double-Typs.  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |erforderlich  <br/> ||Werte des xsd:token-Typs.  <br/> |
|MappingMode  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs xsd:unsignedShort.  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des xsd:double-Typs.  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des xsd:double-Typs.  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des typs xsd:boolean.  <br/> |
   

