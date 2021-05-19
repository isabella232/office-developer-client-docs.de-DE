---
title: Cell-Element (Controls Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Enthält eine Eigenschaft für ein bestimmtes Steuerelementhandle, das für eine Form definiert ist.
ms.openlocfilehash: 662dfe730c92ae25b3d243364bf1fa22a5eb8605
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541834"
---
# <a name="cell-element-controls-row-visio-xml"></a>Cell-Element (Controls Row) (Visio XML)

Enthält eine Eigenschaft für ein bestimmtes Steuerelementhandle, das für eine Form definiert ist.
  
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
|[Row-Element (Abschnitt "Controls")](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für ein bestimmtes Steuerelementhandle, das für eine Form definiert ist.  <br/> |
   
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
|CanGlue  <br/> |Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.  <br/> |[Zelle "Can Glue" (Abschnitt "Controls")](can-glue-cell-controls-section.md) <br/> |
|Eingabeaufforderung  <br/> |Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn der Mauszeiger über dem Steuerpunkt eines Shapes platziert wird.  <br/> |[Zelle "Tip" (Abschnitt "Controls")](tip-cell-controls-section.md) <br/> |
|X  <br/> |Stellt die x-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten anzeigt.  <br/> |[Zelle "X" (Abschnitt "Controls")](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Gibt den Verhaltentyp an, den die X-Koordinate des Steuerelementhandpunkts nach dem Verschoben des Handles zeigt.  <br/> |Keine.  <br/> |
|xDyn  <br/> |Stellt die x-Koordinate für den Verankerungspunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |[Zelle "X Dynamics" (Abschnitt "Controls")](x-dynamics-cell-controls-section.md) <br/> |
|v  <br/> |Stellt die y-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten anzeigt.  <br/> |[Zelle "Y" (Abschnitt "Controls")](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Gibt den Typ des Verhaltens an, das die y-Koordinate des Steuerelementhandles nach dem Verschoben des Handles zeigt.  <br/> |Keine.  <br/> |
|YDyn  <br/> |Stellt die y-Koordinate für den Verankerungspunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |[Zelle "Y Dynamics" (Abschnitt "Controls")](y-dynamics-cell-controls-section.md) <br/> |
   

