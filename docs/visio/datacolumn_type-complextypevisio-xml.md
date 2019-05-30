---
title: DataColumn_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: 7f35cd2ef1f6d710644033599fe4a90a0f2978ef
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541211"
---
# <a name="datacolumntype-complextype-visio-xml"></a>DataColumn_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
      <xs:complexType name="DataColumn_Type">
    <xs:attribute name="ColumnNameID"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="Label"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="OrigLabel"
  type="xsd:string"
    />
    <xs:attribute name="LangID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Calendar"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="DataType"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="UnitType"
  type="xsd:string"
    />
    <xs:attribute name="Currency"
  type="xsd:unsignedShort"
    />
    <xs:attribute name="Degree"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayWidth"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="DisplayOrder"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Mapped"
  type="xsd:boolean"
    />
    <xs:attribute name="Hyperlink"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kalender  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> ||Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Spaltenname  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> ||Werte des Typs XSD: String.  <br/> |
|Währung  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> ||Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|DataType  <br/> |XSD: unsignedShort abgeleitet  <br/> |Optional  <br/> ||Werte des XSD: unsignedShort abgeleitet-Typs.  <br/> |
|Degree  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
|Display Order  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
|DisplayWidth  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
|Hyperlink  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
|Label  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> ||Werte des Typs XSD: String.  <br/> |
|LangID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
|Zugeordnet  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> ||Werte des Typs XSD: String.  <br/> |
|OrigLabel  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des Typs XSD: String.  <br/> |
|UnitType  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des Typs XSD: String.  <br/> |
   

