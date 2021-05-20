---
title: Row-Element (Abschnitt "Fill Gradient") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füllgradienten.
ms.openlocfilehash: d9f3661d91b43bca7ff809c4e41a0c1257660e66
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538620"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a>Row-Element (Abschnitt "Fill Gradient") (Visio XML)

Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füllgradienten.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, Master#.xml, Seite#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füllgradienten.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.  <br/> |Werte des typs xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt den 1-basierten Bezeichner für die Zeile an. Er sollte unqiue und größer als andere Bezeichner im gleichen Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachabhängigen Namen der Zeile an.  <br/> |Werte des xsd:string-Typs.  <br/> |
|N  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des xsd:string-Typs.  <br/> |
|T  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird. Das T-Attribut wird nur für den Abschnitt Geometry verwendet.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

