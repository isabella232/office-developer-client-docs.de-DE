---
title: Master_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 4a3dc7d6df4d0f39a40fa3fc1f02f3cfe8c9e72b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59603515"
---
# <a name="master_type-complextype-visio-xml"></a>Master_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
## <a name="definition"></a>Definition

```XML
          <xs:complexType name="Master_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Icon"  type="Icon_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="BaseID"
  type="xsd:string"
    />
    <xs:attribute name="UniqueID"
  type="xsd:string"
    />
    <xs:attribute name="MatchByName"
  type="xsd:boolean"
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
    <xs:attribute name="IconSize"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="PatternFlags"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Prompt"
  type="xsd:string"
    />
    <xs:attribute name="Hidden"
  type="xsd:boolean"
    />
    <xs:attribute name="IconUpdate"
  type="xsd:boolean"
    />
    <xs:attribute name="AlignName"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="MasterType"
  type="xsd:unsignedShort"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> ||
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-master_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedShort".  <br/> |
|BaseID  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|Hidden  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedShort".  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|Mastertype  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedShort".  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedShort".  <br/> |
|Eingabeaufforderung  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
   

