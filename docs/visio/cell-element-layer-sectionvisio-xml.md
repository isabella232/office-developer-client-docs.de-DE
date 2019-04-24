---
title: Cell-Element (Layer-Abschnitt) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Gibt eine Eigenschaft für eine Ebene oder deren Eigenschaften für eine Seite an.
ms.openlocfilehash: e96fdc1dcd5c9a7a2cb8753beaff766c2b477af2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318172"
---
# <a name="cell-element-layer-section-visio-xml"></a>Cell-Element (Layer-Abschnitt) (' Visio XML ')

Gibt eine Eigenschaft für eine Ebene oder deren Eigenschaften für eine Seite an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Masters. XML, Pages. XML  <br/> |
   
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
|[Row-Element (Layer-Abschnitt)](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft für eine Ebene oder deren Eigenschaften für eine Seite an.  <br/> |
   
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
|Aktiv  <br/> |Gibt an, ob eine Ebene aktiv ist.  <br/> |Keine.  <br/> |
|Farbe  <br/> |Gibt eine der folgenden Optionen an: den Index der Farbe in der Farbtabelle, die zum Anzeigen der Ebene verwendet wird, oder einen RGB-Wert, der eine benutzerdefinierte Farbe angibt, die sich nicht in der Farbtabelle befindet.  <br/> |Keine.  <br/> |
|ColorTrans  <br/> |Bestimmt den Grad der Transparenz für die Textfarbe eines Layers oder einer Form, von 0 (vollständig deckend) bis 1 (vollständig transparent).  <br/> |Keine.  <br/> |
|Glue  <br/> |Gibt an, ob Shapes, die zum Layer gehören, an geklebt werden können.  <br/> |Keine.  <br/> |
|Lock  <br/> |Gibt an, ob die dem Layer zugehörigen Shapes gesperrt sind, damit sie nicht ausgewählt oder bearbeitet werden können.  <br/> |Keine.  <br/> |
|Name  <br/> |Der Name eines Layers.  <br/> |Keine.  <br/> |
|NameUniv  <br/> |Gibt den universellen Namen eines Layers an.  <br/> |Keine.  <br/> |
|Print  <br/> |Gibt an, ob Formen, die zum Layer gehören, beim Drucken der Zeichnung gedruckt werden.  <br/> |Keine.  <br/> |
|Snap  <br/> |Gibt an, ob andere Shapes an Shapes ausgerichtet werden können, die der Ebene zugewiesen sind.  <br/> |Keine.  <br/> |
|Status  <br/> |Gibt an, ob es sich bei der Ebene um eine gültige Ebene für ein Dokument handelt.  <br/> |Keine.  <br/> |
|Visible  <br/> |Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.  <br/> |None.  <br/> |
   

