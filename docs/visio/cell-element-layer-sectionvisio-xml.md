---
title: Zellenelement (Abschnitt "Layer") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f9896839-ca36-b82b-7412-e57195d4b8e2
description: Gibt eine Eigenschaft für einen Layer oder deren Eigenschaften für eine Seite an.
ms.openlocfilehash: 9dd15521f54837b4203778472d6545b50c01d34e
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594874"
---
# <a name="cell-element-layer-section-visio-xml"></a>Zellenelement (Abschnitt "Layer") (Visio XML)

Gibt eine Eigenschaft für einen Layer oder deren Eigenschaften für eine Seite an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |masters.xml, pages.xml  <br/> |
   
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
|[Zeilenelement (Abschnitt "Layer")](row-element-layer-sectionvisio-xml.md) <br/> |[LayerRow_Type](layerrow_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft für einen Layer oder deren Eigenschaften für eine Seite an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehlermeldungszeichenfolge); Der Wert des **V-Attributs** ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungszeichenfolge.  <br/> |
|F  <br/> |xsd:string  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  '(some formula)', wenn die Formel lokal vorhanden ist  <br/>  `No Formula` wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh` wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |xsd:string  <br/> |erforderlich  <br/> |Stellt den Namen der Zelle ShapeSheet dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie unten im Abschnitt "Hinweise".  <br/> |
|U  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar. Der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **N-Attribut** dieses **Cell-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle finden Sie Informationen zu den Werten des **N-Attributs,** die für dieses **Cell-Element** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Aktiv  <br/> |Gibt an, ob ein Layer aktiv ist.  <br/> |Keine  <br/> |
|Farbe  <br/> |Gibt eine der folgenden Werte an: Der Index der Farbe in der Farbtabelle, die zum Anzeigen der Ebene verwendet wird, oder ein RGB-Wert, der eine benutzerdefinierte Farbe angibt, die nicht in der Farbtabelle enthalten ist.  <br/> |Keine  <br/> |
|ColorTrans  <br/> |Bestimmt den Grad der Transparenz für die Textfarbe einer Ebene oder Form von 0 (vollständig undurchsichtig) bis 1 (vollständig transparent).  <br/> |Keine  <br/> |
|Klebstoff  <br/> |Gibt an, ob Shapes, die zum Layer gehören, geklebt werden können.  <br/> |Keine  <br/> |
|Lock  <br/> |Gibt an, ob die dem Layer zugehörigen Shapes gesperrt sind, damit sie nicht ausgewählt oder bearbeitet werden können.  <br/> |Keine  <br/> |
|Name  <br/> |Der Name eines Layers.  <br/> |Keine  <br/> |
|NameUniv  <br/> |Gibt den universellen Namen eines Layers an.  <br/> |Keine  <br/> |
|Drucken  <br/> |Gibt an, ob Shapes, die zum Layer gehören, gedruckt werden, wenn die Zeichnung gedruckt wird.  <br/> |Keine  <br/> |
|Snap  <br/> |Gibt an, ob andere Shapes an Shapes ausrichten können, die dem Layer zugewiesen sind.  <br/> |Keine  <br/> |
|Status  <br/> |Gibt an, ob es sich bei der Ebene um eine gültige Ebene für ein Dokument handelt.  <br/> |Keine  <br/> |
|Visible  <br/> |Gibt an, ob die dem Layer zugehörigen Shapes auf dem Zeichenblatt sichtbar sind.  <br/> |None.  <br/> |
   

