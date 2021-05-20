---
title: Cell-Element (RelMoveTo-Zeile) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8e91497c-0aa1-2021-9317-cf989e5b84a3
description: Enthält die x- oder y-Koordinaten des ersten Scheitelpunkts einer Form oder die X- oder Y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite der Form.
ms.openlocfilehash: 6ec7990887ed59ae229e88b6ad02a7759c770700
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539404"
---
# <a name="cell-element-relmoveto-row-visio-xml"></a>Cell-Element (RelMoveTo-Zeile) (Visio XML)

Enthält die x- oder y-Koordinaten des ersten Scheitelpunkts einer Form oder die X- oder Y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite der Form.
  
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
|[Row-Element (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelMoveTo_Type](relmoveto_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten des ersten Scheitelpunkts einer Form oder die X- oder Y-Koordinaten des ersten Scheitelpunkts nach einem Umbruch in einem Pfad relativ zur Höhe und Breite der Form.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf eine Seite an.  <br/> |
   
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
|X  <br/> |Wenn die **Zeile RelMoveTo** die erste Zeile im Abschnitt ist, stellt die **Zelle X** die X-Koordinate des ersten Scheitelpunkts einer Form relativ zur Breite der Form dar. Wenn die **Zeile RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die **Zelle X** die X-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.  <br/> |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
|v  <br/> |Wenn die **Zeile RelMoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts einer Form relativ zur Höhe der Form dar.  Wenn die **Zeile RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.   <br/> |[RelMoveTo Row (Geometry Section)](relmoveto-row-geometry-section.md) <br/> |
   

