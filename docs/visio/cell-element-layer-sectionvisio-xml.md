---
title: Zellenelement (Layer Abschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Gibt eine Eigenschaft für eine Ebene oder seine Eigenschaften für eine Seite.
ms.openlocfilehash: e96fdc1dcd5c9a7a2cb8753beaff766c2b477af2
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390975"
---
# <a name="cell-element-layer-section-visio-xml"></a>Zellenelement (Layer Abschnitt) ("Visio XML")

Gibt eine Eigenschaft für eine Ebene oder seine Eigenschaften für eine Seite.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Masters.XML, pages.xml  <br/> |
   
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
|[Zeilenelement (Ebenenabschnitt)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft für eine Ebene oder seine Eigenschaften für eine Seite.  <br/> |
   
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
|Aktiv  <br/> |Gibt an, ob eine Ebene aktiv ist.  <br/> |Keine.  <br/> |
|Farbe  <br/> |Gibt eine der folgenden: der Index der Farbe in der Tabelle verwendet, um die Ebene oder einen RGB-Wert festlegen einer benutzerdefinierten Farbe nicht in der Tabelle anzuzeigen.  <br/> |Keine.  <br/> |
|ColorTrans  <br/> |Bestimmt den Grad der Transparenz für eine Ebene oder Textfarbe Shapes im Bereich von 0 (vollständig undurchsichtig) und 1 (vollständig transparent).  <br/> |Keine.  <br/> |
|Kleber  <br/> |Gibt an, ob auf dem Layer zugehörigen Shapes geklebt werden können.  <br/> |Keine.  <br/> |
|Lock  <br/> |Gibt an, ob die dem Layer zugehörigen Shapes gesperrt sind, damit sie nicht ausgewählt oder bearbeitet werden können.  <br/> |Keine.  <br/> |
|Name  <br/> |Der Name einer Ebene.  <br/> |Keine.  <br/> |
|NameUniv  <br/> |Gibt den universellen Namen einer Ebene.  <br/> |Keine.  <br/> |
|Drucken  <br/> |Gibt an, ob dem Layer zugehörigen Shapes gedruckt werden, wenn die Zeichnung gedruckt wird.  <br/> |Keine.  <br/> |
|Ausrichten  <br/> |Gibt an, ob andere Shapes an den dem Layer zugeordneten Shapes Einrasten können.  <br/> |Keine.  <br/> |
|Status  <br/> |Gibt an, ob die Ebene einer gültigen Ebene für ein Dokument ist.  <br/> |Keine.  <br/> |
|Visible  <br/> |Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.  <br/> |Keine.  <br/> |
   

