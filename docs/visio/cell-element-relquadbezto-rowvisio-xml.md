---
title: Zellenelement (RelQuadBezTo Zeile) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b3aea70-a69f-a85e-83d8-c0fa2ee68836
description: Enthält die x- oder y-Koordinaten des Endpunkts des eine quadratische Bézier-Kurve relativ zur Höhe und Breite des Shapes oder die x- oder y-Koordinaten des Kontrollpunkts Breite und Höhe des relativen Kurve-Shapes.
ms.openlocfilehash: 986ed0a5f6e79f13b92f2ede54361916d9681e17
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388672"
---
# <a name="cell-element-relquadbezto-row-visio-xml"></a>Zellenelement (RelQuadBezTo Zeile) ("Visio XML")

Enthält die x- oder y-Koordinaten des Endpunkts des eine quadratische Bézier-Kurve relativ zur Höhe und Breite des Shapes oder die x- oder y-Koordinaten des Kontrollpunkts Breite und Höhe des relativen Kurve-Shapes.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |# .xml Master, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element ("Geometry")](row-element-geometry-sectionvisio-xml.md) <br/> |[RelQuadBezTo_Type](relquadbezto_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des Endpunkts des eine quadratische Bézier-Kurve relativ zur Höhe und Breite des Shapes oder die x- oder y-Koordinaten des Kontrollpunkts Breite und Höhe des relativen Kurve-Shapes.  <br/> |
   
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
|X  <br/> |Die X-Koordinate des Endscheitelpunkts eine quadratische Bézier-Kurve relativ zu der Breite der Form.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|v  <br/> |Die y-Koordinate des Endscheitelpunkts eine quadratische Bézier-Kurve relativ zur Höhe des Shapes.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|A  <br/> |Die X-Koordinate des Steuerelements für die Kurve zeigen relativ zu der Breite des Shapes. ein Punkt auf dem Bogen. Kontrollpunkts ist die beste in der Mitte zwischen dem ersten und letzten Scheitelpunkt des Bogens.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
|B  <br/> |Die y-Koordinate des Steuerelements einer Kurve zeigen relativ zur Höhe des Shapes.  <br/> |[RelQuadBezTo Row (Geometry Section)](relquadbezto-row-geometry-section.md) <br/> |
   

