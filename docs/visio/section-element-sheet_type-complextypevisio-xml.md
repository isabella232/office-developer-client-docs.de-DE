---
title: Section-Element (Sheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Gibt eine Auflistung verwandter Eigenschaften an.
ms.openlocfilehash: c2d6fdcb39bd99f3ea6bb564794f068dd98e34cd
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59598157"
---
# <a name="section-element-sheet_type-complextype-visio-xml"></a>Section-Element (Sheet_Type complexType) (Visio XML)

Gibt eine Auflistung verwandter Eigenschaften an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften einer Zeichnung an.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften eines Zeichenblatts in einer Zeichnung an.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Eigenschaften an, die einem Shape zugeordnet sind.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Eigenschaften an, die einem Format, einer Zeichnung, einem Zeichenblatt oder einer Form zugeordnet sind.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Gibt ein Stylesheet an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Row](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von **Cell_Type** Elementen an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob eine Auflistung, die andernfalls geerbt werden würde, gelöscht wurde. Sie MUSS gleich 0 oder 1 sein. Der Wert 1 gibt an, dass die Auflistung nicht verwendet wird und IGNORIERT WERDEN MUSS. Der Wert 0 gibt an, dass die Auflistung von Eigenschaften für das Shape gültig ist. Wenn das **Del-Attribut** nicht vorhanden ist, ist der Wert 0.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt den nullbasierten Index des Elements an. Er MUSS unter allen **Section_Type** Elementen mit demselben **N-Attribut** des enthaltenden **Sheet_Type** eindeutig sein. Er MUSS größer als das **IX-Attribut** eines vorhergehenden **Section_Type** Elements mit demselben **N-Attribut** des enthaltenden **Sheet_Type** sein.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|N  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt den sprachunabhängigen Namen der Auflistung von Eigenschaften an. Es MUSS unter allen **Section_Type** Elementen des enthaltenden **Sheet_Type** Elements eindeutig sein, es sei denn, es ist gleich "Geometry". Sie MUSS einer Unterüberschrift in **Abschnitten** entsprechen.  <br/> |Werte des Typs "xsd:string".  <br/> |
   
### <a name="remarks"></a>HinwBemerkungeneise

Das **N-Attribut** dieses **Abschnittselements** muss einer der begrenzten Werte sein, die **ShapeSheet-Zellen** entsprechen. In der folgenden Tabelle finden Sie Informationen zu den Werten des **N-Attributs,** die für dieses **Section-Element** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Aktionen  <br/> |Eine Auflistung von Eigenschaften, die für die Formelauswertung verwendet werden. Es MUSS ein **ShapeSheet_Type** oder **PageSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Actions"](actions-section.md) <br/> |
|ActionTag  <br/> |Eine Auflistung von Eigenschaften, die nur für die Formelauswertung verwendet werden. Es MUSS ein **ShapeSheet_Type** oder **PageSheet_Type** übergeordnete Element aufweisen.  <br/> |[Im Abschnitt Aktion-Tag](action-tag-section.md) <br/> |
|Connections  <br/> |Eine Auflistung von Eigenschaften, die nur für die Formelauswertung verwendet werden. Es MUSS ein **ShapeSheet_Type** übergeordnete Element aufweisen.  <br/> ||
|Steuerelemente  <br/> |Eine Auflistung von Eigenschaften, die nur für die Formelauswertung verwendet werden. Es MUSS ein **ShapeSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Controls"](controls-section.md) <br/> |
|Hyperlink  <br/> |Eine Auflistung verwandter Eigenschaften, die die Shape-Hyperlinks angeben. Es MUSS ein **ShapeSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Hyperlinks"](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Eine Auflistung verwandter Eigenschaften, die die Shape-Daten angeben. Es MUSS ein **ShapeSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Shape Data"](shape-data-section.md) <br/> |
|Benutzer  <br/> |Eine Auflistung von Eigenschaften, die für die Formelauswertung verwendet werden. Es MUSS ein **DocumentSheet_Type-,** **PageSheet_Type-** oder **ShapeSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "User-defined Cells"](user-defined-cells-section.md) <br/> |
   
