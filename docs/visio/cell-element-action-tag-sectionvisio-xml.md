---
title: Zellenelement (Aktionstag Abschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6210ff71-fbcd-2c97-6dde-1e334891e08d
description: Eine Eigenschaft für ein Aktionstag definiert auf ein Shape oder Zeichenblatt.
ms.openlocfilehash: 0945235c49e77210564e50e5c111579ab37f3e31
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796559"
---
# <a name="cell-element-action-tag-section-visio-xml"></a>Zellenelement (Aktionstag Abschnitt) ("Visio XML")

Eine Eigenschaft für ein Aktionstag definiert auf ein Shape oder Zeichenblatt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Masters.XML, Master-Shape # .xml, pages.xml, Seite # .xml  <br/> |
   
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
|[Row-Element (ActionTag Abschnitt)](row-element-action-tag-sectionvisio-xml.md) <br/> |[ActionTagRow_Type](actiontag_type-complextypevisio-xml.md) <br/> |Ein Shape oder Zeichenblatt definiert ein Aktionstag.  <br/> |
   
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
|ButtonFace  <br/> |Enthält die ID der Schaltflächenoberseite, die auf der Schaltfläche Aktionstag angezeigt wird.  <br/> |[Zelle "ButtonFace" (Abschnitt "Action Tags")](buttonface-cell-action-tags-section.md) <br/> |
|Beschreibung  <br/> |Enthält eine Zeichenfolge als Beschreibung des Aktionstags, die als QuickInfo angezeigt wird, wenn der Zeiger über dem Tag platziert wird.  <br/> |[Zelle "Description" (Abschnitt "Action Tags")](description-cell-action-tags-section.md) <br/> |
|Deaktiviert  <br/> |Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.  <br/> |[Zelle "Disabled" (Abschnitt "Action Tags")](disabled-cell-action-tags-section.md) <br/> |
|DisplayMode  <br/> |Bestimmt, ob das Aktionstag angezeigt wird, wenn der Zeiger über das Tag bewegt wird, wenn das Shape ausgewählt ist oder immer.  <br/> |[DisplayMode Zelle (Abschnitt "Action Tags")](displaymode-cell-action-tags-section.md) <br/> |
|TagName  <br/> |Der Name des Aktionstags, das als Schlüssel verwendet wird, um das Aktionstag seinen Aktionen zuzuordnen.  <br/> |[Zelle "TagName" (Abschnitt "Action Tags")](tagname-cell-action-tags-section.md) <br/> |
|X  <br/> |Die X-Koordinate der lokalen Koordinaten des Shapes, um die herum die Schaltfläche Aktionstag platziert wird.  <br/> |[Zelle "X" (Abschnitt "Action Tags")](x-cell-action-tags-section.md) <br/> |
|XJustify  <br/> |Der X-Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.  <br/> |[Zelle "X Justify" (Abschnitt "Action Tags")](x-justify-cell-action-tags-section.md) <br/> |
|v  <br/> |Die Y-Koordinate der lokalen Koordinaten des Shapes, um die herum die Schaltfläche Aktionstag platziert wird.  <br/> |[Zelle "Y" (Abschnitt "Action Tags")](y-cell-action-tags-section.md) <br/> |
|YJustify  <br/> |Der Y-Abstand der Schaltfläche Aktionstag in Bezug auf den Punkt, der durch die Zellen X und Y definiert ist.  <br/> |[Zelle "Y Justify" (Abschnitt "Action Tags")](y-justify-cell-action-tags-section.md) <br/> |
   

