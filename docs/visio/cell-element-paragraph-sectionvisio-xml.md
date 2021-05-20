---
title: Cell-Element (Paragraph Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: Gibt ein Absatzformatierungsattribut für den Text des Shapes an, z. B. Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen.
ms.openlocfilehash: fbb837b96d40f412ddefdf1fac9da0d31a709e39
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539481"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Cell-Element (Paragraph Section) (Visio XML)

Gibt ein Absatzformatierungsattribut für den Text des Shapes an, z. B. Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, Master#.xml, Seite#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Cell" type="Cell_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row-Element (Abschnitt "Paragraph")](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |Gibt ein Absatzformatierungsattribut für den Text des Shapes an, z. B. Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehlermeldungszeichenfolge); Der Wert  des V-Attributs ist der letzte gültige Wert.  <br/> |Eine Fehlermeldungszeichenfolge.  <br/> |
|F  <br/> |xsd:string  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  '(einige Formel)' wenn die Formel lokal vorhanden ist  <br/>  `No Formula` wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh` wenn die Formel geerbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |xsd:string  <br/> |erforderlich  <br/> |Stellt den Namen der Zelle ShapeSheet dar.  <br/> |Der Name der Zelle ShapeSheet.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise".  <br/> |
|U  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar Die Standardeinstellung ist DL.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |xsd:string  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der Zelle ShapeSheet.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N-Attribut** dieses **Cell-Elements** muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle finden Sie  Informationen zu den Werten des N-Attributs, die für dieses **Cell-Element zulässig** sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|Bullet  <br/> |Bestimmt das Aufzählungszeichenformat.  <br/> |[Zelle "Bullet" (Abschnitt "Paragraph")](bullet-cell-paragraph-section.md) <br/> |
|BulletFont  <br/> |Stellt die Nummer der Schriftart dar, die zum Formatieren von Text verwendet wird, wenn eine benutzerdefinierte Aufzählungszeichen-Zeichenfolge angegeben ist und der Wert in der Zelle Bullet ungleich Null ist.  <br/> |[Zelle "BulletFont" (Abschnitt "Paragraph")](bulletfont-cell-paragraph-section.md) <br/> |
|BulletFontSize  <br/> |Gibt die Größe eines Aufzählungszeichens an.  <br/> |[Zelle "BulletSize" (Abschnitt "Paragraph")](bulletsize-cell-paragraph-section.md) <br/> |
|BulletStr  <br/> |Ermöglicht das Erstellen von benutzerdefinierten Aufzählungszeichen.  <br/> |[Zelle "BulletString" (Abschnitt "Paragraph")](bulletstring-cell-paragraph-section.md) <br/> |
|Flags  <br/> |Gibt an, ob die Textrichtung von links nach rechts oder von rechts nach links verläuft.  <br/> |[Zelle "Flags" (Abschnitt "Paragraph")](flags-cell-paragraph-section.md) <br/> |
|HorzAlign  <br/> |Definiert die horizontale Ausrichtung des Texts im Textblock des Shapes.  <br/> |[Zelle "HAlign" (Abschnitt "Paragraph")](halign-cell-paragraph-section.md) <br/> |
|IndFirst  <br/> |Stellt den Abstand dar, den die erste Zeile jedes einzelnen Absatzes im Textblock des Shapes vom linken Einzug des Absatzes eingezogen ist. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der Einzug der ersten Zeile gleich.  <br/> |[Zelle "IndFirst" (Abschnitt "Paragraph")](indfirst-cell-paragraph-section.md) <br/> |
|IndLeft  <br/> |Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom linken Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der linke Einzug gleich.  <br/> |[Zelle "IndLeft" (Abschnitt "Paragraph")](indleft-cell-paragraph-section.md) <br/> |
|IndRight  <br/> |Stellt den Abstand dar, den sämtliche Textzeilen in einem Absatz vom rechten Rand des Textblocks eingezogen sind. Dieser Wert ist unabhängig vom Zeichnungsmaßstab. Wenn die Zeichnung skaliert ist, bleibt der rechte Einzug gleich.  <br/> |[Zelle "IndRight" (Abschnitt "Paragraph")](indright-cell-paragraph-section.md) <br/> |
|SpAfter  <br/> |Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, nach jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den letzten Absatz in einem Textblock handelt (die Zelle BottomMargin).  <br/> |[Zelle "SpAfter" (Abschnitt "Paragraph")](spafter-cell-paragraph-section.md) <br/> |
|SpBefore  <br/> |Legt den Platz fest, der zusätzlich zum Platz, der in der Zelle SpLine angegeben wurde, vor jedem Absatz im Textblock des Shapes eingefügt wird, wenn es sich um den ersten Absatz in einem Textblock handelt (die Zelle TopMargin).  <br/> |[Zelle "SpBefore" (Abschnitt "Paragraph")](spbefore-cell-paragraph-section.md) <br/> |
|SpLine  <br/> |Legt den Abstand zwischen einer Textzeile und der nächsten in Prozent fest. 100 % ist dabei die Höhe einer Textzeile.  <br/> |[Zelle "SpLine" (Abschnitt "Paragraph")](spline-cell-paragraph-section.md) <br/> |
|TextPosAfterBullet  <br/> |Stellt den Abstand zwischen der ersten Zeile des Absatzes und dem Aufzählungszeichen dar.  <br/> |[Zelle "TextPosAfterBullet" (Abschnitt "Paragraph")](textposafterbullet-cell-paragraph-section.md) <br/> |
   

