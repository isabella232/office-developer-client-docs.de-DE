---
title: Zeilenelement (Abschnitt "Shape Data") (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9eb74ae8-ff42-6e34-30e2-2080bf8b5754
description: Gibt einen Shape-Dateneintrag zum Zuordnen von Daten zu einer Form an.
ms.openlocfilehash: 7857ad8a28e11d6ed3ba34145ffc0606f306120f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283486"
---
# <a name="row-element-shape-data-section-visio-xml"></a>Zeilenelement (Abschnitt "Shape Data") (' Visio XML ')

Gibt einen Shape-Dateneintrag zum Zuordnen von Daten zu einer Form an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Shape-data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Master #. XML, Page #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="PropertyRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Gibt einen Shape-Dateneintrag zum Zuordnen von Daten zu einer Form an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft der Shape-Daten an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ENTF  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|IX  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt den 1-basierten Bezeichner für die Zeile an. Sie sollte unqiue und größer sein als andere Bezeichner im gleichen Abschnitt. Das Attribut IX wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Rezensent, Scratch und Tabs verwendet. Eine Zeile kann nur eines der Attribute IX oder N aufweisen.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|LocalName  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den eindeutigen sprachenabhängigen Namen der Zeile an.  <br/> |Werte des XSD: String-Typs.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet. Eine Zeile kann nur eines der Attribute IX oder N aufweisen.  <br/> |Werte des XSD: String-Typs.  <br/> |
|T  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den Typ des durch die Zeile dargestellten geometrischen Pfads an und wird in der Geometrie Visualisierung verwendet. Das T-Attribut wird nur für den Abschnitt Geometry verwendet.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

