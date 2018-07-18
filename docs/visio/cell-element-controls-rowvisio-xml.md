---
title: Zellenelement (Zeile mit Steuerelementen) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 3c04d243-002c-bb00-a4be-0bcb8e156402
description: Enthält eine Eigenschaft für ein bestimmtes Steuerpunkt eines Shapes definiert.
ms.openlocfilehash: ff9bd2111b0f5a6544638fb7b33a1a9b797ede7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796586"
---
# <a name="cell-element-controls-row-visio-xml"></a>Zellenelement (Zeile mit Steuerelementen) ("Visio XML")

Enthält eine Eigenschaft für ein bestimmtes Steuerpunkt eines Shapes definiert.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |# .xml Master, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Zeilenelement (Steuerelementzeile)](row-element-controls-sectionvisio-xml.md) <br/> |[ControlRow_Type](controlrow_type-complextypevisio-xml.md) <br/> |Enthält eine Eigenschaft für ein bestimmtes Steuerpunkt eines Shapes definiert.  <br/> |
   
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
   
## <a name="remarks"></a>Bemerkungen

Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen. Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|CanGlue  <br/> |Legt fest, ob ein Steuerpunkt an andere Shapes geklebt werden kann.  <br/> |[Zelle "Can Glue" (Abschnitt "Controls")](can-glue-cell-controls-section.md) <br/> |
|Prompt  <br/> |Enthält einen beschreibenden Text, der als QuickInfo angezeigt wird, wenn der Mauszeiger über dem Steuerpunkt eines Shapes platziert wird.  <br/> |[Zelle "Tip" (Abschnitt "Controls")](tip-cell-controls-section.md) <br/> |
|X  <br/> |Stellt die X-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten anzeigt.  <br/> |[Zelle "X" (Abschnitt "Controls")](x-cell-controls-section.md) <br/> |
|xCon  <br/> |Gibt den Typ des Verhaltens die X-Koordinate des der Steuerpunkt aufweist, wenn dieser verschoben wird.  <br/> |Keine.  <br/> |
|xDyn  <br/> |Stellt die x-Koordinate für den Verankerungspunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |[Zelle "X Dynamics" (Abschnitt "Controls")](x-dynamics-cell-controls-section.md) <br/> |
|v  <br/> |Stellt die Y-Koordinate dar, die die Position des Steuerpunkts eines Shapes in lokalen Koordinaten anzeigt.  <br/> |[Zelle "Y" (Abschnitt "Controls")](y-cell-controls-section.md) <br/> |
|YCon  <br/> |Gibt den Typ des Verhalten, das die y-Koordinate des der Steuerpunkt aufweisen wird, wenn dieser verschoben wird.  <br/> |Keine.  <br/> |
|YDyn  <br/> |Stellt die y-Koordinate für den Verankerungspunkt eines Steuerpunkts in lokalen Koordinaten dar.  <br/> |[Zelle "Y Dynamics" (Abschnitt "Controls")](y-dynamics-cell-controls-section.md) <br/> |
   

