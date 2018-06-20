---
title: Zellenelement (RelEllipticalArcTo Zeile) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: beaa8860-807e-c8dd-8a59-29cd0f91ba45
description: Enthält x- oder y-Koordinaten des Endpunkts der eines elliptischen Bogens relativ zur Höhe und Breite des Shapes x- oder y-Koordinaten des Steuerelements Kontrollpunkte des Bogens relativ zur Breite und Höhe, Winkel zwischen der x-Achse großen Achse der Ellipse oder das Verhältnis zwischen des Shapes die Haupt- und Hilfsintervalle Achse der Ellipse
ms.openlocfilehash: 661f6971ca4c03c68950ead45065bd12160918d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796608"
---
# <a name="cell-element-relellipticalarcto-row-visio-xml"></a>Zellenelement (RelEllipticalArcTo Zeile) ("Visio XML")

Enthält x- oder y-Koordinaten des Endpunkts der eines elliptischen Bogens relativ zur Höhe und Breite des Shapes x- oder y-Koordinaten des Steuerelements Kontrollpunkte des Bogens relativ zur Breite und Höhe, Winkel zwischen der x-Achse großen Achse der Ellipse oder das Verhältnis zwischen des Shapes die Haupt- und Hilfsintervalle Achse der Ellipse
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |# .xml Master, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded">
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element ("Geometry")](row-element-geometry-sectionvisio-xml.md) <br/> |[RelEllipticalArcTo_Type](relellipticalarcto_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten des Endpunkts der eines elliptischen Bogens relativ zur Höhe und Breite des Shapes x- oder y-Koordinaten des Steuerelements Kontrollpunkte des Bogens relativ zur Breite und Höhe, Winkel zwischen der x-Achse großen Achse der Ellipse oder das Verhältnis zwischen des Shapes die Haupt- und Hilfsintervalle Achse der Ellipse  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt an, dass die Formel einen Fehler zurückgibt. Der Wert von **E** ist der aktuelle Wert (Zeichenfolge mit einer Fehlermeldung); der Wert des Attributs **V** ist der letzte gültige Wert.  <br/> |Zeichenfolge mit einer Fehlermeldung.  <br/> |
|F  <br/> |XSD: String  <br/> |Optional  <br/> | Formel für das Element darstellt. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  "(einige Formel)" Wenn die Formel lokal vorhanden ist.  <br/>  `No Formula`Wenn die Formel lokal gelöscht oder blockiert ist.  <br/>  `Inh`Wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |XSD: String  <br/> |erforderlich  <br/> |Der Name der ShapeSheet-Zelle darstellt.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Siehe Abschnitt "Hinweise".  <br/> |
|U  <br/> |XSD: String  <br/> |Optional  <br/> |Stellt eine Einheit der Messung der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |XSD: String  <br/> |Optional  <br/> |Den Wert der Zelle darstellt.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen. Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|X  <br/> |Die X-Koordinate des Endscheitelpunkts eines Bogens relativ zu der Breite der Form.  <br/> |[RelEllipticalArcTo Zeile (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|v  <br/> |Die y-Koordinate des Endscheitelpunkts eines Bogens relativ zur Höhe des Shapes.  <br/> |[RelEllipticalArcTo Zeile (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|A  <br/> |Zeigen Sie die X-Koordinate des des Bogens relativ zu der Breite des Shapes. ein Punkt auf dem Bogen.  <br/> |[RelEllipticalArcTo Zeile (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|B  <br/> |Zeigen Sie die y-Koordinate des Steuerelements eines Bogens relativ zu der Breite des Shapes.  <br/> |[RelEllipticalArcTo Zeile (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|C  <br/> |Der Winkel der Größenachse des Bogens relativ zur x-Achse des übergeordneten Objekts.  <br/> |[RelEllipticalArcTo Zeile (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
|D  <br/> |Das Verhältnis der Größenachse zur kleineren Achse eines Bogens.  <br/> |[RelEllipticalArcTo Zeile (Abschnitt "Geometry")](relellipticalarcto-row-geometry-section.md) <br/> |
   

