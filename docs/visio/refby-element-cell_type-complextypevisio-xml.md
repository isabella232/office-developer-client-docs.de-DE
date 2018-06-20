---
title: RefBy-Element (Cell_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea2a63d3-d319-4420-1929-013dc832b308
description: Gibt einen Verweis auf eine Seite in der Zeichnung.
ms.openlocfilehash: 4d3f131ba5fc106c886d30d8561e095972b05a21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797777"
---
# <a name="refby-element-celltype-complextype-visio-xml"></a>RefBy-Element (Cell_Type ComplexType) ("Visio XML")

Gibt einen Verweis auf eine Seite in der Zeichnung.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.XML, masters.xml, Master-Shape # .xml, pages.xml, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="RefBy" type="RefBy_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zellenelement (Abschnitt "Action Tags")](cell-element-action-tag-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Eine Eigenschaft für ein Aktionstag definiert auf ein Shape oder Zeichenblatt.  <br/> |
|[Zellenelement (Zeile "Actions")](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft einer Aktion in einem Kontext- oder Aktionstagmenü eines benutzerdefinierten Befehls zugeordnet.  <br/> |
|[Zellenelement (Zeile ArcTo)](cell-element-arcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält das X-Koordinate, die y-Koordinate oder die Krümmung eines kreisförmigen Bogens.  <br/> |
|[Zellenelement "(Abschnitt" Character ")](cell-element-character-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Formatierung-Attribut für ein Shape-Text ausführen, wie z. B. Schriftart, Farbe, formatieren, case, relativ zur Grundlinie positionieren oder Schriftgrad.  <br/> |
|[Zellenelement (Verbindung Zeile)](cell-element-connection-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten, horizontaler oder vertikaler Richtung oder Typ für einen einzelnen Verbindungspunkt auf einem Shape.  <br/> |
|[Zellenelement (Zeile "Controls")](cell-element-controls-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für ein bestimmtes Steuerpunkt eines Shapes definiert.  <br/> |
|[Zellenelement (Zeile Ellipse)](cell-element-ellipse-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des Mittelpunkts der Ellipse von zwei Punkten auf der Ellipse.  <br/> |
|[Zellenelement (Zeile EllipticalArcTo)](cell-element-ellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten des Endpunkts eines elliptischen Bogens, x- oder y-Koordinaten des Steuerelements des Bogens, Winkel zwischen der x-Achse großen Achse der Ellipse oder das Verhältnis zwischen der Ellipse Haupt- und Hilfsintervalle Achsen verweist.  <br/> |
|[Zellenelement "(Abschnitt" Feld ")](cell-element-field-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln, die über das Dialogfeld Feld in den Text des Shapes eingefügt.  <br/> |
|[Zellenelement (füllen Farbverlauf Abschnitt)](cell-element-fill-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Farbe, Transparenz und Position des einen Farbverlaufstopp für einen Farbverlauf.  <br/> |
|[Zellenelement (Abschnitt "Geometry")](cell-element-geometry-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Definiert die Eigenschaften, die bestimmen, Formatierung und Verhalten von Eigenschaften in Bezug auf die Linien und Bögen, die im Abschnitt "Geometry" bilden.  <br/> |
|[Zellenelement (Zeile "Hyperlink")](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.  <br/> |
|[Zellenelement (Zeile InfiniteLine)](cell-element-infiniteline-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten von zwei Punkten einer unendlichen Linie.  <br/> |
|[Zellenelement "(Abschnitt" Layer ")](cell-element-layer-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft für eine Ebene oder seine Eigenschaften für eine Seite.  <br/> |
|[Zellenelement (Abschnitt "Line Farbverlauf")](cell-element-line-gradient-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Die Farbe, Transparenz oder Position der einen Farbverlaufstopp für einen Farbverlauf Zeile enthält.  <br/> |
|[Zellenelement (Zeile "LineTo")](cell-element-lineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts.  <br/> |
|[Zellenelement (Zeilen MoveTo-Zeile)](cell-element-moveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die x- oder y-Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke dar.  <br/> |
|[Zellenelement (Zeile NURBSTo)](cell-element-nurbsto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten, Position des zweiten bis letzte Knoten, der Position der letzten Linienbreite, die Position des ersten Knotens, Position der ersten Stärke oder die Formel für einen nicht-gleichförmigen, rationalen B-Spline (NURBS).  <br/> |
|[Zellenelement (Abschnitt "Paragraph")](cell-element-paragraph-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt ein Absatzformat-Attribut für den Text des Shapes, wie etwa Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen an.  <br/> |
|[Zellenelement (Zeile "PolylineTo")](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des letzten Punkts einer Polylinie oder eine Polylinienformel.  <br/> |
|[Zellenelement (RelCubBezTo Zeile)](cell-element-relcubbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des Endpunkts des eine kubische Bézierkurve relativ zur Höhe und Breite des Shapes, die x- oder y-Koordinaten des Kontrollpunkts des Anfang der Höhe und Breite für die Kurve relative Form oder die x- oder y-Koordinaten des Kontrollpunkts der beenden, Breite und Höhe des relativen Kurve-Shapes.  <br/> |
|[Zellenelement (RelEllipticalArcTo Zeile)](cell-element-relellipticalarcto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten des Endpunkts der eines elliptischen Bogens relativ zur Höhe und Breite des Shapes x- oder y-Koordinaten des Steuerelements Kontrollpunkte des Bogens relativ zur Breite und Höhe, Winkel zwischen der x-Achse großen Achse der Ellipse oder das Verhältnis zwischen des Shapes die Haupt- und Hilfsintervalle Achse der Ellipse  <br/> |
|[Zellenelement (RelLineTo Zeile)](cell-element-rellineto-rowvisio-xml.md) [Zelle](cell-element-rellineto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält X- oder y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe des Shapes.  <br/> |
|[Zellenelement (RelMoveTo Zeile)](cell-element-relmoveto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des ersten Scheitelpunkts eines Shapes oder die x- oder y-Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad, relativ zur Höhe und Breite der Form.  <br/> |
|[Zellenelement (RelQuadBezTo-Abschnitt](cell-element-relquadbezto-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des Endpunkts des eine quadratische Bézier-Kurve relativ zur Höhe und Breite des Shapes oder die x- oder y-Koordinaten des Kontrollpunkts Breite und Höhe des relativen Kurve-Shapes.  <br/> |
|[Zellenelement (Abschnitt "Scratch")](cell-element-scratch-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine arbeitsumgebung für die Eingabe und Testen von Formeln, die auf die von anderen Zellen verwiesen werden können.  <br/> |
|[Zellenelement (Abschnitt "Shape Data"](cell-element-shape-data-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft eines Shape-Daten an.  <br/> |
|[Zellenelement (Zeile "SplineKnot")](cell-element-splineknot-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten für Kontrollpunkts eines Splines oder den Knoten eines Splines.  <br/> |
|[Zellenelement (SplineStart-Abschnitt](cell-element-splinestart-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten für den zweiten Kontrollpunkts eines Splines, dessen zweiten Knoten, dessen ersten Knoten, der letzte Knoten oder der Grad eines Splines.  <br/> |
|[Zellenelement "(Abschnitt" Tabs ")](cell-element-tabs-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft, die Form und-Art Tabstoppposition oder Ausrichtung von Steuerelementen an.  <br/> |
|[Zellenelement (User-defined Cells Abschnitt)](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Eine Eigenschaft eines vom Benutzer angegebener bestimmte Informationen, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Gibt die ID einer Seite in der Zeichnung.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|T  <br/> |XSD: String  <br/> |erforderlich  <br/> |Gibt den Verweistyp an.  <br/> |Werte des Typs xsd: String.  <br/> |
   

