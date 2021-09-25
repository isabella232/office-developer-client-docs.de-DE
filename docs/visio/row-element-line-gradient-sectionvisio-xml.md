---
title: Zeilenelement (Abschnitt "Line Gradient") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 4d823766-5cb0-925c-f622-18025f44426c
description: Enthält die Farbe, Transparenz und Position eines Farbverlaufstopps für einen Linienverlauf.
ms.openlocfilehash: f07cfccd9444d1bad69b8bfbf6e01491dec6e1cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59559626"
---
# <a name="row-element-line-gradient-section-visio-xml"></a>Zeilenelement (Abschnitt "Line Gradient") (Visio XML)

Enthält die Farbe, Transparenz und Position eines Farbverlaufstopps für einen Linienverlauf.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[LineGradientRow_Type](linegradientrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="LineGradientRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufstopps für einen Linienverlauf.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt werden würde, gelöscht wurde.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt den 1-basierten Bezeichner für die Zeile an. Er sollte unaufwendbar und größer als andere Bezeichner im selben Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte "Character", "Connection", "Field", "FillGradient", "Geometry", "Layer", "LineGradient", "Paragraph", "Reviewer", "Scratch" und "Tabs" verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|LocalName  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachabhängigen Namen der Zeile an.  <br/> |Werte des Typs "xsd:string".  <br/> |
|N  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte "User", "Property", "Actions", "Control", "Connection", "Hyperlink" und "ActionTag" verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des Typs "xsd:string".  <br/> |
|T  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird. Das T-Attribut wird nur für den Abschnitt Geometry verwendet.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

