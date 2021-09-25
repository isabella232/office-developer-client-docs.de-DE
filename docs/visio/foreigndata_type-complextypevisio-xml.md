---
title: ForeignData_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21b394a6-6f95-fc17-482c-4cb648a0d9bb
ms.openlocfilehash: 95fbb82360d70fcc442965f34d39bd5347fc10c8
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628304"
---
# <a name="foreigndata_type-complextype-visio-xml"></a>ForeignData_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Rel](rel-element-foreigndata_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CompressionLevel  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des Typs "xsd:double".  <br/> |
|CompressionType  <br/> |xsd:token  <br/> |Optional  <br/> ||Werte des Typs "xsd:token".  <br/> |
|ExtentX  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des Typs "xsd:double".  <br/> |
|ExtentY  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des Typs "xsd:double".  <br/> |
|ForeignType  <br/> |xsd:token  <br/> |Erforderlich  <br/> ||Werte des Typs "xsd:token".  <br/> |
|Mappingmode  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedShort".  <br/> |
|ObjectHeight  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des Typs "xsd:double".  <br/> |
|ObjectType  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|ObjectWidth  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des Typs "xsd:double".  <br/> |
|ShowAsIcon  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
   

