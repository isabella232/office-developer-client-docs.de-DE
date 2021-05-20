---
title: ColorEntry-Element (Colors_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3f325ad8-bbc7-28bf-9e48-1fde4fbdbdc0
description: Enthält einen Farbtabelle-Eintrag.
ms.openlocfilehash: f2221d8d32823e5eec4a100eaf4e8f62b914df28
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540182"
---
# <a name="colorentry-element-colors_type-complextype-visio-xml"></a>ColorEntry-Element (Colors_Type complexType) (Visio XML)

Enthält einen Farbtabelle-Eintrag.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ColorEntry_Type](colorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="ColorEntry" type="ColorEntry_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Colors](colors-element-visiodocument_type-complextypevisio-xml.md) <br/> |[Colors_Type](colors_type-complextypevisio-xml.md) <br/> |Enthält die Farbtabelle des Dokuments.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|IX  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Der nullbasierte Index des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|RGB  <br/> |xsd:string  <br/> |erforderlich  <br/> |Der Hexadezimalwert des Farbtabelleeintrags.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

