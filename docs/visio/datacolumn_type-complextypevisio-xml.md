---
title: DataColumn_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: bee50623-cdf7-b9d7-867a-70c86922cbac
ms.openlocfilehash: a925d01365d78c899c5cd828c604a6ee18b0242b
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582841"
---
# <a name="datacolumn_type-complextype-visio-xml"></a>DataColumn_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Kalender  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedShort".  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |Erforderlich  <br/> ||Werte des Typs "xsd:string".  <br/> |
|Währung  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedShort".  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedShort".  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|Hyperlink  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|Beschriftung  <br/> |xsd:string  <br/> |Erforderlich  <br/> ||Werte des Typs "xsd:string".  <br/> |
|Langid  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|Zugeordnet  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|Name  <br/> |xsd:string  <br/> |Erforderlich  <br/> ||Werte des Typs "xsd:string".  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|Unittype  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
   

