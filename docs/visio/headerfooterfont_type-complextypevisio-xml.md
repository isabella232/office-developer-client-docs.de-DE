---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 9f67e4aaecda4cc9260e357a9da6304f849abb77
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570498"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
## <a name="definition"></a>Definition

```XML
      <xs:complexType name="HeaderFooterFont_Type">
    <xs:attribute name="Height"
  type="xsd:int"
    />
    <xs:attribute name="Width"
  type="xsd:int"
    />
    <xs:attribute name="Escapement"
  type="xsd:int"
    />
    <xs:attribute name="Orientation"
  type="xsd:int"
    />
    <xs:attribute name="Weight"
  type="xsd:int"
    />
    <xs:attribute name="Italic"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Underline"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="StrikeOut"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="CharSet"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="OutPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="ClipPrecision"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="Quality"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="PitchAndFamily"
  type="xsd:unsignedByte"
    />
    <xs:attribute name="FaceName"
  type="xsd:string"
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
|CharSet  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedByte".  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedByte".  <br/> |
|Hemmung  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des Typs "xsd:int".  <br/> |
|FaceName  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|Height  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des Typs "xsd:int".  <br/> |
|Kursiv  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedByte".  <br/> |
|Orientierung  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des Typs "xsd:int".  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedByte".  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedByte".  <br/> |
|Qualität  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedByte".  <br/> |
|Durchgestrichen  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedByte".  <br/> |
|Unterstrichen  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedByte".  <br/> |
|Schriftbreite  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des Typs "xsd:int".  <br/> |
|Width  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des Typs "xsd:int".  <br/> |
   

