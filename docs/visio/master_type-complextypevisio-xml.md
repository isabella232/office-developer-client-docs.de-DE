---
title: Master_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d799074-13d9-3c98-3bee-b57af9966c81
ms.openlocfilehash: 186099d495849706f68113abb269de4a1f5a2ce7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341804"
---
# <a name="mastertype-complextype-visio-xml"></a>Master_Type complexType (' Visio XML ')

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
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

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> ||
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-master_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> ||Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|BaseID  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|Ausgeblendet  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
|IconSize  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> ||Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|IconUpdate  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
|IsCustomname  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
|IsCustomNameU  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
|MasterType Direktive  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> ||Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|MatchByName  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|NameU  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|PatternFlags  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> ||Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Eingabeaufforderung  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|UniqueID  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
   

