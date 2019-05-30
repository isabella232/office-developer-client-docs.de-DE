---
title: Cell-Element (Aktions-Tag-Abschnitt) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Definiert eine Eigenschaft für ein Action-Tag auf einem Shape oder einer Seite.
ms.openlocfilehash: 3b43206838dae432df677a3ff8792c85328db53b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538802"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Cell-Element (Aktions-Tag-Abschnitt) (Visio XML)

Definiert eine Eigenschaft für ein Action-Tag auf einem Shape oder einer Seite.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Masters. XML, Master #. XML, Pages. XML, Page #. XML  <br/> |
   
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
|[Row-Element (ActionTag-Abschnitt)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Definiert ein Action-Tag auf einem Shape oder einer Seite.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehler Meldungszeichenfolge); der Wert des **V** -Attributs ist der letzte gültige Wert.  <br/> |Eine Fehler Meldungszeichenfolge.  <br/> |
|F  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  "(eine Formel)", wenn die Formel lokal vorhanden ist  <br/>  `No Formula`Wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh`, wenn die Formel vererbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Stellt den Namen der ShapeSheet-Zelle dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.  <br/> |
|U  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar, bei der es sich bei der Standardeinstellung um DL handelt.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N** -Attribut dieses **Cell** -Elements muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle können Sie die Werte des **N** -Attributs bestimmen, die für dieses **Zellen** Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|ButtonFace  <br/> |Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.  <br/> |[Zelle "ButtonFace" (Abschnitt "Action Tags")](buttonface-cell-action-tags-section.md) <br/> |
|Beschreibung  <br/> |Enthält eine Zeichenfolge als Beschreibung des Aktionstags, die als QuickInfo angezeigt wird, wenn der Zeiger über dem Tag platziert wird.  <br/> |[Zelle "Description" (Abschnitt "Action Tags")](description-cell-action-tags-section.md) <br/> |
|Deaktiviert  <br/> |Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.  <br/> |[Zelle "Disabled" (Abschnitt "Action Tags")](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist, oder die ganze Zeit.  <br/> |[DisplayMode Zelle (Abschnitt "Action Tags")](displaymode-cell-action-tags-section.md) <br/> |
|Tagname  <br/> |Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.  <br/> |[Zelle "TagName" (Abschnitt "Action Tags")](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |Die Position der x-Koordinate in den lokalen Koordinaten des Shapes, um die herum die Schaltfläche Aktionstag eingefügt wird.  <br/> |[Zelle "X" (Abschnitt "Action Tags")](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Der x-Offset der Aktions-Tag-Schaltfläche relativ zu dem durch die Zellen x und Y definierten Punkt.  <br/> |[Zelle "X Justify" (Abschnitt "Action Tags")](x-justify-cell-action-tags-section.md) <br/> |
|v  <br/> |Die Position der y-Koordinate in den lokalen Koordinaten des Shapes, um die herum die Schaltfläche Aktionstag eingefügt wird.  <br/> |[Zelle "Y" (Abschnitt "Action Tags")](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |Der y-Offset der Aktionstags-Schaltfläche relativ zu dem durch die Zellen X und y definierten Punkt.  <br/> |[Zelle "Y Justify" (Abschnitt "Action Tags")](y-justify-cell-action-tags-section.md) <br/> |
   

