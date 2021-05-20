---
title: Row-Element (Geometry Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2b273958-1997-7c63-4a61-d231f023a81f
description: Enthält Zeilen, die die Koordinaten der Scheitelpunkte für die Linien und Bögen auflisten, aus denen das Shape besteht.
ms.openlocfilehash: 6dbf18b749ed072645c4941922729010f74fc0ae
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540854"
---
# <a name="row-element-geometry-section-visio-xml"></a>Row-Element (Geometry Section) (Visio XML)

Enthält Zeilen, die die Koordinaten der Scheitelpunkte für die Linien und Bögen auflisten, aus denen das Shape besteht.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[GeometryRow_Type](geometry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="GeometryRow_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Enthält Zeilen, die die Koordinaten der Scheitelpunkte für die Linien und Bögen auflisten, aus denen das Shape besteht.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

> [!NOTE]
> Das Cell-Element ist das einzige untergeordnete Element dieses Elements. Je nach dem "T"-Attribut dieses Elements unterscheidet sich die Bedeutung der Cell-Elemente. In der folgenden Tabelle entspricht der parathetische Text im Elementnamen dem "T"-Wert, auf den das Thema angewendet wird. 
  
|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zellenelement (ArcTo-Zeile)](arcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten und die Krümmung eines kreisförmigen Bogens.  <br/> |
|[Zellenelement (Ellipsenzeile)](ellipse-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten des Mittelpunkts der Ellipse von zwei Punkten auf der Ellipse.  <br/> |
|[Zellenelement (EllipticalArcTo-Zeile)](ellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten des elliptischen Endpunkts eines Bogens, die x- und y-Koordinaten der Kontrollpunkte des Bogens, den Winkel von der x-Achse zur größeren Achse der Ellipse und das Verhältnis zwischen der großen und der kleinen Achse der Ellipse.  <br/> |
|[Zellenelement (InfiniteLine-Zeile)](infiniteline-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten von zwei Punkten einer unendlichen Linie.  <br/> |
|[Zellenelement (LineTo-Zeile)](lineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x-> und y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts.  <br/> |
|[Zellenelement (MoveTo-Zeile)](moveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die x- und y-Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke dar.  <br/> |
|[Zellenelement (NURBSTo-Zeile)](nurbsto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten, die Positionen des zweiten bis letzten Knotens, die Position der letzen Stärke, die Position des ersten Knotens, die Position der ersten Stärke und die Formel für einen nicht-gleichförmigen rationalen B-Spline (NURBS).  <br/> |
|[Zellenelement (PolyLineTo-Zeile)](polylineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten des letzten Punkts einer Polylinie und eine Polylinienformel.  <br/> |
|[Zellenelement (RelCubBezTo-Zeile)](relcubbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten des Endpunkts einer kubischen Bézierkurve relativ zur Breite und Höhe der Form, die X- und Y-Koordinaten des Kontrollpunkts am Anfang der Breite und Höhe der Kurve relativer Form sowie die X- und Y-Koordinaten des Kontrollpunkts des Endes der Breite und Höhe der Kurve relativer Form.  <br/> |
|[Zellenelement (RelQuadBezTo-Zeile)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe der Form sowie die x- und y-Koordinaten des Kontrollpunkts der Breite und Höhe der Kurve relativer Form.  <br/> |
|[Zellenelement (RelEllipticalArcTo-Zeile)](relellipticalarcto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält X- und Y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, x- und y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel von der X-Achse zur Hauptachse der Ellipse und Verhältnis zwischen den Haupt- und Nebenachsen der Ellipse.  <br/> |
|[Zellenelement (RelLineTo-Zeile)](rellineto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält X- und Y-Koordinaten des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite und Höhe eines Shapes.  <br/> |
|[Zellenelement (RelMoveTo-Zeile)](relmoveto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die X- und Y-Koordinaten des ersten Scheitelpunkts einer Form oder die X- und Y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite der Form.  <br/> |
|[Zellenelement (RelQuadBezTo-Zeile)](relquadbezto-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe der Form sowie die x- und y-Koordinaten des Kontrollpunkts der Breite und Höhe der Kurve relativer Form.  <br/> |
|[Zellenelement (SplineKnot-Zeile)](splineknot-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten für den Kontrollpunkt eines Splines und den Knoten eines Splines.  <br/> |
|[Zellenelement (SplineStart-Zeile)](splinestart-row-geometry-section.md) <br/> |[Cell_Type](https://msdn.microsoft.com/library/6f23bcc4-af93-4023-a380-3e78a228e166%28Office.15%29.aspx) <br/> |Enthält die x- und y-Koordinaten des zweiten Kontrollpunkts eines Splines, dessen zweiten Knoten, dessen ersten Knoten, den letzten Knoten und den Grad eines Splines.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.  <br/> |Werte des typs xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt den 1-basierten Bezeichner für die Zeile an. Er sollte unqiue und größer als andere Bezeichner im gleichen Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachabhängigen Namen der Zeile an.  <br/> |Werte des xsd:string-Typs.  <br/> |
|N  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des xsd:string-Typs.  <br/> |
|T  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird. Das T-Attribut wird nur für den Abschnitt Geometry verwendet.  <br/> |Werte des xsd:string-Typs.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **T-Attribut** dieses **Row-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zeilen entsprechen. In der folgenden Tabelle finden Sie  Informationen zu den Werten des T-Attributs, die für dieses **Row-Element zulässig** sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|ArcTo  <br/> |Enthält die x- und y-Koordinaten und die Krümmung eines kreisförmigen Bogens.  <br/> |[Zeile "ArcTo" (Abschnitt "Geometry")](arcto-row-geometry-section.md) <br/> |
|Ellipse  <br/> |Enthält die x- und y-Koordinaten des Mittelpunkts der Ellipse von zwei Punkten auf der Ellipse.  <br/> |[Zeile "Ellipse" (Abschnitt "Geometry")](ellipse-row-geometry-section.md) <br/> |
|EllipticalArcTo  <br/> |Enthält die x- und y-Koordinaten des elliptischen Endpunkts eines Bogens, die x- und y-Koordinaten der Kontrollpunkte des Bogens, den Winkel von der x-Achse zur größeren Achse der Ellipse und das Verhältnis zwischen der großen und der kleinen Achse der Ellipse.  <br/> |[Zeile "EllipticalArcTo" (Abschnitt "Geometry")](ellipticalarcto-row-geometry-section.md) <br/> |
|InfiniteLine  <br/> |Enthält die x- und y-Koordinaten von zwei Punkten einer unendlichen Linie.  <br/> |[Zeile "InfiniteLine" (Abschnitt "Geometry")](infiniteline-row-geometry-section.md) |
|LineTo  <br/> |Enthält die x-> und y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts.  <br/> |[Zeile "LineTo" (Abschnitt "Geometry")](lineto-row-geometry-section.md) <br/> |
|MoveTo  <br/> |Enthält die x- und y-Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die x- und y-Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke dar.  <br/> |[Zeile "MoveTo" (Abschnitt "Geometry")](moveto-row-geometry-section.md) <br/> |
|NURBSTo  <br/> |Enthält die x- und y-Koordinaten, die Positionen des zweiten bis letzten Knotens, die Position der letzen Stärke, die Position des ersten Knotens, die Position der ersten Stärke und die Formel für einen nicht-gleichförmigen rationalen B-Spline (NURBS).  <br/> |[Zeile "NURBSTo" (Abschnitt "Geometry")](nurbsto-row-geometry-section.md) <br/> |
|PolylineTo  <br/> |Enthält die x- und y-Koordinaten des letzten Punkts einer Polylinie und eine Polylinienformel.  <br/> |[Zeile "PolylineTo" (Abschnitt "Geometry")](polylineto-row-geometry-section.md) <br/> |
|RelCubBezTo  <br/> |Enthält die x- und y-Koordinaten des Endpunkts einer kubischen Bézierkurve relativ zur Breite und Höhe der Form, die X- und Y-Koordinaten des Kontrollpunkts am Anfang der Breite und Höhe der Kurve relativer Form sowie die X- und Y-Koordinaten des Kontrollpunkts des Endes der Breite und Höhe der Kurve relativer Form.  <br/> |[RelCubBezTo Row (Geometry Section)](relcubbezto-row-geometry-section.md) <br/> |
|RelEllipticalArcTo  <br/> |Enthält X- und Y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, x- und y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel von der X-Achse zur Hauptachse der Ellipse und Verhältnis zwischen den Haupt- und Nebenachsen der Ellipse.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|RelLineTo  <br/> |Enthält X- und Y-Koordinaten des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite und Höhe eines Shapes.  <br/> |[RelLineTo Row (Geometry Section)](rellineto-row-geometry-section.md) <br/> |
|RelMoveTo  <br/> |Enthält die X- und Y-Koordinaten des ersten Scheitelpunkts einer Form oder die X- und Y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite der Form.  <br/> |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
|RelQuadBezTo  <br/> |Enthält die x- und y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe der Form sowie die x- und y-Koordinaten des Kontrollpunkts der Breite und Höhe der Kurve relativer Form.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|SplineKnot  <br/> |Enthält die x- und y-Koordinaten für den Kontrollpunkt eines Splines und den Knoten eines Splines.  <br/> |[Zeile "SplineKnot" (Abschnitt "Geometry")](splineknot-row-geometry-section.md) <br/> |
|SplineStart  <br/> |Enthält die x- und y-Koordinaten des zweiten Kontrollpunkts eines Splines, dessen zweiten Knoten, dessen ersten Knoten, den letzten Knoten und den Grad eines Splines.  <br/> |[Zeile "SplineStart" (Abschnitt "Geometry")](splinestart-row-geometry-section.md) <br/> |
   

