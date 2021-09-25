---
title: Zellenelement (Zeile "RelQuadBezTo") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 8b3aea70-a69f-a85e-83d8-c0fa2ee68836
description: Enthält die X- oder Y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe des Shapes oder zu den X- oder Y-Koordinaten des Kontrollpunkts der relativen Breite und Höhe der Kurve.
ms.openlocfilehash: 5d40d49d7544660e1a525834aeea05d67c1a2f80
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578074"
---
# <a name="cell-element-relquadbezto-row-visio-xml"></a>Zellenelement (Zeile "RelQuadBezTo") (Visio XML)

Enthält die X- oder Y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe des Shapes oder zu den X- oder Y-Koordinaten des Kontrollpunkts der relativen Breite und Höhe der Kurve.
  
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

### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zeilenelement (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelQuadBezTo_Type](relquadbezto_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe des Shapes oder zu den X- oder Y-Koordinaten des Kontrollpunkts der relativen Breite und Höhe der Kurve.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehlermeldungszeichenfolge); Der Wert des **V-Attributs** ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungszeichenfolge.  <br/> |
|F  <br/> |xsd:string  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  '(some formula)', wenn die Formel lokal vorhanden ist  <br/>  `No Formula` wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh` wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |xsd:string  <br/> |erforderlich  <br/> |Stellt den Namen der Zelle ShapeSheet dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie unten im Abschnitt "Hinweise".  <br/> |
|U  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar. Der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **N-Attribut** dieses **Cell-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle finden Sie Informationen zu den Werten des **N-Attributs,** die für dieses **Cell-Element** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|X  <br/> |Die X-Koordinate des Endscheitelpunkts einer quadratischen Bézierkurve relativ zur Breite des Shapes.  <br/> |[Zeile "RelQuadBezTo" (Abschnitt "Geometry")](relquadbezto-row-geometry-section.md) <br/> |
|J  <br/> |Die Y-Koordinate des Endscheitelpunkts einer quadratischen Bézierkurve relativ zur Höhe des Shapes.  <br/> |[Zeile "RelQuadBezTo" (Abschnitt "Geometry")](relquadbezto-row-geometry-section.md) <br/> |
|A  <br/> |Die X-Koordinate des Kontrollpunkts der Kurve relativ zur Breite des Shapes; ein Punkt auf dem Bogen. Der Kontrollpunkt befindet sich am besten etwa in der Mitte zwischen den Anfangs- und Endscheitelpunkten des Bogens.  <br/> |[Zeile "RelQuadBezTo" (Abschnitt "Geometry")](relquadbezto-row-geometry-section.md) <br/> |
|B  <br/> |Die Y-Koordinate des Kontrollpunkts einer Kurve relativ zur Höhe des Shapes.  <br/> |[Zeile "RelQuadBezTo" (Abschnitt "Geometry")](relquadbezto-row-geometry-section.md) <br/> |
   

