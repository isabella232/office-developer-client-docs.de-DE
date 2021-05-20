---
title: RefBy-Element (Cell_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.
ms.openlocfilehash: cb47919a97b8ad42f62bcb1337cd8e6b3596f5ff
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538312"
---
# <a name="refby-element-cell_type-complextype-visio-xml"></a>RefBy-Element (Cell_Type complexType) (Visio XML)

Gibt einen Verweis auf ein Zeichenblatt in der Zeichnung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, masters.xml, Master#.xml, pages.xml, Seite#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell-Element (Abschnitt "Action Tag")](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Definiert eine Eigenschaft für ein Aktionstag auf einer Form oder Seite.  <br/> |
|[Zellenelement (Aktionenzeile)](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext- oder Aktionstagmenü zugeordnet ist.  <br/> |
|[Zellenelement (ArcTo-Zeile)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X-Koordinate, Y-Koordinate oder den Bogen eines Kreisbogens.  <br/> |
|[Cell-Element (Abschnitt "Character")](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Formatierungsattribut für die Textlauf eines Shapes an, z. B. Schriftart, Farbe, Formatvorlage, Groß-/Klein- oder Position relativ zur Grundlinie oder Punktgröße.  <br/> |
|[Zellenelement (Verbindungszeile)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten, horizontale oder vertikale Richtung oder typ für einen einzelnen Verbindungspunkt einer Form.  <br/> |
|[Zellenelement (Steuerelementzeile)](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für ein bestimmtes Steuerelementhandle, das für eine Form definiert ist.  <br/> |
|[Zellenelement (Ellipsenzeile)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten des Mittelpunkts der Ellipse und zwei Punkte auf der Ellipse.  <br/> |
|[Zellenelement (EllipticalArcTo-Zeile)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten des Endpunkts eines elliptischen Bogens, X- oder Y-Koordinaten der Kontrollpunkte im Bogen, Winkel von der X-Achse zur Hauptachse der Ellipse oder Verhältnis zwischen Haupt- und Nebenachse der Ellipse.  <br/> |
|[Cell-Element (Field Section)](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.  <br/> |
|[Cell-Element (Abschnitt "Fill Gradient")](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position eines Farbverlaufsstopps für einen Füllgradienten.  <br/> |
|[Cell-Element (Abschnitt "Geometry")](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Definiert Eigenschaften, die Formatierungs- und Verhaltenseigenschaften im Hinblick auf die Linien und Bögen bestimmen, aus der der Abschnitt "Geometry" ist.  <br/> |
|[Zellenelement (Linkzeile)](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.  <br/> |
|[Zellenelement (InfiniteLine-Zeile)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten von zwei Punkten in einer unendlichen Linie.  <br/> |
|[Cell-Element (Layer Section)](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft für einen Layer oder seine Eigenschaften für eine Seite an.  <br/> |
|[Cell-Element (Abschnitt "Line Gradient")](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz oder Position eines Farbverlaufsstopps für einen Linienverlauf.  <br/> |
|[Zellenelement (LineTo-Zeile)](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten des endenden Scheitelpunkts eines geraden Abschnitts.  <br/> |
|[Zellenelement (MoveTo-Zeile)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten des ersten Scheitelpunkts einer Form oder stellt die X- oder Y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar.  <br/> |
|[Zellenelement (NURBSTo-Zeile)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten, die Position des vorletzten Knotens, die Position der letzten Gewichtung, die Position des ersten Knotens, die Position der ersten Gewichtung oder die Formel für einen nichtuniformierten rationalen B-Spline (NURBS).  <br/> |
|[Cell-Element (Abschnitt "Paragraph")](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Absatzformatierungsattribut für den Text des Shapes an, z. B. Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen.  <br/> |
|[Zellenelement (PolyLineTo-Zeile)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten des letzten Punkts einer Polylinie oder einer Polylinienformel.  <br/> |
|[Zellenelement (RelCubBezTo-Zeile)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des Endpunkts einer kubischen Bézierkurve relativ zur Breite und Höhe der Form, die X- oder Y-Koordinaten des Kontrollpunkts am Anfang der Breite und Höhe der Kurve relativer Form oder die X- oder Y-Koordinaten des Kontrollpunkts des Endes der Breite und Höhe der Kurve relativer Form.  <br/> |
|[Zellenelement (RelEllipticalArcTo-Zeile)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe des Shapes, x- oder y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel von der X-Achse zur Hauptachse der Ellipse oder Verhältnis zwischen den Haupt- und Nebenachsen der Ellipse.  <br/> |
|[Zelle des Cell-Elements (RelLineTo Row)](cell-element-rellineto-rowvisio-xml.md)[](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite und Höhe eines Shapes.  <br/> |
|[Zellenelement (RelMoveTo-Zeile)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des ersten Scheitelpunkts einer Form oder die X- oder Y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite der Form.  <br/> |
|[Cell-Element (Abschnitt "RelQuadBezTo"](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe der Form oder zu den x- oder y-Koordinaten des Kontrollpunkts der Breite und Höhe der Kurve relativer Form.  <br/> |
|[Cell-Element (Scratch Section)](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt einen Arbeitsbereich zum Eingeben und Testen von Formeln an, auf die von anderen Zellen verwiesen werden kann.  <br/> |
|[Cell-Element (Abschnitt "Shape Data"](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft der Shapedaten an.  <br/> |
|[Zellenelement (SplineKnot-Zeile)](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten für den Kontrollpunkt eines Splines oder einen Splineknoten.  <br/> |
|[Cell-Element (Abschnitt SplineStart](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten für den zweiten Kontrollpunkt eines Splines, den zweiten Knoten, den ersten Knoten, den letzten Knoten oder den Grad des Splines.  <br/> |
|[Cell-Element (Tabs Section)](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft an, die die Position oder Ausrichtung der Registerkartenstopps für Form und Format steuert.  <br/> |
|[Cell-Element (Abschnitt "User-defined Cells")](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Eine Eigenschaft eines benutzerdefinierten Informationsteils, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Gibt die ID eines Zeichenblatts in der Zeichnung an.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|T  <br/> |xsd:string  <br/> |erforderlich  <br/> |Gibt den Referenztyp an.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

