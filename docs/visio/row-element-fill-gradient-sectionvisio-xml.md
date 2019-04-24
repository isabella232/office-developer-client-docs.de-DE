---
title: Row-Element (Abschnitt "Fill Gradient") (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f216afb5-4393-6e1c-54c2-3c184a26d934
description: Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füll Verlauf.
ms.openlocfilehash: 55ec3b58f57d1fb008825c1a5a4156e5aec59552
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358518"
---
# <a name="row-element-fill-gradient-section-visio-xml"></a>Row-Element (Abschnitt "Fill Gradient") (' Visio XML ')

Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füll Verlauf.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[FillGradientRow_Type](fillgradientrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML, Master #. XML, Page #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="FillGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füll Verlauf.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ENTF  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|IX  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt den 1-basierten Bezeichner für die Zeile an. Sie sollte unqiue und größer sein als andere Bezeichner im gleichen Abschnitt. Das Attribut IX wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Rezensent, Scratch und Tabs verwendet. Eine Zeile kann nur eines der Attribute IX oder N aufweisen.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|LocalName  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den eindeutigen sprachenabhängigen Namen der Zeile an.  <br/> |Werte des XSD: String-Typs.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet. Eine Zeile kann nur eines der Attribute IX oder N aufweisen.  <br/> |Werte des XSD: String-Typs.  <br/> |
|T  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den Typ des durch die Zeile dargestellten geometrischen Pfads an und wird in der Geometrie Visualisierung verwendet. Das T-Attribut wird nur für den Abschnitt Geometry verwendet.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

