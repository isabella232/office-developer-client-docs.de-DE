---
title: Zellenelement (Abschnitt "Geometry") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 82dcad38-d5fa-4892-91d9-1f3f25f1e600
description: Definiert die Eigenschaften, die bestimmen, Formatierung und Verhalten von Eigenschaften in Bezug auf die Linien und Bögen, die im Abschnitt "Geometry" bilden.
ms.openlocfilehash: ebfdb4dc7809f8883143fdda39f873a36f7bf896
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25389309"
---
# <a name="cell-element-geometry-section-visio-xml"></a>Zellenelement (Abschnitt "Geometry") ("Visio XML")

Definiert die Eigenschaften, die bestimmen, Formatierung und Verhalten von Eigenschaften in Bezug auf die Linien und Bögen, die im Abschnitt "Geometry" bilden.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |# .xml Master, Seite # .xml  <br/> |
   
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
|[Row-Element ("Geometry")](row-element-geometry-sectionvisio-xml.md) <br/> |[Geometry_Type](geometry_type-complextypevisio-xml.md) <br/> |Definiert die Eigenschaften, die bestimmen, Formatierung und Verhalten von Eigenschaften in Bezug auf die Linien und Bögen, die im Abschnitt "Geometry" bilden.  <br/> |
   
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
|NoFill  <br/> |Gibt an, ob ein Pfad gefüllt werden kann.  <br/> |[Zelle "NoFill" (Abschnitt "Geometry")](nofill-cell-geometry-section.md) <br/> |
|NoLine  <br/> |Legt fest, ob eine Linie um die Grenze des Pfads gezogen wird.  <br/> |[Zelle "NoLine" (Abschnitt "Geometry")](noline-cell-geometry-section.md) <br/> |
|NoQuickDrag  <br/> |Bestimmt, ob ein Shape ausgewählt oder gezogen werden, wenn der Benutzer den vom Abschnitt "Geometrie" definierten ausgefüllten Bereich klickt werden kann.  <br/> |[NoQuickDrag Cell (Geometry Section)](noquickdrag-cell-geometry-section.md) <br/> |
|NoShow  <br/> |Gibt an, ob ein Pfad auf dem Zeichenblatt angezeigt wird.  <br/> |[Zelle "NoShow" (Abschnitt "Geometry")](noshow-cell-geometry-section.md) <br/> |
|NoSnap  <br/> |Definiert, ob andere Shapes an einem Pfad einrasten.  <br/> |[Zelle "NoSnap" (Abschnitt "Geometry")](nosnap-cell-geometry-section.md) <br/> |
   

