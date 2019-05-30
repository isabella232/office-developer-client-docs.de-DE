---
title: FaceName-Element (FaceNames_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Enthält Informationen zu einer Schriftart.
ms.openlocfilehash: 773b5f10607cc6d515671d93d7d4abd9e39e72ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541015"
---
# <a name="facename-element-facenamestype-complextype-visio-xml"></a>FaceName-Element (FaceNames_Type complexType) (Visio XML)

Enthält Informationen zu einer Schriftart.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **FaceName** -Elementen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|CharSets  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die unterstützten Zeichensätze der Schriftart.  <br/> |Werte des Typs XSD: String.  <br/> |
|Flags  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Flags, die Folgendes angeben: fehlende Schriftart, Standardschriftart, asiatische Schriftart, komplexe Schriftart, vertikale Schriftart und Schriftarttyp.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|NameU  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Der Name der Schriftart als UTF-16-Unicode-Zeichenfolge.  <br/> ||
|PANOS  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Panose-Signatur für die Schriftart. Panose ist ein Klassifikationssystem für Schriften, die Sie basierend auf Ihren visuellen Eigenschaften kategorisieren.  <br/> |Werte des Typs XSD: String.  <br/> |
|Unicode Ranges  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die unterstützten Unicode-Bereiche der Schriftart.  <br/> |Werte des Typs XSD: String.  <br/> |
   

