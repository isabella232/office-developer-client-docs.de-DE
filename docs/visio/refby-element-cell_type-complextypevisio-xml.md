---
title: RefBy-Element (Cell_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Gibt einen Verweis auf eine Seite in der Zeichnung an.
ms.openlocfilehash: 1731bd20a5ba4358c72370dfcdc6d8a6fc791e2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348454"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>RefBy-Element (Cell_Type complexType) (' Visio XML ')

Gibt einen Verweis auf eine Seite in der Zeichnung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |"Document. xml", "Masters. xml", "#. xml", "pages. xml", "page #. xml"  <br/> |
   
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
|[Cell-Element (Action Tag section)](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Definiert eine Eigenschaft für ein Aktionstag auf einem Shape oder einer Seite.  <br/> |
|[Zellenelement (Aktionenzeile)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext-oder aktionstagmenü zugeordnet ist.  <br/> |
|[Zellenelement (ArcTo-Zeile)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-Koordinate, y-Koordinate oder den Bogen eines kreisförmigen Bogens.  <br/> |
|[Cell-Element (Abschnitt "Character")](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Formatierungs Attribut für den Textlauf einer Form an, beispielsweise Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Basislinie oder Punktgröße.  <br/> |
|[Zellenelement (Verbindungszeile)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten, die horizontale oder vertikale Richtung oder den Typ für einen einzelnen Verbindungspunkt in einem Shape.  <br/> |
|[Zellenelement (Steuerelementzeile)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für ein Shape definiert ist.  <br/> |
|[Zellenelement (Ellipsenzeile)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des Mittelpunkts der Ellipse und zwei Punkte auf der Ellipse.  <br/> |
|[Zellenelement (EllipticalArcTo-Zeile)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten des Endpunkts eines elliptischen Bogens, x-oder y-Koordinaten der Steuerpunkte des Bogens, Winkel von der x-Achse zur Hauptachse der Ellipse oder Verhältnis zwischen Haupt-und Nebenachsen der Ellipse.  <br/> |
|[Cell-Element (Field section)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.  <br/> |
|[Cell-Element (Farbverlaufs Abschnitt)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füll Verlauf.  <br/> |
|[Cell-Element (Abschnitt "Geometry")](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Definiert Eigenschaften, mit denen die Formatierungs-und Verhaltenseigenschaften in Bezug auf die Linien und Bögen bestimmt werden, aus denen sich der Geometry-Abschnitt zusammensetzt.  <br/> |
|[Zellenelement (Linkzeile)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.  <br/> |
|[Zellenelement (InfiniteLine-Zeile)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten von zwei Punkten auf einer unendlichen Linien.  <br/> |
|[Cell-Element (Layer-Abschnitt)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft für eine Ebene oder deren Eigenschaften für eine Seite an.  <br/> |
|[Zellenelement (Abschnitt "Linienverlauf")](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz oder Position eines Farbverlaufsstopps für einen Linien Farbverlauf.  <br/> |
|[Zellenelement (LineTo-Zeile)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten des Endpunkts eines geraden Linienabschnitts.  <br/> |
|[Zellenelement (MoveTo-Zeile)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des ersten Scheitelpunkts einer Form oder stellt die x-oder y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar.  <br/> |
|[Zellenelement (NURBSTo-Zeile)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten, die Position des zweiten bis letzten Knotens, die Position der letzten Gewichtung, die Position des ersten Knotens, die Position der ersten Gewichtung oder die Formel für einen nicht einheitlichen rationalen B-Spline (NURBS).  <br/> |
|[Cell-Element (Abschnitt "Paragraph")](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Paragraph-Formatierungs Attribut für den Text des Shapes an, beispielsweise Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen.  <br/> |
|[Zellenelement (PolyLineTo-Zeile)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten des letzten Punkts einer Polylinie oder einer Polylinie.  <br/> |
|[Zellenelement (RelCubBezTo-Zeile)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinate des Endpunkts einer kubischen Bézier-Kurve relativ zur Breite und Höhe der Form, die x-oder y-Koordinaten des Steuerelements am Anfang der Breite und Höhe des Kurven relativen Shapes oder die x-oder y-Koordinate des Kontrollpunkts. des Endes der Breite und Höhe der Kurven relativen Form.  <br/> |
|[Zellenelement (RelEllipticalArcTo-Zeile)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinate des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, x-oder y-Koordinate der Steuerpunkte des Bogens im Verhältnis zur Breite und Höhe des Shapes, Winkel von der x-Achse zur Hauptachse der Ellipse oder Verhältnis zwischen dem Haupt-und Nebenachsen der Ellipse.  <br/> |
|[Cell-Element (RelLineTo-Zeile)](cell-element-rellineto-rowvisio-xml.md) [Zelle](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten des Endpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe eines Shapes.  <br/> |
|[Zellenelement (RelMoveTo-Zeile)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des ersten Scheitelpunkts einer Form oder die x-oder y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad, relativ zur Höhe und Breite der Form.  <br/> |
|[Cell-Element (RelQuadBezTo-Abschnitt](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinate des Endpunkts einer quadratischen Bézier-Kurve relativ zur Breite und Höhe des Shapes oder die x-oder y-Koordinaten des Steuerelements der Breite und Höhe der Kurven relativen Form.  <br/> |
|[Cell-Element (Abschnitt "Scratch")](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt einen Arbeitsbereich zum eingeben und Testen von Formeln an, auf die von anderen Zellen verwiesen werden kann.  <br/> |
|[Cell-Element (Shape Data Section](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft der Shape-Daten an.  <br/> |
|[Zellenelement (SplineKnot-Zeile)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten für einen Spline-Kontrollpunkt oder einen Spline-Knoten.  <br/> |
|[Cell-Element (Zeile SplineStart-Abschnitt](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x-oder y-Koordinaten für den zweiten Kontrollpunkt eines Splines, den zweiten Knoten, den ersten Knoten, den letzten Knoten oder den Grad des Splines.  <br/> |
|[Cell-Element (Registerkarten Abschnitt)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft an, die die Position oder Ausrichtung der Tabstopps für Shape und Style steuert.  <br/> |
|[Cell-Element (Abschnitt "User-Defined Cells")](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Eine Eigenschaft einer vom Benutzer angegebenen Information, auf die von anderen Zellen und Add-on-Tools verwiesen werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Gibt die ID einer Seite in der Zeichnung an.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|T  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den Verweistyp an.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

