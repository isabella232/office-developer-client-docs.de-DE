---
title: Zellenelement (Abschnitt "Geometry") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Definiert Eigenschaften, die formatierungs- und verhaltensbezogene Eigenschaften in Bezug auf die Linien und Bögen bestimmen, aus denen der Abschnitt "Geometry" bestehen.
ms.openlocfilehash: 838b7f20eab82718c2f8df21ae0b0037e76961db
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59628703"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Zellenelement (Abschnitt "Geometry") (Visio XML)

Definiert Eigenschaften, die formatierungs- und verhaltensbezogene Eigenschaften in Bezug auf die Linien und Bögen bestimmen, aus denen der Abschnitt "Geometry" bestehen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Zeilenelement (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Definiert Eigenschaften, die formatierungs- und verhaltensbezogene Eigenschaften in Bezug auf die Linien und Bögen bestimmen, aus denen der Abschnitt "Geometry" bestehen.  <br/> |
   
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
|NoFill  <br/> |Gibt an, ob ein Pfad gefüllt werden kann.  <br/> |[Zelle "NoFill" (Abschnitt "Geometry")](nofill-cell-geometry-section.md) <br/> |
|NoLine  <br/> |Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.  <br/> |[Zelle "NoLine" (Abschnitt "Geometry")](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den im Abschnitt Geometrie definierten ausgefüllten Bereich klickt.  <br/> |[Zelle "NoQuickDrag" (Abschnitt "Geometry")](noquickdrag-cell-geometry-section.md) <br/> |
|Noshow  <br/> |Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.  <br/> |[Zelle "NoShow" (Abschnitt "Geometry")](noshow-cell-geometry-section.md) <br/> |
|NoSnap  <br/> |Definiert, ob andere Shapes an einem Pfad einrasten.  <br/> |[Zelle "NoSnap" (Abschnitt "Geometry")](nosnap-cell-geometry-section.md) <br/> |
   

