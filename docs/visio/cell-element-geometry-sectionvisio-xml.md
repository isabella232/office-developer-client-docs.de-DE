---
title: Cell-Element (Abschnitt "Geometry") (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Definiert Eigenschaften, mit denen die Formatierungs-und Verhaltenseigenschaften in Bezug auf die Linien und Bögen bestimmt werden, aus denen sich der Geometry-Abschnitt zusammensetzt.
ms.openlocfilehash: ebfdb4dc7809f8883143fdda39f873a36f7bf896
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356056"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Cell-Element (Abschnitt "Geometry") (' Visio XML ')

Definiert Eigenschaften, mit denen die Formatierungs-und Verhaltenseigenschaften in Bezug auf die Linien und Bögen bestimmt werden, aus denen sich der Geometry-Abschnitt zusammensetzt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Master #. XML, Page #. XML  <br/> |
   
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
|[Row-Element (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Definiert Eigenschaften, mit denen die Formatierungs-und Verhaltenseigenschaften in Bezug auf die Linien und Bögen bestimmt werden, aus denen sich der Geometry-Abschnitt zusammensetzt.  <br/> |
   
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
|NoFill  <br/> |Gibt an, ob ein Pfad gefüllt werden kann.  <br/> |[Zelle "NoFill" (Abschnitt "Geometry")](nofill-cell-geometry-section.md) <br/> |
|Zelle NoLine  <br/> |Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.  <br/> |[Zelle "NoLine" (Abschnitt "Geometry")](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Bestimmt, ob ein Shape ausgewählt oder gezogen werden kann, wenn der Benutzer auf den durch den Abschnitt Geometrie definierten gefüllten Bereich klickt.  <br/> |[Zelle "NoQuickDrag" (Abschnitt "Geometry")](noquickdrag-cell-geometry-section.md) <br/> |
|NoShow  <br/> |Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.  <br/> |[Zelle "NoShow" (Abschnitt "Geometry")](noshow-cell-geometry-section.md) <br/> |
|Zelle NoSnap  <br/> |Definiert, ob andere Shapes an einem Pfad einrasten.  <br/> |[Zelle "NoSnap" (Abschnitt "Geometry")](nosnap-cell-geometry-section.md) <br/> |
   

