---
title: HeaderFooterFont_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: 1d7c4d6850e4a8ea1933ae751c580d09e0dd67bd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797131"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>HeaderFooterFont_Type ComplexType ("Visio XML")

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
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

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedByte.  <br/> |
|ClipPrecision  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedByte.  <br/> |
|Vorschub  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des Typs xsd: int.  <br/> |
|FaceName  <br/> |XSD: String  <br/> |Optional  <br/> ||Werte des Typs xsd: String.  <br/> |
|Höhe  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des Typs xsd: int.  <br/> |
|Kursiv  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedByte.  <br/> |
|Ausrichtung  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des Typs xsd: int.  <br/> |
|OutPrecision  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedByte.  <br/> |
|PitchAndFamily  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedByte.  <br/> |
|Qualität  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedByte.  <br/> |
|Durchgestrichen  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedByte.  <br/> |
|Unterstrichen  <br/> |XSD:unsignedByte  <br/> |Optional  <br/> ||Werte des Typs Xsd:unsignedByte.  <br/> |
|Weight  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des Typs xsd: int.  <br/> |
|Breite  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des Typs xsd: int.  <br/> |
   

