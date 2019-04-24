---
title: Cell-Element (Actions-Zeile) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext-oder aktionstagmenü zugeordnet ist.
ms.openlocfilehash: 01b81a593de07be8059263d7a6e6538f31ed3be1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356273"
---
# <a name="cell-element-actions-row-visio-xml"></a>Cell-Element (Actions-Zeile) (' Visio XML ')

Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext-oder aktionstagmenü zugeordnet ist.
  
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
|[Row-Element (Actions section)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext-oder aktionstagmenü zugeordnet ist.  <br/> |
   
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
|Aktion  <br/> |Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer einen Befehl in einem Kontext- oder Aktionstagmenü auswählt.  <br/> |[Zelle "Action" (Abschnitt "Actions")](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird.  <br/> |[Zelle "BeginGroup" (Abschnitt "Actions")](begingroup-cell-actions-section.md) <br/> |
|"ButtonFace  <br/> |Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.  <br/> |[Zelle "ButtonFace" (Abschnitt "Actions")](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |Gibt an, ob ein Element im Kontext- oder Aktionstagmenü aktiviert ist.  <br/> |[Zelle "Checked" (Abschnitt "Actions")](checked-cell-actions-section.md) <br/> |
|Deaktiviert  <br/> |Gibt an, ob ein Element in einem Kontext- oder Aktionstagmenü deaktiviert ist.  <br/> |[Zelle "Disabled" (Abschnitt "Actions")](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt.  <br/> |[FlyoutChild Cell (Actions section)](flyoutchild-cell-actions-section.md) <br/> |
|Unsichtbar  <br/> |Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist.  <br/> |[Zelle "Invisible" (Abschnitt "Actions")](invisible-cell-actions-section.md) <br/> |
|Menü  <br/> |Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird.  <br/> |[Zelle "Menu" (Abschnitt "Actions")](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist.  <br/> |[Zelle "ReadOnly" (Abschnitt "Actions")](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Eine Zahl, mit der die Reihenfolge von Aktionen bestimmt wird, die in einem Kontext- oder Aktionstagmenü angezeigt werden.  <br/> |[Zelle "SortKey" (Abschnitt "Actions") SortKey Cell (Actions section)](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.  <br/> |[Zelle "TagName" (Abschnitt "Actions")](tagname-cell-actions-section.md) <br/> |
   