Das **IX-Attribut** dieses **Abschnittselements** muss einer der begrenzten Werte sein, die **ShapeSheet-Zellen** entsprechen. In der folgenden Tabelle finden Sie  Informationen zu den Werten des IX-Attributs, die für dieses **Section-Element** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Anmerkung  <br/> |Eine Auflistung von Eigenschaften, die Informationen zu Kommentaren enthalten, die in eine Dokumentseite eingefügt werden.  <br/> |[Abschnitt "Annotation"](annotation-section.md) <br/> |
|Zeichen  <br/> |Eine Auflistung verwandter Eigenschaften, die die Zeicheneigenschaften des Texts einer Form angeben. Es MUSS ein **ShapeSheet_Type** übergeordnetes Element oder ein **StyleSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Character"](character-section.md) <br/> |
|Connections  <br/> |Eine Auflistung von Eigenschaften, die nur für die Formelauswertung verwendet werden. Es MUSS ein **ShapeSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Connection Points"](connection-points-section.md) <br/> |
|Feld  <br/> |Eine Auflistung verwandter Eigenschaften, die die Textfelder eines Shapes angeben. Es MUSS ein **ShapeSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Text Fields"](text-fields-section.md) <br/> |
|FillGradient  <br/> |Eine Auflistung von Eigenschaften, die den Füllfarbverlauf einer Form angeben. Es MUSS ein **ShapeSheet_Type** oder **StyleSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Fill Gradient"](fill-gradient-section.md) <br/> |
|Geometrie  <br/> |Eine Auflistung verwandter Eigenschaften, die die Geometrievisualisierung angeben. Es MUSS ein **ShapeSheet_Type** übergeordnete Element aufweisen. Die erste **Row_Type** untergeordneten Element dieses Elements MUSS vom Typ "MoveTo", "RelMoveTo", "Ellipse" oder "InfiniteLine" sein.  <br/> |[Abschnitt "Geometrie"](geometry-section.md) <br/> |
|Ebenen  <br/> |Eine Auflistung von Eigenschaften, die alle Ebenen anzeigen, die auf einem Zeichenblatt definiert sind. Es MUSS das untergeordnete Element eines **PageSheet_Type-Elements** sein.  <br/> |[Abschnitt "Layers"](layers-section.md) <br/> |
|Linienverlauf  <br/> |Eine Auflistung verwandter Eigenschaften, die den Linienfarbverlauf einer Form angeben. Es MUSS ein **ShapeSheet_Type** oder **StyleSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Line Gradient"](line-gradient-section.md) <br/> |
|Absatz  <br/> |Eine Auflistung verwandter Eigenschaften, die die Absatzeigenschaften des Texts einer Form angeben. Es MUSS ein **ShapeSheet_Type** übergeordnetes Element oder ein **StyleSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Paragraph"](paragraph-section.md) <br/> |
|Reviewer  <br/> |Eine Auflistung von Eigenschaften, die für die Formelauswertung verwendet werden. Es MUSS ein **DocumentSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Reviewer"](reviewer-section.md) <br/> |
|Kratzen  <br/> |Eine Auflistung von Eigenschaften, die für die Formelauswertung verwendet werden. Es MUSS ein **DocumentSheet_Type-,** **PageSheet_Type-** oder **ShapeSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|Registerkarten  <br/> |Eine Auflistung verwandter Eigenschaften, die die Registerkarteneigenschaften des Texts einer Form angeben. Es MUSS ein **ShapeSheet_Type** übergeordnetes Element oder ein **StyleSheet_Type** übergeordnete Element aufweisen.  <br/> |[Abschnitt "Tabs"](tabs-section.md) <br/> |
   

