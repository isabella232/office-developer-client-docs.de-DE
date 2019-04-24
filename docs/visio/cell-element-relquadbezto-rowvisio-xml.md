---
title: Cell-Element (RelQuadBezTo-Zeile) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 8b3aea70-a69f-a85e-83d8-c0fa2ee68836
description: Enthält die x-oder y-Koordinate des Endpunkts einer quadratischen Bézier-Kurve relativ zur Breite und Höhe des Shapes oder die x-oder y-Koordinaten des Steuerelements der Breite und Höhe der Kurven relativen Form.
ms.openlocfilehash: 986ed0a5f6e79f13b92f2ede54361916d9681e17
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339613"
---
# <a name="cell-element-relquadbezto-row-visio-xml"></a>Cell-Element (RelQuadBezTo-Zeile) (' Visio XML ')

Enthält die x-oder y-Koordinate des Endpunkts einer quadratischen Bézier-Kurve relativ zur Breite und Höhe des Shapes oder die x-oder y-Koordinaten des Steuerelements der Breite und Höhe der Kurven relativen Form.
  
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

### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element (Geometry)](row-element-geometry-sectionvisio-xml.md) <br/> |[RelQuadBezTo_Type](relquadbezto_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinate des Endpunkts einer quadratischen Bézier-Kurve relativ zur Breite und Höhe des Shapes oder die x-oder y-Koordinaten des Steuerelements der Breite und Höhe der Kurven relativen Form.  <br/> |
   
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
|X  <br/> |Die x-Koordinate des Endpunkts einer quadratischen Bézier-Kurve relativ zur Breite der Form.  <br/> |[Zeile "RelQuadBezTo" (Abschnitt "Geometry")](relquadbezto-row-geometry-section.md) <br/> |
|v  <br/> |Die y-Koordinate des Endpunkts einer quadratischen Bézier-Kurve relativ zur Höhe der Form.  <br/> |[Zeile "RelQuadBezTo" (Abschnitt "Geometry")](relquadbezto-row-geometry-section.md) <br/> |
|A  <br/> |Die x-Koordinate des Kontrollpunkts der Kurve relativ zur Breite der Form; ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten in der Mitte zwischen dem Anfangs-und Endscheitel des Bogens.  <br/> |[Zeile "RelQuadBezTo" (Abschnitt "Geometry")](relquadbezto-row-geometry-section.md) <br/> |
|B  <br/> |Die y-Koordinate des Steuerpunkts eines Bogens relativ zur Höhe der Form.  <br/> |[Zeile "RelQuadBezTo" (Abschnitt "Geometry")](relquadbezto-row-geometry-section.md) <br/> |
   

