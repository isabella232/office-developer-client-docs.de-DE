---
title: FaceName_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d24f350c-35bf-ab16-2469-39fd5344e5fe
ms.openlocfilehash: 8035f541e619360403336bd2fbd931cf05dbfe59
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322554"
---
# <a name="facenametype-complextype-visio-xml"></a>FaceName_Type complexType (' Visio XML ')

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
      <xs:complexType name="FaceName_Type">
    <xs:attribute name="NameU"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="UnicodeRanges"
  type="xsd:string"
    />
    <xs:attribute name="CharSets"
  type="xsd:string"
    />
    <xs:attribute name="Panos"
  type="xsd:string"
    />
    <xs:attribute name="Panose"
  type="xsd:string"
    />
    <xs:attribute name="Flags"
  type="xsd:unsignedInt"
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
|CharSets  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|Flags  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
|NameU  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> ||Werte des XSD: String-Typs.  <br/> |
|PANOS  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|Panose  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|Unicode Ranges  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
   

