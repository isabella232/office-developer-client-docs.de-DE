---
title: Zeilenelement (Abschnitt "Action Tag") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 54c3315f-770f-6995-d0d8-ab66e4fe10d9
description: Definiert ein Aktionstag auf einem Shape oder Zeichenblatt.
ms.openlocfilehash: a1e2a4b79c6ea73ba64ba13977753d464aab3775
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59623054"
---
# <a name="row-element-action-tag-section-visio-xml"></a>Zeilenelement (Abschnitt "Action Tag") (Visio XML)

Definiert ein Aktionstag auf einem Shape oder Zeichenblatt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ActionTagRow_Type](actiontagrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="ActionTagRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Definiert ein Aktionstag auf einem Shape oder Zeichenblatt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Definiert eine Eigenschaft für ein Aktionstag in einem Shape oder Zeichenblatt.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt werden würde, gelöscht wurde.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt den 1-basierten Bezeichner für die Zeile an. Er sollte unaufwendbar und größer als andere Bezeichner im selben Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte "Character", "Connection", "Field", "FillGradient", "Geometry", "Layer", "LineGradient", "Paragraph", "Reviewer", "Scratch" und "Tabs" verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|LocalName  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachabhängigen Namen der Zeile an.  <br/> |Werte des Typs "xsd:string".  <br/> |
|N  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte "User", "Property", "Actions", "Control", "Connection", "Hyperlink" und "ActionTag" verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des Typs "xsd:string".  <br/> |
|T  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird. Das T-Attribut wird nur für den Abschnitt Geometry verwendet.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

