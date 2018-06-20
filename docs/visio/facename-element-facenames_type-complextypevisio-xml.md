---
title: FaceName-Element (FaceNames_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Enthält Informationen zu einer Schriftart.
ms.openlocfilehash: 8a66d5294e239e4540939cc7053e1f67a777144d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796955"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>FaceName-Element (FaceNames_Type ComplexType) ("Visio XML")

Enthält Informationen zu einer Schriftart.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **FaceName** -Elementen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Zeichensätze  <br/> |XSD: String  <br/> |Optional  <br/> |Unterstützte Zeichensätze der Schriftart.  <br/> |Werte des Typs xsd: String.  <br/> |
|Flags  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Flags, die Folgendes angeben: fehlende Schriftart, Standardschriftart, asiatischen Schriftart, komplexe Schriftart, vertikalen Schriftart und der Schriftarttyp.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|NameU  <br/> |XSD: String  <br/> |erforderlich  <br/> |Der Name der Schriftart als UTF-16 Unicode-Zeichenfolge.  <br/> ||
|Panos  <br/> |XSD: String  <br/> |Optional  <br/> |Die Panose Signatur für die Schriftart. Panose ist ein Klassifizierungssystem für Schriftarten, die anhand ihrer visuellen Merkmale kategorisiert.  <br/> |Werte des Typs xsd: String.  <br/> |
|UnicodeRanges  <br/> |XSD: String  <br/> |Optional  <br/> |Die unterstützten Unicode-Bereiche der Schriftart.  <br/> |Werte des Typs xsd: String.  <br/> |
   

