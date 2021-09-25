---
title: Zellenelement (SplineStart Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 021536b9-6724-4b8a-35c2-966e456e5232
description: Enthält x- oder y-Koordinaten für den zweiten Kontrollpunkt eines Splines, dessen zweiten Knoten, seinen ersten Knoten, den letzten Knoten oder den Grad des Splines.
ms.openlocfilehash: 2c6a5caa7ecbc087e9623a789247e9d0f6c23b33
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578046"
---
# <a name="cell-element-splinestart-row-visio-xml"></a>Zellenelement (SplineStart Row) (Visio XML)

Enthält x- oder y-Koordinaten für den zweiten Kontrollpunkt eines Splines, dessen zweiten Knoten, seinen ersten Knoten, den letzten Knoten oder den Grad des Splines.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element>
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zeilenelement (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[SplineStart_Type](splinestart_type-complextypevisio-xml.md) <br/> |Enthält x- oder y-Koordinaten für den zweiten Kontrollpunkt eines Splines, dessen zweiten Knoten, seinen ersten Knoten, den letzten Knoten oder den Grad des Splines.  <br/> |
   
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
|X  <br/> |Die x-Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |[Zeile "SplineStart" (Abschnitt "Geometry")](splinestart-row-geometry-section.md) <br/> |
|J  <br/> |Die y-Koordinate des zweiten Kontrollpunkts eines Splines.  <br/> |[Zeile "SplineStart" (Abschnitt "Geometry")](splinestart-row-geometry-section.md) <br/> |
|A  <br/> |Der zweite Knoten des Splines.  <br/> |[Zeile "SplineStart" (Abschnitt "Geometry")](splinestart-row-geometry-section.md) <br/> |
|B  <br/> |Der erste Knoten eines Splines.  <br/> |[Zeile "SplineStart" (Abschnitt "Geometry")](splinestart-row-geometry-section.md) <br/> |
|C  <br/> |Der letzte Knoten eines Splines.  <br/> |[Zeile "RelEllipticalArcTo" (Abschnitt "Geometry")](splinestart-row-geometry-section.md) <br/> |
|D  <br/> |Der Grad eines Splines (eine Ganzzahl von 1 bis 25).  <br/> |[Zeile "SplineStart" (Abschnitt "Geometry")](splinestart-row-geometry-section.md) <br/> |
   

