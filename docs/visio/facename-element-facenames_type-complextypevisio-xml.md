---
title: FaceName-Element (FaceNames_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b1783f05-ced1-917f-8298-eca4ecfa3912
description: Enthält Informationen zu einer Schriftart.
ms.openlocfilehash: 1d67c8c246236dd39cfc2a1fde39b0e9a0d24014
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582722"
---
# <a name="facename-element-facenames_type-complextype-visio-xml"></a>FaceName-Element (FaceNames_Type complexType) (Visio XML)

Enthält Informationen zu einer Schriftart.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[FaceName_Type](facename_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="FaceName" type="FaceName_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element > 
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[FaceNames](facenames-element-visiodocument_type-complextypevisio-xml.md) <br/> |[FaceNames_Type](facenames_type-complextypevisio-xml.md) <br/> |Enthält eine Auflistung von **FaceName-Elementen.**  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Zeichensätze  <br/> |xsd:string  <br/> |Optional  <br/> |Die unterstützten Zeichensätze der Schriftart.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Flags  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Kennzeichen, die Folgendes angeben: fehlende Schriftart, Standardschriftart, asiatische Schriftart, komplexe Schriftart, vertikale Schriftart und Schriftarttyp.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|NameU  <br/> |xsd:string  <br/> |Erforderlich  <br/> |Der Name der Schriftart als UTF-16 Unicode-Zeichenfolge.  <br/> ||
|Panos  <br/> |xsd:string  <br/> |Optional  <br/> |Die Panosesignatur für die Schriftart. Panose ist ein Klassifizierungssystem für Schriftarten, das sie basierend auf ihren visuellen Merkmalen kategorisiert.  <br/> |Werte des Typs "xsd:string".  <br/> |
|UnicodeRanges  <br/> |xsd:string  <br/> |Optional  <br/> |Die unterstützten Unicode-Bereiche der Schriftart.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

