---
title: Zellenelement (Abschnitt "Character") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Gibt eine Formatierung-Attribut für ein Shape-Text ausführen, wie z. B. Schriftart, Farbe, formatieren, case, relativ zur Grundlinie positionieren oder Schriftgrad.
ms.openlocfilehash: 0d0725ec6ff19104d95780dcfbb3fff9715cbe92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796575"
---
# <a name="cell-element-character-section-visio-xml"></a>Zellenelement (Abschnitt "Character") ("Visio XML")

Gibt eine Formatierung-Attribut für ein Shape-Text ausführen, wie z. B. Schriftart, Farbe, formatieren, case, relativ zur Grundlinie positionieren oder Schriftgrad.
  
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
|[Zeilenelement (Zeichenabschnitt)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Gibt eine Formatierung-Attribut für ein Shape-Text ausführen, wie z. B. Schriftart, Farbe, formatieren, case, relativ zur Grundlinie positionieren oder Schriftgrad.  <br/> |
   
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
   
## <a name="remarks"></a>Bemerkungen

Das **N** -Attribut dieses Elements **Zelle** muss eine der eine begrenzte Auswahl von Werten sein, die ShapeSheet-Zellen entsprechen. Finden Sie in der Tabelle unten, um die Werte der **N** -Attribut zu bestimmen, die für diese **Zelle** Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|AsianFont  <br/> |Die Enumeration der Schriftgrad zum Formatieren eines Textlaufs mit asiatischen Zeichen enthält.  <br/> |[Zelle "AsianFont" (Abschnitt "Character")](asianfont-cell-character-section.md) <br/> |
|Case  <br/> |Bestimmt die Groß-/Kleinschreibung eines Shape Texts ausführen.  <br/> |[Zelle "Case" (Abschnitt "Character")](case-cell-character-section.md) <br/> |
|Farbe  <br/> |Legt die Farbe für den Text eines Shapes ausführen.  <br/> |[Zelle "Color" (Abschnitt "Character")](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Bestimmt den Grad der Transparenz für eine Ebene oder Text des Shapes, die Farbe von 0 (vollständig undurchsichtig) und 1 (vollständig transparent) ausführen.  <br/> |Keine.  <br/> |
|ComplexScriptFont  <br/> |Enthält die Nummer der Schriftart zum Formatieren eines komplexen Schriftzeichen zusammengesetzten Textlaufs verwendet.  <br/> |[Zelle "ComplexScriptFont" (Abschnitt "Character")](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Der Schriftgrad zum Formatieren von einer Text ausführen zusammengesetzten komplexen Schriftzeichen.  <br/> |[Zelle "ComplexScriptSize" (Abschnitt "Character")](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Bestimmt, ob der Bereich eines doppelte unterstrichen.  <br/> |[Zelle "DoubleULine" (Abschnitt "Character")](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Bestimmt, ob eine ausführen Text doppelt durchgestrichen formatiert ist.  <br/> |[Zelle "DoubleStrikethrough" (Abschnitt "Character")](doublestrikethrough-cell-character-section.md) <br/> |
|Font  <br/> |Stellt die Anzahl der Schriftart verwendet, um einen Textlauf formatieren.  <br/> |[Zelle "Font" (Abschnitt "Character")](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Gibt die Schriftartbreite.  <br/> |Keine.  <br/> |
|LangID  <br/> |Gibt die Sprache, in der ein Textlauf eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Character")](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Gibt den Abstand zwischen zwei oder mehr Zeichen. Speicherplatz kann hinzugefügt oder in Schritten von jeweils 1/20 Punkt subtrahiert werden.  <br/> |Keine.  <br/> |
|Overline  <br/> |Bestimmt, ob ein Textlauf überstrichen.  <br/> |[Zelle "Overline" (Abschnitt "Character")](overline-cell-character-section.md) <br/> |
|POS  <br/> |Bestimmt die Position des ein Shape-Texts relativ zur Grundlinie ausführen.  <br/> |[Zelle "Pos" (Abschnitt "Character")](pos-cell-character-section.md) <br/> |
|Größe  <br/> |Bestimmt die Größe des eines Textlaufs im Textblock des Shapes.  <br/> |[Zelle "Size" (Abschnitt "Character")](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Bestimmt, ob eine ausführen Text als durchgestrichen formatiert ist.  <br/> |[Zelle "Strikethru" (Abschnitt "Character")](strikethru-cell-character-section.md) <br/> |
|Formatvorlage  <br/> |Zeigt die zeichenformatierung für einen Textbereich ein übernommen ausführen im Textblock des Shapes.  <br/> |[Zelle "Style" (Abschnitt "Character")](style-cell-character-section.md) <br/> |
   

