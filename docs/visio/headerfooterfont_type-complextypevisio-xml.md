---
title: HeaderFooterFont_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: cc51924aa68e3248583be5f717b5813d4a32af2b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335623"
---
# <a name="headerfooterfonttype-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (' Visio XML ')

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
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

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> ||Werte des XSD: unsignedByte-Typs.  <br/> |
|ClipPrecision  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> ||Werte des XSD: unsignedByte-Typs.  <br/> |
|Hemmung  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des XSD: int-Typs.  <br/> |
|FaceName  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|Height  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des XSD: int-Typs.  <br/> |
|Kursiv  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> ||Werte des XSD: unsignedByte-Typs.  <br/> |
|Orientierung  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des XSD: int-Typs.  <br/> |
|OutPrecision  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> ||Werte des XSD: unsignedByte-Typs.  <br/> |
|PitchAndFamily  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> ||Werte des XSD: unsignedByte-Typs.  <br/> |
|Quality  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> ||Werte des XSD: unsignedByte-Typs.  <br/> |
|Durchgestrichen  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> ||Werte des XSD: unsignedByte-Typs.  <br/> |
|Unterstrichen  <br/> |XSD: unsignedByte  <br/> |Optional  <br/> ||Werte des XSD: unsignedByte-Typs.  <br/> |
|Schriftbreite  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des XSD: int-Typs.  <br/> |
|Width  <br/> |XSD: int  <br/> |Optional  <br/> ||Werte des XSD: int-Typs.  <br/> |
   

