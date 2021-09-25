---
title: Zellenelement (Abschnitt "Action Tag") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Definiert eine Eigenschaft für ein Aktionstag in einem Shape oder Zeichenblatt.
ms.openlocfilehash: ca7c75f364209b2f40d17b4830128d729d762c34
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59615998"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Zellenelement (Abschnitt "Action Tag") (Visio XML)

Definiert eine Eigenschaft für ein Aktionstag in einem Shape oder Zeichenblatt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |masters.xml, master#.xml, pages.xml, page#.xml  <br/> |
   
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
|[Row-Element (Abschnitt "ActionTag")](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Definiert ein Aktionstag auf einem Shape oder Zeichenblatt.  <br/> |
   
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
|ButtonFace  <br/> |Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.  <br/> |[Zelle "ButtonFace" (Abschnitt "Action Tags")](buttonface-cell-action-tags-section.md) <br/> |
|Beschreibung  <br/> |Enthält eine Zeichenfolge als Beschreibung des Aktionstags, die als QuickInfo angezeigt wird, wenn der Zeiger über dem Tag platziert wird.  <br/> |[Zelle "Description" (Abschnitt "Action Tags")](description-cell-action-tags-section.md) <br/> |
|Deaktiviert  <br/> |Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.  <br/> |[Zelle "Disabled" (Abschnitt "Action Tags")](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist oder immer.  <br/> |[DisplayMode Zelle (Abschnitt "Action Tags")](displaymode-cell-action-tags-section.md) <br/> |
|Tagname  <br/> |Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.  <br/> |[Zelle "TagName" (Abschnitt "Action Tags")](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |Die X-Koordinatenposition in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche des Aktionstags befindet.  <br/> |[Zelle "X" (Abschnitt "Action Tags")](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Der X-Offset der Aktionstag-Schaltfläche relativ zu dem von den Zellen X und Y definierten Punkt.  <br/> |[Zelle "X Justify" (Abschnitt "Action Tags")](x-justify-cell-action-tags-section.md) <br/> |
|J  <br/> |Die Y-Koordinatenposition in den lokalen Koordinaten des Shapes, um die sich die Aktionstagschaltfläche befindet.  <br/> |[Zelle "Y" (Abschnitt "Action Tags")](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |Der Y-Offset der Aktionstag-Schaltfläche relativ zu dem von den Zellen X und Y definierten Punkt.  <br/> |[Zelle "Y Justify" (Abschnitt "Action Tags")](y-justify-cell-action-tags-section.md) <br/> |
   

