---
title: Zellenelement (Zeile Actions) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae2b4db-03f4-1b8a-1274-7eb1521f2f59
description: Gibt eine Eigenschaft einer Aktion in einem Kontext- oder Aktionstagmenü eines benutzerdefinierten Befehls zugeordnet.
ms.openlocfilehash: 01b81a593de07be8059263d7a6e6538f31ed3be1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25395672"
---
# <a name="cell-element-actions-row-visio-xml"></a>Zellenelement (Zeile Actions) ("Visio XML")

Gibt eine Eigenschaft einer Aktion in einem Kontext- oder Aktionstagmenü eines benutzerdefinierten Befehls zugeordnet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Zeilenelement (Aktionenzeile)](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft einer Aktion in einem Kontext- oder Aktionstagmenü eines benutzerdefinierten Befehls zugeordnet.  <br/> |
   
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
   
## <a name="remarks"></a>Hinweise

Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen. Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Aktion  <br/> |Enthält die Formel, die ausgeführt werden soll, wenn ein Benutzer einen Befehl in einem Kontext- oder Aktionstagmenü auswählt.  <br/> |[Zelle "Action" (Abschnitt "Actions")](action-cell-actions-section.md) <br/> |
|BeginGroup  <br/> |Gibt an, ob über dieser Aktion ein Trennzeichen in das Menü eingefügt wird.  <br/> |[Zelle "BeginGroup" (Abschnitt "Actions")](begingroup-cell-actions-section.md) <br/> |
|ButtonFace  <br/> |Bestimmt das Symbol, das neben einem Element in einem Kontext- oder Aktionstagmenü angezeigt wird.  <br/> |[Zelle "ButtonFace" (Abschnitt "Actions")](buttonface-cell-actions-section.md) <br/> |
|Checked  <br/> |Gibt an, ob ein Element im Kontext- oder Aktionstagmenü aktiviert ist.  <br/> |[Zelle "Checked" (Abschnitt "Actions")](checked-cell-actions-section.md) <br/> |
|Deaktiviert  <br/> |Gibt an, ob ein Element in einem Kontext- oder Aktionstagmenü deaktiviert ist.  <br/> |[Zelle "Disabled" (Abschnitt "Actions")](disabled-cell-actions-section.md) <br/> |
|FlyoutChild  <br/> |Bestimmt, ob die Zeile ein untergeordnetes Erweiterungsmenü der letzten Zeile oberhalb befindlichen Zeile ist, bei der es sich nicht um eine untergeordnete Erweiterung handelt.  <br/> |[FlyoutChild Cell (Actions Section)](flyoutchild-cell-actions-section.md) <br/> |
|Nicht sichtbare  <br/> |Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist.  <br/> |[Zelle "Invisible" (Abschnitt "Actions")](invisible-cell-actions-section.md) <br/> |
|Menü  <br/> |Definiert den Namen eines Menüelements, das in einem Kontext- oder Aktionstagmenü für ein Shape oder Zeichenblatt angezeigt wird.  <br/> |[Zelle "Menu" (Abschnitt "Actions")](menu-cell-actions-section.md) <br/> |
|ReadOnly  <br/> |Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist.  <br/> |[Zelle "ReadOnly" (Abschnitt "Actions")](readonly-cell-actions-section.md) <br/> |
|SortKey  <br/> |Eine Zahl, mit der die Reihenfolge von Aktionen bestimmt wird, die in einem Kontext- oder Aktionstagmenü angezeigt werden.  <br/> |[Zelle "SortKey" (Abschnitt "Actions") Zelle "SortKey" (Abschnitt "Actions")](sortkey-cell-actions-section.md) <br/> |
|TagName  <br/> |Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.  <br/> |[Zelle "TagName" (Abschnitt "Actions")](tagname-cell-actions-section.md) <br/> |
   

