---
title: Zellenelement (Zeile "RelCubBezTo") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: daa5c527-65fe-a1e4-ab3e-24e77bdb522b
description: Enthält die x- oder y-Koordinaten des Endpunkts einer kubischen Bézierkurve relativ zur Breite und Höhe des Shapes, die x- oder y-Koordinaten des Kontrollpunkts des Anfangspunkts der relativen Breite und Höhe der Kurve oder die x- oder y-Koordinaten des Kontrollpunkts des Endes der relativen Breite und Höhe der Kurve.
ms.openlocfilehash: 9dc19d4ac2059a31cc8be48a0a49ae8e9f53ca90
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608515"
---
# <a name="cell-element-relcubbezto-row-visio-xml"></a>Zellenelement (Zeile "RelCubBezTo") (Visio XML)

Enthält die x- oder y-Koordinaten des Endpunkts einer kubischen Bézierkurve relativ zur Breite und Höhe des Shapes, die x- oder y-Koordinaten des Kontrollpunkts des Anfangspunkts der relativen Breite und Höhe der Kurve oder die x- oder y-Koordinaten des Kontrollpunkts des Endes der relativen Breite und Höhe der Kurve.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zeilenelement (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelCubBezTo_Type](relcubbezto_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des Endpunkts einer kubischen Bézierkurve relativ zur Breite und Höhe des Shapes, die x- oder y-Koordinaten des Kontrollpunkts des Anfangspunkts der relativen Breite und Höhe der Kurve oder die x- oder y-Koordinaten des Kontrollpunkts des Endes der relativen Breite und Höhe der Kurve.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehlermeldungszeichenfolge); Der Wert des **V-Attributs** ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungszeichenfolge.  <br/> |
|F  <br/> |xsd:string  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  '(some formula)', wenn die Formel lokal vorhanden ist  <br/>  `No Formula` wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh` wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |xsd:string  <br/> |Erforderlich  <br/> |Stellt den Namen der Zelle ShapeSheet dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie unten im Abschnitt "Hinweise".  <br/> |
|U  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar. Der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **N-Attribut** dieses **Cell-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle finden Sie Informationen zu den Werten des **N-Attributs,** die für dieses **Cell-Element** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|X  <br/> |Die X-Koordinate des Endscheitelpunkts einer kubischen Bézierkurve relativ zur Breite des Shapes.  <br/> |[Zeile "RelCubBezTo" (Abschnitt "Geometry")](relcubbezto-row-geometry-section.md) <br/> |
|J  <br/> |Die Y-Koordinate des Endscheitelpunkts einer kubischen Bézierkurve relativ zur Höhe des Shapes.  <br/> |[Zeile "RelCubBezTo" (Abschnitt "Geometry")](relcubbezto-row-geometry-section.md) <br/> |
|A  <br/> |Die X-Koordinate des Anfangspunkts der Kurve relativ zur Breite des Shapes; ein Punkt auf dem Bogen. Der Kontrollpunkt befindet sich am besten zwischen den Anfangs- und Endscheitelpunkten des Bogens.  <br/> |[Zeile "RelCubBezTo" (Abschnitt "Geometry")](relcubbezto-row-geometry-section.md) <br/> |
|B  <br/> |Die Y-Koordinate des Anfangspunkts einer Kurve relativ zur Höhe des Shapes.  <br/> |[Zeile "RelCubBezTo" (Abschnitt "Geometry")](relcubbezto-row-geometry-section.md) <br/> |
|C  <br/> |Die X-Koordinate des Endpunktsteuerpunkts der Kurve relativ zur Breite des Shapes; ein Punkt auf dem Bogen. Der Kontrollpunkt befindet sich am besten zwischen dem Anfangssteuerpunkt und endenden Scheitelpunkten des Bogens.  <br/> |[Zeile "RelCubBezTo" (Abschnitt "Geometry")](relcubbezto-row-geometry-section.md) <br/> |
|D  <br/> |Die Y-Koordinate des Endpunktsteuerpunkts einer Kurve relativ zur Höhe des Shapes.  <br/> |[Zeile "RelCubBezTo" (Abschnitt "Geometry")](relcubbezto-row-geometry-section.md) <br/> |
   

