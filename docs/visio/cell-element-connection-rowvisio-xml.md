---
title: Cell-Element (Verbindungs Zeile) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Enthält die x-oder y-Koordinaten, die horizontale oder vertikale Richtung oder den Typ für einen einzelnen Verbindungspunkt in einem Shape.
ms.openlocfilehash: 367d7e462c1eb5b8fa6ee0572346f45ad621fa15
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356105"
---
# <a name="cell-element-connection-row-visio-xml"></a>Cell-Element (Verbindungs Zeile) (' Visio XML ')

Enthält die x-oder y-Koordinaten, die horizontale oder vertikale Richtung oder den Typ für einen einzelnen Verbindungspunkt in einem Shape.
  
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
|[Row-Element (Connection-Abschnitt)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Enthält die x-und y-Koordinaten, die horizontale und die vertikale Richtung und den Typ für einen einzelnen Verbindungspunkt in einem Shape.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Enthält die x-oder y-Koordinaten, die horizontale und die vertikale Richtung und den Typ für einen einzelnen Verbindungspunkt in einem Shape.  <br/> |
   
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
|AutoGen  <br/> |Gibt an, ob der Verbindungspunkt automatisch generiert wird. Der Wert 1 gibt an, dass der Verbindungspunkt automatisch generiert wird.  <br/> |Keine.  <br/> |
|DirX  <br/> |Bestimmt die x-Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts.  <br/> |[Zelle "DirX / A" (Abschnitt "Connection Points")](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Legt die Y-Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts fest.  <br/> |[Zelle "DirY / B" (Abschnitt "Connection Points")](diryb-cell-connection-points-section.md) <br/> |
|Eingabeaufforderung  <br/> |Dieses Attribut ist für die spätere Verwendung reserviert.  <br/> |Keine.  <br/> |
|Typ  <br/> |Legt den Verbindungspunkttyp fest.  <br/> |[Zelle "Type / C" (Abschnitt "Connection Points")](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Stellt die X-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.  <br/> |[Zelle "X" (Abschnitt "Connection Points")](x-cell-connection-points-section.md) <br/> |
|v  <br/> |Bestimmt die y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten.  <br/> |[Zelle "Y" (Abschnitt "Connection Points")](y-cell-connection-points-section.md) <br/> |
   

