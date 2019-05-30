---
title: Cell-Element (Character section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Gibt ein Formatierungs Attribut für die Textausführung eines Shapes an, beispielsweise Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Grundlinie oder Punktgröße.
ms.openlocfilehash: a7d67aa3c53f3a4c673151afc991202904f0557b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540084"
---
# <a name="cell-element-character-section-visio-xml"></a>Cell-Element (Character section) (Visio XML)

Gibt ein Formatierungs Attribut für die Textausführung eines Shapes an, beispielsweise Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Grundlinie oder Punktgröße.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML, Master #. XML, Seite #. XML  <br/> |
   
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
|[Row-Element (Abschnitt "Character")](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Gibt ein Formatierungs Attribut für die Textausführung eines Shapes an, beispielsweise Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Grundlinie oder Punktgröße.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|E  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt an, dass die Formel zu einem Fehler ausgewertet wird. Der Wert von **E** ist der aktuelle Wert (eine Fehler Meldungszeichenfolge); der Wert des **V** -Attributs ist der letzte gültige Wert.  <br/> |Eine Fehler Meldungszeichenfolge.  <br/> |
|F  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> | Stellt die Formel des Elements dar. Dieses Attribut kann eine der folgenden Zeichenfolgen enthalten:  <br/>  "(eine Formel)", wenn die Formel lokal vorhanden ist  <br/>  `No Formula`Wenn die Formel lokal gelöscht oder blockiert wird  <br/>  `Inh`, wenn die Formel vererbt wird.  <br/> |Eine Formel.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> |Stellt den Namen der ShapeSheet-Zelle dar.  <br/> |Der Name der ShapeSheet-Zelle.  <br/> Weitere Informationen finden Sie im Abschnitt "Hinweise" weiter unten.  <br/> |
|U  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt eine Maßeinheit dar, bei der es sich bei der Standardeinstellung um DL handelt.  <br/> |Die Einheiten der Zelle.  <br/> |
|V  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Stellt den Wert der Zelle dar.  <br/> |Der Wert der ShapeSheet-Zelle.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **N** -Attribut dieses **Cell** -Elements muss einer der begrenzten Werte sein, die ShapeSheet-Zellen entsprechen. In der folgenden Tabelle können Sie die Werte des **N** -Attributs bestimmen, die für dieses **Zellen** Element zulässig sind. 
  
|**Wert**|**Beschreibung**|**Weitere Informationen**|
|:-----|:-----|:-----|
|"AsianFont  <br/> |Enthält die Aufzählung der Schriftart, die zum Formatieren eines Textlaufs mit asiatischen Zeichen verwendet wird.  <br/> |[Zelle "AsianFont" (Abschnitt "Character")](asianfont-cell-character-section.md) <br/> |
|Fall  <br/> |Bestimmt die Groß-/Kleinschreibung der Textausführung eines Shapes.  <br/> |[Zelle "Case" (Abschnitt "Character")](case-cell-character-section.md) <br/> |
|Farbe  <br/> |Bestimmt die Farbe, die für die Textausführung eines Shapes verwendet wird.  <br/> |[Zelle "Color" (Abschnitt "Character")](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Legt den Grad der Transparenz für die Text Lauf Farbe einer Ebene oder Form fest (von 0 (vollständig deckend) auf 1 (vollständig transparent).  <br/> |Keine.  <br/> |
|"ComplexScriptFont  <br/> |Enthält die Nummer der Schriftart, die zum Formatieren eines Textlaufs verwendet wird, der aus komplexen Skript Zeichen besteht.  <br/> |[Zelle "ComplexScriptFont" (Abschnitt "Character")](complexscriptfont-cell-character-section.md) <br/> |
|Zelle ComplexScriptSize  <br/> |Die Größe der Schriftart, die zum Formatieren eines Textlaufs verwendet wird, der aus komplexen Skript Zeichen besteht.  <br/> |[Zelle "ComplexScriptSize" (Abschnitt "Character")](complexscriptsize-cell-character-section.md) <br/> |
|DoubleULine  <br/> |Bestimmt, ob der Bereich eines Textlaufs darunter doppelt unterstrichen ist.  <br/> |[Zelle "DoubleULine" (Abschnitt "Character")](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikeThrough  <br/> |Bestimmt, ob ein Textlauf als doppelt durchgestrichen formatiert ist.  <br/> |[Zelle "DoubleStrikethrough" (Abschnitt "Character")](doublestrikethrough-cell-character-section.md) <br/> |
|Font  <br/> |Stellt die Nummer der Schriftart dar, die zum Formatieren eines Textlaufs verwendet wird.  <br/> |[Zelle "Font" (Abschnitt "Character")](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Gibt die Schriftbreite an.  <br/> |Keine.  <br/> |
|LangID  <br/> |Gibt die Sprache an, in der ein Text Lauf eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Character")](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Gibt die Größe des Speicherplatzes zwischen zwei oder mehr Zeichen an. Dieser Platz kann in 1/20 Pkt-Schritten hinzugefügt oder abgezogen werden.  <br/> |Keine.  <br/> |
|Overline  <br/> |Bestimmt, ob ein Textlauf eine Zeile über dem Text hat.  <br/> |[Zelle "Overline" (Abschnitt "Character")](overline-cell-character-section.md) <br/> |
|POS  <br/> |Bestimmt die Position des Text Laufs einer Form relativ zur Basislinie.  <br/> |[Zelle "Pos" (Abschnitt "Character")](pos-cell-character-section.md) <br/> |
|Größe  <br/> |Bestimmt die Größe eines Texts, der im TextBlock des Shapes ausgeführt wird.  <br/> |[Zelle "Size" (Abschnitt "Character")](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Bestimmt, ob ein Textlauf als durchgestrichen formatiert ist.  <br/> |[Zelle "Strikethru" (Abschnitt "Character")](strikethru-cell-character-section.md) <br/> |
|Format  <br/> |Zeigt die Zeichenformatierung an, die auf einen Textbereich angewendet wird, der im TextBlock des Shapes ausgeführt wird.  <br/> |[Zelle "Style" (Abschnitt "Character")](style-cell-character-section.md) <br/> |
   

