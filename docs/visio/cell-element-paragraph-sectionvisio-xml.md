---
title: Zellenelement (Abschnitt "Paragraph") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: de0d3aac-1a0f-1bdf-da94-e6699a55d08e
description: Gibt ein Absatzformat-Attribut für den Text des Shapes, wie etwa Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen an.
ms.openlocfilehash: 38309d3d1158b02084af6686c483547b28b8995f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796595"
---
# <a name="cell-element-paragraph-section-visio-xml"></a>Zellenelement (Abschnitt "Paragraph") ("Visio XML")

Gibt ein Absatzformat-Attribut für den Text des Shapes, wie etwa Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.XML, master # .xml, Seite # .xml  <br/> |
   
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
|[Row-Element (Abschnitt "Paragraph")](row-element-paragraph-sectionvisio-xml.md) <br/> |[ParagraphRow_Type](paragraphrow_type-complextypevisio-xml.md) <br/> |Gibt ein Absatzformat-Attribut für den Text des Shapes, wie etwa Einzüge, Zeilenabstand, Aufzählungszeichen oder horizontale Ausrichtung von Absätzen an.  <br/> |
   
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
|Aufzählungszeichen  <br/> |Bestimmt das Aufzählungszeichenformat.  <br/> |[Zelle "Bullet" (Abschnitt "Paragraph")](bullet-cell-paragraph-section.md) <br/> |
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
   

