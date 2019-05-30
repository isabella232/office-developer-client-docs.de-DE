---
title: Section-Element (Sheet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2e7e5dcc-f667-a08c-caa0-4b81e3126ef9
description: Gibt eine Auflistung verwandter Eigenschaften an.
ms.openlocfilehash: 2862d2ccf10d235996c2a6fb26691d498bdfdbcf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539033"
---
# <a name="section-element-sheettype-complextype-visio-xml"></a>Section-Element (Sheet_Type complexType) (Visio XML)

Gibt eine Auflistung verwandter Eigenschaften an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML, Masters. XML, Master #. XML, Pages. XML, Page #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Section" type="Section_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[DocumentSheet](documentsheet-element-visiodocument_type-complextypevisio-xml.md) <br/> |[DocumentSheet_Type](documentsheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften einer Zeichnung an.  <br/> |
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften eines Zeichenblatts in einer Zeichnung an.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[Master_Type complexType](master_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften des Zeichenblatts an, das dem Master zugeordnet ist.  <br/> |
|[Shape](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[ShapeSheet_Type](shapesheet_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Eigenschaften an, die einer Form zugeordnet sind.  <br/> |
|[Sheet](shape-element-shapes_type-complextypevisio-xml.md) <br/> |[Sheet_Type](sheet_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von Eigenschaften an, die einer Formatvorlage, Zeichnung, einem Zeichenblatt oder einer Form zugeordnet sind.  <br/> |
|[Stylesheet](stylesheet-element-stylesheets_type-complextypevisio-xml.md) <br/> |[StyleSheet_Type](stylesheet_type-complextypevisio-xml.md) <br/> |Gibt ein Stylesheet an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-elementvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine einzelne Eigenschaft an.  <br/> |
|[Zeile](https://msdn.microsoft.com/library/c978e3eb-b895-8fb7-e2ba-88c50e57b3db%28Office.15%29.aspx) <br/> |[Row_Type](row_type-complextypevisio-xml.md) <br/> |Gibt eine Auflistung von **Cell_Type** -Elementen an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eine Sammlung, die andernfalls vererbt werden würde, gelöscht wurde. Es muss gleich 0 oder 1 sein. Der Wert 1 gibt an, dass die Auflistung nicht verwendet wird und ignoriert werden muss. Der Wert 0 gibt an, dass die Auflistung von Eigenschaften für die Form gültig ist. Wenn das **del** -Attribut nicht vorhanden ist, ist der Wert 0.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|IX  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt den nullbasierten Index des Elements an. Es muss unter allen **Section_Type** -Elementen mit dem gleichen **N** -Attribut der enthaltenden **Sheet_Type**eindeutig sein. Er muss größer sein als das **IX** -Attribut eines beliebigen vorangehenden **Section_Type** -Elements mit demselben **N** -Attribut des enthaltenden **Sheet_Type**.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den sprachunabhängigen Namen der Auflistung von Eigenschaften an. Es muss bei allen **Section_Type** -Elementen des enthaltenden **Sheet_Type** -Elements eindeutig sein, es sei denn, es ist gleich "Geometry". Sie muss einer Unterüberschrift in Sections **** entsprechen.  <br/> |Werte des Typs XSD: String.  <br/> |
   
### <a name="remarks"></a>Hinweise

Das **N** -Attribut dieses **section** -Elements muss einer der begrenzten Werte sein, die **ShapeSheet** -Zellen entsprechen. In der folgenden Tabelle können Sie die Werte des **N** -Attributs bestimmen, die für dieses **section** -Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Aktionen  <br/> |Eine Auflistung von Eigenschaften, die für die Formelauswertung verwendet werden. Es muss über ein **ShapeSheet_Type** -oder **PageSheet_Type** -übergeordnetes Element verfügen.  <br/> |[Abschnitt "Actions"](actions-section.md) <br/> |
|ActionTag  <br/> |Eine Auflistung von Eigenschaften, die nur für die Formelauswertung verwendet werden. Es muss über ein **ShapeSheet_Type** -oder **PageSheet_Type** -übergeordnetes Element verfügen.  <br/> |[Im Abschnitt Aktion-Tag](action-tag-section.md) <br/> |
|Connections  <br/> |Eine Auflistung von Eigenschaften, die nur für die Formelauswertung verwendet werden. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element verfügen.  <br/> ||
|Steuerelemente  <br/> |Eine Auflistung von Eigenschaften, die nur für die Formelauswertung verwendet werden. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Controls"](controls-section.md) <br/> |
|Hyperlink  <br/> |Eine Auflistung verwandter Eigenschaften, die die Shape-Hyperlinks angeben. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Hyperlinks"](hyperlinks-section.md) <br/> |
|ShapeData  <br/> |Eine Auflistung verwandter Eigenschaften, mit denen die Shape-Daten angegeben werden. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Shape Data"](shape-data-section.md) <br/> |
|Benutzer  <br/> |Eine Auflistung von Eigenschaften, die für die Formelauswertung verwendet werden. Es muss über ein **DocumentSheet_Type**-, **PageSheet_Type**-oder **ShapeSheet_Type** -Element verfügen.  <br/> |[Abschnitt "User-defined Cells"](user-defined-cells-section.md) <br/> |
   
Das **IX** -Attribut dieses **section** -Elements muss einer der begrenzten Werte sein, die **ShapeSheet** -Zellen entsprechen. In der folgenden Tabelle können Sie die Werte des **IX** -Attributs bestimmen, die für dieses **section** -Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Anmerkung  <br/> |Eine Auflistung von Eigenschaften, die Informationen zu Kommentaren enthalten, die in eine Dokumentseite eingefügt werden.  <br/> |[Abschnitt "Annotation"](annotation-section.md) <br/> |
|Zeichen  <br/> |Eine Auflistung verwandter Eigenschaften, mit denen die Zeicheneigenschaften des Texts einer Form angegeben werden. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element oder ein übergeordnetes **StyleSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Character"](character-section.md) <br/> |
|Connections  <br/> |Eine Auflistung von Eigenschaften, die nur für die Formelauswertung verwendet werden. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Connection Points"](connection-points-section.md) <br/> |
|Feld  <br/> |Eine Auflistung verwandter Eigenschaften, die die Textfelder eines Shapes angeben. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Text Fields"](text-fields-section.md) <br/> |
|FillGradient  <br/> |Eine Auflistung von Eigenschaften, die den Füll Farbverlauf eines Shapes angeben. Es muss über ein **ShapeSheet_Type** -oder **StyleSheet_Type** -übergeordnetes Element verfügen.  <br/> |[Abschnitt "Füll Verlauf"](fill-gradient-section.md) <br/> |
|Geometrie  <br/> |Eine Auflistung verwandter Eigenschaften, die die Geometrie Visualisierung angeben. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element verfügen. Das erste untergeordnete **Row_Type** -Element dieses Elements muss vom Typ MoveTo, RelMoveTo, Ellipse oder endloslinie sein.  <br/> |[Abschnitt "Geometrie"](geometry-section.md) <br/> |
|Ebenen  <br/> |Eine Auflistung von Eigenschaften, die alle auf einem Zeichenblatt definierten Ebenen anzeigen. Es muss das untergeordnete Element eines **PageSheet_Type** -Elements sein.  <br/> |[Abschnitt "Layers"](layers-section.md) <br/> |
|Streckenverlauf  <br/> |Eine Auflistung verwandter Eigenschaften, die den Linien Farbverlauf eines Shapes angeben. Es muss über ein **ShapeSheet_Type** -oder **StyleSheet_Type** -übergeordnetes Element verfügen.  <br/> |[Abschnitt "Streckenverlauf"](line-gradient-section.md) <br/> |
|Absatz  <br/> |Eine Auflistung verwandter Eigenschaften, mit denen die Absatzeigenschaften des Texts einer Form angegeben werden. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element oder ein übergeordnetes **StyleSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Paragraph"](paragraph-section.md) <br/> |
|Reviewer  <br/> |Eine Auflistung von Eigenschaften, die für die Formelauswertung verwendet werden. Es muss über ein übergeordnetes **DocumentSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Reviewer"](reviewer-section.md) <br/> |
|Scratch  <br/> |Eine Auflistung von Eigenschaften, die für die Formelauswertung verwendet werden. Es muss über ein **DocumentSheet_Type**-, **PageSheet_Type**-oder **ShapeSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Scratch"](scratch-section.md) <br/> |
|Registerkarten  <br/> |Eine Auflistung verwandter Eigenschaften, die die registerkarteneigenschaften des Texts eines Shapes angeben. Es muss über ein übergeordnetes **ShapeSheet_Type** -Element oder ein übergeordnetes **StyleSheet_Type** -Element verfügen.  <br/> |[Abschnitt "Tabs"](tabs-section.md) <br/> |
   

