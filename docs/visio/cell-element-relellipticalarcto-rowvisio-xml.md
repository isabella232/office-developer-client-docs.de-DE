---
title: Cell-Element (RelEllipticalArcTo-Zeile) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Enthält X- oder Y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe des Shapes, x- oder y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel von der X-Achse zur Hauptachse der Ellipse oder Verhältnis zwischen den Haupt- und Nebenachsen der Ellipse.
ms.openlocfilehash: 84d7fe222cd46b54f38bc03e058103cc1d7a9620
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539432"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Cell-Element (RelEllipticalArcTo-Zeile) (Visio XML)

Enthält X- oder Y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe des Shapes, x- oder y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel von der X-Achse zur Hauptachse der Ellipse oder Verhältnis zwischen den Haupt- und Nebenachsen der Ellipse.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Enthält X- oder Y-Koordinaten des Endpunkts eines elliptischen Bogens relativ zur Breite und Höhe des Shapes, x- oder y-Koordinaten der Kontrollpunkte im Bogen relativ zur Breite und Höhe des Shapes, Winkel von der X-Achse zur Hauptachse der Ellipse oder Verhältnis zwischen den Haupt- und Nebenachsen der Ellipse.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehlermeldungszeichenfolge); Der Wert  des V-Attributs ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungszeichenfolge.  <br/> |
|F  <br/> |xsd:string  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  '(einige Formel)' wenn die Formel lokal vorhanden ist  <br/>  `No Formula` wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh` wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |xsd:string  <br/> |erforderlich  <br/> |Stellt den Namen der Zelle ShapeSheet dar.  <br/> |Der Name der Zelle ShapeSheet.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise".  <br/> |
|U  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar Die Standardeinstellung ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der Zelle ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N-Attribut** dieses **Cell-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle finden Sie  Informationen zu den Werten des N-Attributs, die für dieses **Cell-Element zulässig** sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|X  <br/> |Die X-Koordinate des endenden Scheitelpunkts in einem Bogen relativ zur Breite der Form.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|v  <br/> |Die y-Koordinate des endenden Scheitelpunkts in einem Bogen relativ zur Höhe der Form.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |Die X-Koordinate des Kontrollpunkts des Bogens relativ zur Breite des Shapes; einen Punkt im Bogen.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Die y-Koordinate des Kontrollpunkts eines Bogens relativ zur Breite des Shapes.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Der Winkel der Hauptachse eines Bogens relativ zur X-Achse des übergeordneten Bogens.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Das Verhältnis der Hauptachse eines Bogens zur Nebenachse eines Bogens.  <br/> |[RelEllipticalArcTo Row (Geometry Section)](relellipticalarcto-row-geometry-section.md) <br/> |
   

