---
title: Cell-Element (NURBSTo-Zeile) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e76bae8f-b9de-39ef-1f56-b00a6cd2ba6c
description: Enthält die x-oder y-Koordinaten, die Position des zweiten bis letzten Knotens, die Position der letzten Gewichtung, die Position des ersten Knotens, die Position der ersten Gewichtung oder die Formel für einen nicht einheitlichen rationalen B-Spline (NURBS).
ms.openlocfilehash: f23f73d67d72f9536dc7ffe9e083058ea9306217
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357694"
---
# <a name="cell-element-nurbsto-row-visio-xml"></a>Cell-Element (NURBSTo-Zeile) (' Visio XML ')

Enthält die x-oder y-Koordinaten, die Position des zweiten bis letzten Knotens, die Position der letzten Gewichtung, die Position des ersten Knotens, die Position der ersten Gewichtung oder die Formel für einen nicht einheitlichen rationalen B-Spline (NURBS).
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Master #. XML, Page #. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[NURBSTo_Type](nurbsto_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten, die Position des zweiten bis letzten Knotens, die Position der letzten Gewichtung, die Position des ersten Knotens, die Position der ersten Gewichtung oder die Formel für einen nicht einheitlichen rationalen B-Spline (NURBS).  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehler Meldungszeichenfolge); der Wert des **V** -Attributs ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungs-Zeichenfolge.  <br/> |
|F  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  ' (eine Formel) ', wenn die Formel lokal vorhanden ist  <br/>  `No Formula`Wenn die Formel lokal gelöscht oder gesperrt ist  <br/>  `Inh`Wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Stellt den Namen der ShapeSheet-Zelle dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise" unten.  <br/> |
|U  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **N** -Attribut dieses **Cell** -Elements muss einer einer begrenzten Menge von Werten sein, die ShapeSheet-Zellen entsprechen. In der nachstehenden Tabelle finden Sie die Werte des **N** -Attributs, die für dieses **Cell** -Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|X  <br/> |Die x-Koordinate des letzten Kontrollpunkts eines NURBS.  <br/> |[Zeile "NURBSTo" (Abschnitt "Geometry")](nurbsto-row-geometry-section.md) <br/> |
|v  <br/> |Die y-Koordinate des letzten Kontrollpunkts eines NURBS.  <br/> |[Zeile "NURBSTo" (Abschnitt "Geometry")](nurbsto-row-geometry-section.md) <br/> |
|A  <br/> |Der zweite bis letzte Knoten des NURBS.  <br/> |[Zeile "NURBSTo" (Abschnitt "Geometry")](nurbsto-row-geometry-section.md) <br/> |
|B  <br/> |Die letzte Stärke des NURBS.  <br/> |[Zeile "NURBSTo" (Abschnitt "Geometry")](nurbsto-row-geometry-section.md) <br/> |
|C  <br/> |Der erste Knoten des NURBS.  <br/> |[Zeile "NURBSTo" (Abschnitt "Geometry")](nurbsto-row-geometry-section.md) <br/> |
|D  <br/> |Die erste Stärke des NURBS.  <br/> |[Zeile "NURBSTo" (Abschnitt "Geometry")](nurbsto-row-geometry-section.md) <br/> |
|E  <br/> |Die Formel für einen NURBS.  <br/> |[Zeile "NURBSTo" (Abschnitt "Geometry")](nurbsto-row-geometry-section.md) <br/> |
   

