---
title: RefBy-Element (Cell_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Gibt einen Verweis auf eine Seite in der Zeichnung an.
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538312"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>RefBy-Element (Cell_Type complexType) (Visio XML)

Gibt einen Verweis auf eine Seite in der Zeichnung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML, Masters. XML, Master #. XML, Pages. XML, Page #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell-Element (Aktions-Tag-Abschnitt)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Definiert eine Eigenschaft für ein Action-Tag auf einem Shape oder einer Seite.  <br/> |
|[Zellenelement (Aktionenzeile)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext-oder Aktionstags Menü zugeordnet ist.  <br/> |
|[Zellenelement (ArcTo-Zeile)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-Koordinate, die y-Koordinate oder die Verbeugung eines kreisförmigen Bogens.  <br/> |
|[Cell-Element (Abschnitt "Character")](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Formatierungs Attribut für die Textausführung eines Shapes an, beispielsweise Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Grundlinie oder Punktgröße.  <br/> |
|[Zellenelement (Verbindungszeile)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten, die horizontale oder vertikale Richtung oder den Typ für einen einzelnen Verbindungspfad auf einem Shape.  <br/> |
|[Zellenelement (Steuerelementzeile)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für eine Form definiert ist.  <br/> |
|[Zellenelement (Ellipsenzeile)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des Mittelpunkts der Ellipse und zwei Punkte auf der Ellipse.  <br/> |
|[Zellenelement (EllipticalArcTo-Zeile)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten des Endpunkts eines elliptischen Bogens, der x-oder y-Koordinaten der Kontrollpunkte des Bogens, des Winkels von der x-Achse zur Hauptachse der Ellipse oder des Verhältnisses zwischen den Haupt-und Nebenachsen der Ellipse.  <br/> |
|[Cell-Element (Feldabschnitt)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.  <br/> |
|[Cell-Element (Abschnitt "Füll Verlauf")](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füll Verlauf.  <br/> |
|[Zellenelement (Abschnitt "Geometry")](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Definiert Eigenschaften, die Formatierungs-und Verhaltenseigenschaften in Bezug auf die Linien und Bögen bestimmen, aus denen sich der Abschnitt Geometry zusammensetzt.  <br/> |
|[Zellenelement (Linkzeile)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.  <br/> |
|[Zellenelement (InfiniteLine-Zeile)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten von zwei Punkten auf einer unendlichen Reihe.  <br/> |
|[Cell-Element (Layer section)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft für einen Layer oder seine Eigenschaften für eine Seite an.  <br/> |
|[Cell-Element (Abschnitt "Streckenverlauf")](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, die Transparenz oder die Position eines Farbverlaufsstopps für einen linearen Farbverlauf.  <br/> |
|[Zellenelement (LineTo-Zeile)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des endscheitels eines geraden Linie-Segments.  <br/> |
|[Zellenelement (MoveTo-Zeile)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des ersten Scheitelpunkts einer Form oder stellt die x-oder y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar.  <br/> |
|[Zellenelement (NURBSTo-Zeile)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten, die Position des zweiten bis letzten Knotens, die Position der letzten Gewichtung, die Position des ersten Knotens, die Position der ersten Gewichtung oder die Formel für einen nicht einheitlichen rationalen B-Spline (NURBS).  <br/> |
|[Cell-Element (Abschnitt "Paragraph")](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Attribut für die Absatzformatierung für den Text des Shapes an, beispielsweise Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen.  <br/> |
|[Zellenelement (PolyLineTo-Zeile)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten des letzten Kommas einer Polylinie oder einer Polylinien Formel.  <br/> |
|[Zellenelement (RelCubBezTo-Zeile)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des Endpunkts einer kubischen Bézier-Kurve relativ zur Breite und Höhe der Form, die x-oder y-Koordinaten des Kontrollpunkts am Anfang der relativen Form der Kurve, die die Breite und Höhe des Shapes oder die x-oder y-Koordinaten des Kontrollpunkts enthält. des Endes der Breite und Höhe des Kurven relativen Shapes.  <br/> |
|[Zellenelement (RelEllipticalArcTo-Zeile)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, die x-oder y-Koordinate der Kontrollpunkte des Bogens relativ zur Breite und Höhe des Shapes, von der x-Achse zur Hauptachse der Ellipse oder zum Verhältnis zwischen dem Haupt-und Nebenachsen der Ellipse.  <br/> |
|[Cell-Element (RelLineTo-Zeile)](cell-element-rellineto-rowvisio-xml.md) [Zelle](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des endscheitels eines geraden Liniensegments relativ zur Breite und Höhe eines Shapes.  <br/> |
|[Zellenelement (RelMoveTo-Zeile)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des ersten Scheitelpunkts einer Form oder die x-oder y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung eines Pfads relativ zur Höhe und Breite der Form.  <br/> |
|[Cell-Element (RelQuadBezTo-Abschnitt](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des Endpunkts einer quadratischen Bézier-Kurve relativ zur Breite und Höhe der Form oder die x-oder y-Koordinaten des Kontrollpunkts der relativen Form der Kurve, die die Breite und Höhe aufweist.  <br/> |
|[Cell-Element (Scratch section)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt einen Arbeitsbereich zum eingeben und Testen von Formeln an, auf die von anderen Zellen verwiesen werden kann.  <br/> |
|[Cell-Element (Shape-Datenabschnitt](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft der Shape-Daten an.  <br/> |
|[Zellenelement (SplineKnot-Zeile)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten für den Kontrollpunkte eines Splines oder den Knoten eines Splines.  <br/> |
|[Cell-Element (Zeile SplineStart-Abschnitt](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten für den zweiten Kontrollpunkte eines Splines, den zweiten Knoten, den ersten Knoten, den letzten Knoten oder den Grad des Splines.  <br/> |
|[Cell-Element (Tabs-Abschnitt)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft an, die die Position oder Ausrichtung von Shape-und Style-Tabstopps steuert.  <br/> |
|[Cell-Element (Abschnitt "User-Defined Cells")](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Eine Eigenschaft einer vom Benutzer angegebenen Information, auf die von anderen Zellen und Add-on-Tools verwiesen werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt die ID einer Seite in der Zeichnung an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|T  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den Verweistyp an.  <br/> |Werte des Typs XSD: String.  <br/> |
   

