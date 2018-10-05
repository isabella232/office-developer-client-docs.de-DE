---
title: Zellenelement (Verbindung Zeile) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7cafaa31-c56b-ebb0-3bfb-c339cc93038e
description: Enthält die x- oder y-Koordinaten, horizontaler oder vertikaler Richtung oder Typ für einen einzelnen Verbindungspunkt auf einem Shape.
ms.openlocfilehash: 367d7e462c1eb5b8fa6ee0572346f45ad621fa15
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388959"
---
# <a name="cell-element-connection-row-visio-xml"></a>Zellenelement (Verbindung Zeile) ("Visio XML")

Enthält die x- oder y-Koordinaten, horizontaler oder vertikaler Richtung oder Typ für einen einzelnen Verbindungspunkt auf einem Shape.
  
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
|[Zeilenelement (Verbindungszeile)](row-element-connection-sectionvisio-xml.md) <br/> |[ConnectionRow_Type](connectionrow_type-complextypevisio-xml.md) <br/> |Enthält die x- und y-Koordinaten, die horizontalen und vertikalen Richtung und den Typ für einen einzelnen Verbindungspunkt auf einem Shape.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Enthält die x- oder y-Koordinaten, die horizontalen und vertikalen Richtung und den Typ für einen einzelnen Verbindungspunkt auf einem Shape.  <br/> |
   
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
|AutoGen  <br/> |Gibt an, ob die Verbindung automatisch generiert wird. Der Wert 1 gibt an, dass der Verbindungspunkt automatisch generiert wird.  <br/> |Keine.  <br/> |
|DirX  <br/> |Legt die X-Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts.  <br/> |[Zelle "DirX / A" (Abschnitt "Connection Points")](dirxa-cell-connection-points-section.md) <br/> |
|DirY  <br/> |Die y-Komponente für den erforderlichen Ausrichtungsvektor eines passenden Verbindungspunkts bestimmt.  <br/> |[Zelle "DirY / B" (Abschnitt "Connection Points")](diryb-cell-connection-points-section.md) <br/> |
|Eingabeaufforderung  <br/> |Dieses Attribut ist für die zukünftige Verwendung reserviert.  <br/> |Keine.  <br/> |
|Typ  <br/> |Legt den Verbindungspunkttyp fest.  <br/> |[Zelle "Type / C" (Abschnitt "Connection Points")](typec-cell-connection-points-section.md) <br/> |
|X  <br/> |Stellt die X-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.  <br/> |[Zelle "X" (Abschnitt "Connection Points")](x-cell-connection-points-section.md) <br/> |
|v  <br/> |Bestimmt die y-Koordinate für einen Verbindungspunkt in lokalen Koordinaten dar.  <br/> |[Zelle "Y" (Abschnitt "Connection Points")](y-cell-connection-points-section.md) <br/> |
   

