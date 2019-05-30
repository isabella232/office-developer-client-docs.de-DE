---
title: Cell-Element (RelEllipticalArcTo Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Enthält die x-oder y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, die x-oder y-Koordinate der Kontrollpunkte des Bogens relativ zur Breite und Höhe des Shapes, von der x-Achse zur Hauptachse der Ellipse oder zum Verhältnis zwischen dem Haupt-und Nebenachsen der Ellipse.
ms.openlocfilehash: 84d7fe222cd46b54f38bc03e058103cc1d7a9620
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539432"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Cell-Element (RelEllipticalArcTo Row) (Visio XML)

Enthält die x-oder y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, die x-oder y-Koordinate der Kontrollpunkte des Bogens relativ zur Breite und Höhe des Shapes, von der x-Achse zur Hauptachse der Ellipse oder zum Verhältnis zwischen dem Haupt-und Nebenachsen der Ellipse.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Master #. XML, Seite #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe der Form, die x-oder y-Koordinate der Kontrollpunkte des Bogens relativ zur Breite und Höhe des Shapes, von der x-Achse zur Hauptachse der Ellipse oder zum Verhältnis zwischen dem Haupt-und Nebenachsen der Ellipse.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehler Meldungszeichenfolge); der Wert des **V** -Attributs ist der letzte gültige Wert.  <br/> |Eine Fehler Meldungszeichenfolge.  <br/> |
|F  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  "(eine Formel)", wenn die Formel lokal vorhanden ist  <br/>  `No Formula`Wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh`, wenn die Formel vererbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Stellt den Namen der ShapeSheet-Zelle dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.  <br/> |
|U  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar, bei der es sich bei der Standardeinstellung um DL handelt.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N** -Attribut dieses **Cell** -Elements muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle können Sie die Werte des **N** -Attributs bestimmen, die für dieses **Zellen** Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|X  <br/> |Die x-Koordinate des letzten Scheitelpunkts eines Bogens relativ zur Breite der Form.  <br/> |[Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|v  <br/> |Die y-Koordinate des letzten Scheitelpunkts eines Bogens relativ zur Höhe der Form.  <br/> |[Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |Die x-Koordinate des Kontrollpunktes des Bogens relativ zur Breite des Shapes; ein Eckpunkt auf dem Bogen.  <br/> |[Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Die y-Koordinate des Kontrollpunktes eines Bogens relativ zur Breite des Shapes.  <br/> |[Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Der Winkel der Hauptachse eines Bogens relativ zur x-Achse des übergeordneten Elements.  <br/> |[Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Das Verhältnis der Hauptachse eines Bogens zur Nebenachse.  <br/> |[Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
   

