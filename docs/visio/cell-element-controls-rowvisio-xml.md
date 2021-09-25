---
title: Zellenelement (Controls Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für ein Shape definiert ist.
ms.openlocfilehash: 45759522218736ddb6b08c3fd989658e08145fba
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615984"
---
# <a name="cell-element-controls-row-visio-xml"></a>Zellenelement (Controls Row) (Visio XML)

Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für ein Shape definiert ist.
  
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
|[Row-Element (Abschnitt "Controls")](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für ein Shape definiert ist.  <br/> |
   
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
   
## <a name="remarks"></a>Bemerkungen

Das **N-Attribut** dieses **Cell-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle finden Sie Informationen zu den Werten des **N-Attributs,** die für dieses **Cell-Element** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|CanGlue  <br/> |Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.  <br/> |[Zelle "Can Glue" (Abschnitt "Controls")](can-glue-cell-controls-section.md) <br/> |
|Eingabeaufforderung  <br/> |Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn der Mauszeiger über dem Steuerpunkt eines Shapes platziert wird.  <br/> |[Zelle "Tip" (Abschnitt "Controls")](tip-cell-controls-section.md) <br/> |
|X  <br/> |Stellt die x-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten anzeigt.  <br/> |[Zelle "X" (Abschnitt "Controls")](x-cell-controls-section.md) <br/> |
|Xcon  <br/> |Gibt die Art des Verhaltens an, das die X-Koordinate des Steuerpunkts nach dem Verschieben des Ziehpunkts aufweist.  <br/> |Keine  <br/> |
|xDyn  <br/> |Stellt die x-Koordinate für den Verankerungspunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |[Zelle "X Dynamics" (Abschnitt "Controls")](x-dynamics-cell-controls-section.md) <br/> |
|J  <br/> |Stellt die y-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten anzeigt.  <br/> |[Zelle "Y" (Abschnitt "Controls")](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Gibt die Art des Verhaltens an, das die Y-Koordinate des Steuerpunkts nach dem Verschieben des Ziehpunkts zeigt.  <br/> |Keine  <br/> |
|JJJN  <br/> |Stellt die y-Koordinate für den Verankerungspunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |[Zelle "Y Dynamics" (Abschnitt "Controls")](y-dynamics-cell-controls-section.md) <br/> |
   

