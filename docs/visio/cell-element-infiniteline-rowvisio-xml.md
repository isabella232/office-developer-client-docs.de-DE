---
title: Cell-Element (InfiniteLine Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e14b8246-0064-3a54-7bd6-ad28180f9ea6
description: Enthält die X- oder Y-Koordinaten von zwei Punkten in einer unendlichen Linie.
ms.openlocfilehash: 1198e516a15e829b9a2da23491ca5f75e88a8e7d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539772"
---
# <a name="cell-element-infiniteline-row-visio-xml"></a>Cell-Element (InfiniteLine Row) (Visio XML)

Enthält die X- oder Y-Koordinaten von zwei Punkten in einer unendlichen Linie.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[InfiniteLine_Type](infiniteline_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten von zwei Punkten in einer unendlichen Linie.  <br/> |
   
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
|X  <br/> |Eine X-Koordinate eines Punkts auf der unendlichen Linie; gekoppelt mit y-Koordinate, die durch die Zelle Y dargestellt wird.  <br/> |[Zeile "InfiniteLine" (Abschnitt "Geometry")](infiniteline-row-geometry-section.md) <br/> |
|v  <br/> |Eine y-Koordinate eines Punkts auf der unendlichen Linie; gekoppelt mit x-Koordinate, die durch die Zelle X dargestellt wird.  <br/> |[Zeile "InfiniteLine" (Abschnitt "Geometry")](infiniteline-row-geometry-section.md) <br/> |
|A  <br/> |Die x-Koordinate eines Punkts auf der unendlichen Linie gepaart mit einer y-Koordinate, dargestellt durch die Zelle B.  <br/> |[Zeile "InfiniteLine" (Abschnitt "Geometry")](infiniteline-row-geometry-section.md) <br/> |
|B  <br/> |Die y-Koordinate eines Punkts auf der unendlichen Linie gepaart mit einer x-Koordinate, dargestellt durch die Zelle A.  <br/> |[Zeile "InfiniteLine" (Abschnitt "Geometry")](infiniteline-row-geometry-section.md) <br/> |
   

