---
title: HeaderFooterFont_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1e4134be-fb18-768e-b477-f9f40f72548d
ms.openlocfilehash: dd99d87e0d80aad3bcde31e4834337ee59088da2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541071"
---
# <a name="headerfooterfont_type-complextype-visio-xml"></a>HeaderFooterFont_Type complexType (Visio XML)

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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CharSet  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des xsd:unsignedByte-Typs.  <br/> |
|ClipPrecision  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des xsd:unsignedByte-Typs.  <br/> |
|Escapement  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des xsd:int-Typs.  <br/> |
|FaceName  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|Height  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des xsd:int-Typs.  <br/> |
|Kursiv  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des xsd:unsignedByte-Typs.  <br/> |
|Orientierung  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des xsd:int-Typs.  <br/> |
|OutPrecision  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des xsd:unsignedByte-Typs.  <br/> |
|PitchAndFamily  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des xsd:unsignedByte-Typs.  <br/> |
|Qualität  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des xsd:unsignedByte-Typs.  <br/> |
|StrikeOut  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des xsd:unsignedByte-Typs.  <br/> |
|Unterstrichen  <br/> |xsd:unsignedByte  <br/> |Optional  <br/> ||Werte des xsd:unsignedByte-Typs.  <br/> |
|Schriftbreite  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des xsd:int-Typs.  <br/> |
|Width  <br/> |xsd:int  <br/> |Optional  <br/> ||Werte des xsd:int-Typs.  <br/> |
   

