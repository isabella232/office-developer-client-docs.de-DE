---
title: RefBy-Element (Cell_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.
ms.openlocfilehash: 5629718ca152e08b914a8f71880dbadf321591cf
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59565912"
---
# <a name="refby-element-cell_type-complextype-visio-xml"></a>RefBy-Element (Cell_Type complexType) (Visio XML)

Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zellenelement (Abschnitt "Action Tag")](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Definiert eine Eigenschaft für ein Aktionstag in einem Shape oder Zeichenblatt.  <br/> |
|[Zellenelement (Aktionenzeile)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext- oder Aktionstagmenü zugeordnet ist.  <br/> |
|[Zellenelement (ArcTo-Zeile)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X-Koordinate, die Y-Koordinate oder den Bogen eines kreisförmigen Bogens.  <br/> |
|[Zellenelement (Abschnitt "Character")](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Formatierungsattribut für den Textlauf eines Shapes an, z. B. Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Grundlinie oder Punktgröße.  <br/> |
|[Zellenelement (Verbindungszeile)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten, die horizontale oder vertikale Richtung oder den Typ für einen einzelnen Verbindungspunkt in einem Shape.  <br/> |
|[Zellenelement (Steuerelementzeile)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für ein Shape definiert ist.  <br/> |
|[Zellenelement (Ellipsenzeile)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten des Mittelpunkts der Ellipse und zwei Punkte auf der Ellipse.  <br/> |
|[Zellenelement (EllipticalArcTo-Zeile)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten des Endpunkts eines elliptischen Bogens, x- oder y-Koordinaten der Kontrollpunkte im Bogen, Winkel von der X-Achse zur Hauptachse der Ellipse oder Verhältnis zwischen der Haupt- und Nebenachse der Ellipse.  <br/> |
|[Zellenelement (Abschnitt "Field")](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.  <br/> |
|[Zellenelement (Abschnitt "Fill Gradient")](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufstopps für einen Füllverlauf.  <br/> |
|[Zellenelement (Abschnitt "Geometry")](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Definiert Eigenschaften, die formatierungs- und verhaltensbezogene Eigenschaften in Bezug auf die Linien und Bögen bestimmen, aus denen der Abschnitt "Geometry" bestehen.  <br/> |
|[Zellenelement (Linkzeile)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.  <br/> |
|[Zellenelement (InfiniteLine-Zeile)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten von zwei Punkten auf einer unendlichen Linie.  <br/> |
|[Zellenelement (Abschnitt "Layer")](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft für einen Layer oder deren Eigenschaften für eine Seite an.  <br/> |
|[Zellenelement (Abschnitt "Line Gradient")](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz oder Position eines Farbverlaufstopps für einen Linienverlauf.  <br/> |
|[Zellenelement (LineTo-Zeile)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten des Endscheitelpunkts eines geraden Liniensegments.  <br/> |
|[Zellenelement (MoveTo-Zeile)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die x- oder y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad dar.  <br/> |
|[Zellenelement (NURBSTo-Zeile)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten, die Position des zweiten bis letzten Knotens, die Position der letzten Gewichtung, die Position des ersten Knotens, die Position der ersten Gewichtung oder die Formel für einen nicht fähigen rationalen B-Spline (NURBS).  <br/> |
|[Zellenelement (Abschnitt "Paragraph")](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Absatzformatierungsattribut für den Text des Shapes an, z. B. Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen.  <br/> |
|[Zellenelement (PolyLineTo-Zeile)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten des letzten Punkts einer Polylinie oder einer Polylinienformel.  <br/> |
|[Zellenelement (RelCubBezTo-Zeile)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des Endpunkts einer kubischen Bézierkurve relativ zur Breite und Höhe des Shapes, die x- oder y-Koordinaten des Kontrollpunkts des Anfangspunkts der relativen Breite und Höhe der Kurve oder die x- oder y-Koordinaten des Kontrollpunkts des Endes der relativen Breite und Höhe der Kurve.  <br/> |
|[Zellenelement (RelEllipticalArcTo-Zeile)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe des Shapes, x- oder y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, zum Winkel von der X-Achse zur Hauptachse der Ellipse oder zum Verhältnis zwischen der Haupt- und Hilfsachse der Ellipse.  <br/> |
|[Zelle "Cell"-Element (Zeile "RelLineTo")](cell-element-rellineto-rowvisio-xml.md)[](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten des Endscheitelpunkts eines geraden Liniensegments relativ zur Breite und Höhe eines Shapes.  <br/> |
|[Zellenelement (RelMoveTo-Zeile)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten des ersten Scheitelpunkts eines Shapes oder die x- oder y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite des Shapes.  <br/> |
|[Zellenelement (Abschnitt "RelQuadBezTo"](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe des Shapes oder zu den X- oder Y-Koordinaten des Kontrollpunkts der relativen Breite und Höhe der Kurve.  <br/> |
|[Zellenelement (Abschnitt "Scratch")](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt einen Arbeitsbereich zum Eingeben und Testen von Formeln an, auf die von anderen Zellen verwiesen werden kann.  <br/> |
|[Zellenelement (Abschnitt "Shape Data"](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft der Shape-Daten an.  <br/> |
|[Zellenelement (SplineKnot-Zeile)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten für den Kontrollpunkt eines Splines oder den Knoten eines Splines.  <br/> |
|[Zellenelement (Abschnitt "SplineStart"](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten für den zweiten Kontrollpunkt eines Splines, dessen zweiten Knoten, seinen ersten Knoten, den letzten Knoten oder den Grad des Splines.  <br/> |
|[Zellenelement (Abschnitt "Tabs")](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft an, die die Position oder Ausrichtung von Tabstopps für Formen und Stile steuert.  <br/> |
|[Zellenelement (Abschnitt "User-defined Cells")](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |Eine Eigenschaft einer vom Benutzer angegebenen Information, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Gibt die ID eines Zeichenblatts in der Zeichnung an.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|T  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt den Verweistyp an.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

