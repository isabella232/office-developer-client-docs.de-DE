---
title: Section-Element (Sheet_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Gibt eine Auflistung von verwandten Eigenschaften an.
ms.openlocfilehash: 7cb5e1c30960e69b252abc7af38e021607fd3502
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797988"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Section-Element (Sheet_Type ComplexType) ("Visio XML")

Gibt eine Auflistung von verwandten Eigenschaften an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.XML, masters.xml, Master-Shape # .xml, pages.xml, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Gibt Eigenschaften einer Zeichnung.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften einer Seite in einer Zeichnung.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts das Master-Shape zugeordnet.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Eigenschaften, die mit einer Form verknüpft ist.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Eigenschaften, die mit einer Formatvorlage, Zeichnung, Zeichnung Seite oder Shape verknüpft ist.  <br/> |
|[StyleSheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Gibt ein Stylesheet.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](http://msdn.microsoft.com/library/70a9d6d6-a4ff-2b0d-febc-789a04a2f5b0%28Office.15%29.aspx) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Row](http://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von **Cell_Type** -Elementen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ENTF  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eine Auflistung, die andernfalls geerbt werden würden gelöscht wurde. Es muss gleich 0 oder 1 sein. Der Wert 1 gibt an, dass die Auflistung nicht verwendet wird und ignoriert werden muss. Der Wert 0 gibt an, dass die Auflistung von Eigenschaften für die Form gültig ist. Wenn Sie das **ENTF** -Attribut nicht vorhanden ist, ist der Wert 0.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt den nullbasierten Index des Elements an. Es muss für alle Elemente mit dem gleichen **N** -Attribut des der enthaltenden **Sheet_Type** **Section_Type** eindeutig sein. Es muss größer als das **IX** -Attribut des keinem vorstehenden **Section_Type** -Element mit dem gleichen **N** -Attribut des der enthaltenden **Sheet_Type**sein.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|N  <br/> |XSD: String  <br/> |erforderlich  <br/> |Der sprachenunabhängige Name der Properties-Auflistung gibt. Es muss angemessen aller Elemente **Section_Type** des enthaltenden **Sheet_Type** -Elements eindeutig sein, es sei denn, "Geometrie" entspricht. Es muss eine Unterüberschrift in **Abschnitten**gleich sein.  <br/> |Werte des Typs xsd: String.  <br/> |
   
### <a name="remarks"></a>Bemerkungen

**N** -Attribut dieses Elements **im Abschnitt** muss einer der eine begrenzte Auswahl von Werten entsprechen, die **ShapeSheet-** Zellen entsprechen. Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für dieses Element **im Abschnitt** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Aktionen  <br/> |Eine Auflistung von Eigenschaften, die für formelauswertung verwendet werden. Sie benötigen ein **ShapeSheet_Type** oder **PageSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Actions"](actions-section.md) <br/> |
|ActionTag  <br/> |Eine Auflistung von Eigenschaften, die für nur formelauswertung verwendet werden. Sie benötigen ein **ShapeSheet_Type** oder **PageSheet_Type** übergeordnetes Element.  <br/> |[Im Abschnitt Aktion-Tag](action-tag-section.md) <br/> |
|Verbindungen  <br/> |Eine Auflistung von Eigenschaften, die für nur formelauswertung verwendet werden. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element.  <br/> ||
|Steuerelemente  <br/> |Eine Auflistung von Eigenschaften, die für nur formelauswertung verwendet werden. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Controls"](controls-section.md) <br/> |
|Hyperlink  <br/> |Eine Auflistung von verwandten Eigenschaften, die die Hyperlinks Shape angeben. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Hyperlinks"](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Eine Auflistung von Eigenschaften, die die Shape-Daten angeben. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Shape Data"](shape-data-section.md) <br/> |
|Benutzer  <br/> |Eine Auflistung von Eigenschaften, die für formelauswertung verwendet werden. Sie benötigen eine **DocumentSheet_Type**, **PageSheet_Type**oder **ShapeSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "User-defined Cells"](user-defined-cells-section.md) <br/> |
   
Das Attribut **IX** dieses Elements **im Abschnitt** muss eine der eine begrenzte Auswahl von Werten sein, die **ShapeSheet-** Zellen entsprechen. Finden Sie in der Tabelle unten, um die Werte des Attributs **IX** zu bestimmen, die für dieses Element **im Abschnitt** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Anmerkung  <br/> |Eine Auflistung von Eigenschaften mit Informationen zu Kommentaren, die in eine Dokumentseite eingefügt.  <br/> |[Abschnitt "Annotation"](annotation-section.md) <br/> |
|Zeichen  <br/> |Eine Auflistung von verwandten Eigenschaften, die zum Angeben von Eigenschaften für die Zeichen des Texts eines Shapes. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element oder ein **StyleSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Character"](character-section.md) <br/> |
|Verbindungen  <br/> |Eine Auflistung von Eigenschaften, die für nur formelauswertung verwendet werden. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Connection Points"](connection-points-section.md) <br/> |
|Feld  <br/> |Eine Auflistung von verwandten Eigenschaften, mit denen die Textfelder eines Shapes. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Text Fields"](text-fields-section.md) <br/> |
|FillGradient  <br/> |Eine Auflistung von Eigenschaften, mit denen der Farbverlauf für die Farbe eines Shapes. Sie benötigen ein **ShapeSheet_Type** oder **StyleSheet_Type** übergeordnetes Element.  <br/> |[Fill Gradient Section](fill-gradient-section.md) <br/> |
|Geometrie  <br/> |Eine Auflistung von verwandten Eigenschaften, die die Geometrie Visualisierung anzugeben. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element. Das erste **Row_Type** untergeordnete Element dieses Elements muss vom Typ MoveTo, RelMoveTo, eine Ellipse oder InfiniteLine sein.  <br/> |[Abschnitt "Geometrie"](geometry-section.md) <br/> |
|Layers  <br/> |Eine Auflistung von Eigenschaften, die auf einem Zeichenblatt definierte alle Ebenen anzuzeigen. Es muss ein **PageSheet_Type** -Element untergeordnet sein.  <br/> |[Abschnitt "Layers"](layers-section.md) <br/> |
|Zeile Farbverlauf  <br/> |Eine Auflistung von verwandten Eigenschaften, mit denen Farbverlauf Zeile eines Shapes. Sie benötigen ein **ShapeSheet_Type** oder **StyleSheet_Type** übergeordnetes Element.  <br/> |[Line Gradient Section](line-gradient-section.md) <br/> |
|Paragraph  <br/> |Eine Auflistung von verwandten Eigenschaften, mit denen die Absatzeigenschaften des Texts eines Shapes. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element oder ein **StyleSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Paragraph"](paragraph-section.md) <br/> |
|Prüfer  <br/> |Eine Auflistung von Eigenschaften, die für formelauswertung verwendet werden. Sie benötigen ein **DocumentSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Reviewer"](reviewer-section.md) <br/> |
|"Scratch"  <br/> |Eine Auflistung von Eigenschaften, die für formelauswertung verwendet werden. Sie benötigen eine **DocumentSheet_Type**, **PageSheet_Type**oder **ShapeSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|Registerkarten  <br/> |Eine Auflistung von verwandten Eigenschaften, mit denen die Registerkarten Eigenschaften des Texts eines Shapes. Sie benötigen ein **ShapeSheet_Type** übergeordnetes Element oder ein **StyleSheet_Type** übergeordnetes Element.  <br/> |[Abschnitt "Tabs"](tabs-section.md) <br/> |
   

