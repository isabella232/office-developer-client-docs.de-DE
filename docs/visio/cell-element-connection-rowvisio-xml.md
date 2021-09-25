---
title: Zellenelement (Connection Row) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Enthält die X- oder Y-Koordinaten, die horizontale oder vertikale Richtung oder den Typ für einen einzelnen Verbindungspunkt in einem Shape.
ms.openlocfilehash: 645272faca5afe580314039cfc66a88e66f0c359
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608529"
---
# <a name="cell-element-connection-row-visio-xml"></a>Zellenelement (Connection Row) (Visio XML)

Enthält die X- oder Y-Koordinaten, die horizontale oder vertikale Richtung oder den Typ für einen einzelnen Verbindungspunkt in einem Shape.
  
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
|[Row-Element (Abschnitt "Connection")](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Enthält die X- und Y-Koordinaten, die horizontale und vertikale Richtung sowie den Typ für einen einzelnen Verbindungspunkt in einem Shape.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Enthält die X- oder Y-Koordinaten, die horizontale und vertikale Richtung sowie den Typ für einen einzelnen Verbindungspunkt in einem Shape.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehlermeldungszeichenfolge); Der Wert des **V-Attributs** ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungszeichenfolge.  <br/> |
|F  <br/> |xsd:string  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  '(some formula)', wenn die Formel lokal vorhanden ist  <br/>  `No Formula` wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh` wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |xsd:string  <br/> |Erforderlich  <br/> |Stellt den Namen der Zelle ShapeSheet dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie unten im Abschnitt "Hinweise".  <br/> |
|U  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar. Der Standardwert ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **N-Attribut** dieses **Cell-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle finden Sie Informationen zu den Werten des **N-Attributs,** die für dieses **Cell-Element** zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Autogen  <br/> |Gibt an, ob der Verbindungspunkt automatisch generiert wird. Der Wert 1 gibt an, dass der Verbindungspunkt automatisch generiert wird.  <br/> |Keine  <br/> |
|DirX  <br/> |Bestimmt die x-Komponente für den erforderlichen Ausrichtungsvektor eines übereinstimmenden Verbindungspunkts.  <br/> |[Zelle "DirX / A" (Abschnitt "Connection Points")](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Legt die Y-Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts fest.  <br/> |[Zelle "DirY / B" (Abschnitt "Connection Points")](diryb-cell-connection-points-section.md) <br/> |
|Eingabeaufforderung  <br/> |Dieses Attribut ist für die zukünftige Verwendung reserviert.  <br/> |Keine  <br/> |
|Typ  <br/> |Legt den Verbindungspunkttyp fest.  <br/> |[Zelle "Type / C" (Abschnitt "Connection Points")](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Stellt die X-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.  <br/> |[Zelle "X" (Abschnitt "Connection Points")](x-cell-connection-points-section.md) <br/> |
|J  <br/> |Bestimmt die Y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten.  <br/> |[Zelle "Y" (Abschnitt "Connection Points")](y-cell-connection-points-section.md) <br/> |
   

