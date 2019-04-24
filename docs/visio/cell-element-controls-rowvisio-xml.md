---
title: Cell-Element (Controls-Zeile) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für ein Shape definiert ist.
ms.openlocfilehash: ea54865a645486dfba53688278cb380142899d77
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356091"
---
# <a name="cell-element-controls-row-visio-xml"></a>Cell-Element (Controls-Zeile) (' Visio XML ')

Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für ein Shape definiert ist.
  
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
|[Row-Element (Abschnitt "Controls")](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für einen bestimmten Steuerpunkt, der für ein Shape definiert ist.  <br/> |
   
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
|CanGlue  <br/> |Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.  <br/> |[Zelle "Can Glue" (Abschnitt "Controls")](can-glue-cell-controls-section.md) <br/> |
|Eingabeaufforderung  <br/> |Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn der Mauszeiger über dem Steuerpunkt eines Shapes platziert wird.  <br/> |[Zelle "Tip" (Abschnitt "Controls")](tip-cell-controls-section.md) <br/> |
|X  <br/> |Stellt die x-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten anzeigt.  <br/> |[Zelle "X" (Abschnitt "Controls")](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Gibt den Typ des Verhaltens an, das die x-Koordinate des Steuerpunkts aufweist, nachdem der Ziehpunkt verschoben wurde.  <br/> |Keine.  <br/> |
|xDyn  <br/> |Stellt die x-Koordinate für den Verankerungspunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |[Zelle "X Dynamics" (Abschnitt "Controls")](x-dynamics-cell-controls-section.md) <br/> |
|v  <br/> |Stellt die y-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten anzeigt.  <br/> |[Zelle "Y" (Abschnitt "Controls")](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Gibt den Typ des Verhaltens an, den die y-Koordinate des Steuerpunkts zeigt, nachdem der Ziehpunkt verschoben wurde.  <br/> |Keine.  <br/> |
|Y Dynamics  <br/> |Stellt die y-Koordinate für den Verankerungspunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |[Zelle "Y Dynamics" (Abschnitt "Controls")](y-dynamics-cell-controls-section.md) <br/> |
   

