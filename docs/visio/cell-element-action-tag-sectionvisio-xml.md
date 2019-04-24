---
title: Cell-Element (Action Tag section) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Definiert eine Eigenschaft für ein Aktionstag auf einem Shape oder einer Seite.
ms.openlocfilehash: 61fad8575532adde0106ef6db2888fe38f3ae4b7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32337177"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Cell-Element (Action Tag section) (' Visio XML ')

Definiert eine Eigenschaft für ein Aktionstag auf einem Shape oder einer Seite.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |"Masters. xml", "Master #. xml", "pages. xml", "page #. xml"  <br/> |
   
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
|[Row-Element (ActionTag-Abschnitt)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Definiert ein Aktionstag auf einem Shape oder einer Seite.  <br/> |
   
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
|"ButtonFace  <br/> |Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.  <br/> |[Zelle "ButtonFace" (Abschnitt "Action Tags")](buttonface-cell-action-tags-section.md) <br/> |
|Beschreibung  <br/> |Enthält eine Zeichenfolge als Beschreibung des Aktionstags, die als QuickInfo angezeigt wird, wenn der Zeiger über dem Tag platziert wird.  <br/> |[Zelle "Description" (Abschnitt "Action Tags")](description-cell-action-tags-section.md) <br/> |
|Deaktiviert  <br/> |Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.  <br/> |[Zelle "Disabled" (Abschnitt "Action Tags")](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist, oder die ganze Zeit.  <br/> |[DisplayMode Zelle (Abschnitt "Action Tags")](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.  <br/> |[Zelle "TagName" (Abschnitt "Action Tags")](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |Die x-Koordinate in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche Aktionstag befindet.  <br/> |[Zelle "X" (Abschnitt "Action Tags")](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Der x-Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.  <br/> |[Zelle "X Justify" (Abschnitt "Action Tags")](x-justify-cell-action-tags-section.md) <br/> |
|v  <br/> |Die y-Koordinatenposition in den lokalen Koordinaten des Shapes, um die sich die Schaltfläche Aktionstag befindet.  <br/> |[Zelle "Y" (Abschnitt "Action Tags")](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |Der y-Offset der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.  <br/> |[Zelle "Y Justify" (Abschnitt "Action Tags")](y-justify-cell-action-tags-section.md) <br/> |
   

