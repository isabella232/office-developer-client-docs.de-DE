---
title: Zellenelement (Abschnitt "Character") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Gibt ein Formatierungsattribut für den Textlauf eines Shapes an, z. B. Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Grundlinie oder Punktgröße.
ms.openlocfilehash: 1dea1b40afad75f59eb171b02dd102a9bcc97fb7
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59608543"
---
# <a name="cell-element-character-section-visio-xml"></a>Zellenelement (Abschnitt "Character") (Visio XML)

Gibt ein Formatierungsattribut für den Textlauf eines Shapes an, z. B. Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Grundlinie oder Punktgröße.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, master#.xml, page#.xml  <br/> |
   
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
|[Zeilenelement (Abschnitt "Character")](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Gibt ein Formatierungsattribut für den Textlauf eines Shapes an, z. B. Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Grundlinie oder Punktgröße.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[RefBy](refby-element-cell_type-complextypevisio-xml.md) <br/> |[RefBy_Type](refby_type-complextypevisio-xml.md) <br/> |Gibt einen Verweis auf ein Zeichenblatt an.  <br/> |
   
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
|AsianFont  <br/> |Enthält die Aufzählung der Schriftart, die zum Formatieren eines Textlaufs mit asiatischen Zeichen verwendet wird.  <br/> |[Zelle "AsianFont" (Abschnitt "Character")](asianfont-cell-character-section.md) <br/> |
|Fall  <br/> |Bestimmt die Groß-/Kleinschreibung des Textlaufs eines Shapes.  <br/> |[Zelle "Case" (Abschnitt "Character")](case-cell-character-section.md) <br/> |
|Farbe  <br/> |Bestimmt die Farbe, die für die Textausführung eines Shapes verwendet wird.  <br/> |[Zelle "Color" (Abschnitt "Character")](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Bestimmt den Grad der Transparenz für die Textlauffarbe einer Ebene oder Form von 0 (vollständig undurchsichtig) bis 1 (vollständig transparent).  <br/> |Keine  <br/> |
|ComplexScriptFont  <br/> |Enthält die Nummer der Schriftart, die zum Formatieren eines Textlaufs verwendet wird, der aus komplexen Skriptzeichen besteht.  <br/> |[Zelle "ComplexScriptFont" (Abschnitt "Character")](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Die Größe der Schriftart, die zum Formatieren eines Textlaufs verwendet wird, der aus komplexen Skriptzeichen besteht.  <br/> |[Zelle "ComplexScriptSize" (Abschnitt "Character")](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Bestimmt, ob der Bereich eines Textlaufs eine doppelte Unterstreichung darunter aufweist.  <br/> |[Zelle "DoubleULine" (Abschnitt "Character")](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Bestimmt, ob eine Textausführung als doppelt durchgestrichen formatiert ist.  <br/> |[Zelle "DoubleStrikethrough" (Abschnitt "Character")](doublestrikethrough-cell-character-section.md) <br/> |
|Font  <br/> |Stellt die Nummer der Schriftart dar, die zum Formatieren eines Textlaufs verwendet wird.  <br/> |[Zelle "Font" (Abschnitt "Character")](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Gibt die Schriftbreite an.  <br/> |Keine  <br/> |
|Langid  <br/> |Gibt die Sprache an, in der eine Textausführung eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Character")](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Gibt den Abstand zwischen zwei oder mehr Zeichen an. Dieser Platz kann in 1/20 Pkt-Schritten hinzugefügt oder abgezogen werden.  <br/> |Keine  <br/> |
|Overline  <br/> |Bestimmt, ob ein Textlauf eine Zeile darüber hat.  <br/> |[Zelle "Overline" (Abschnitt "Character")](overline-cell-character-section.md) <br/> |
|Pos  <br/> |Bestimmt die Position des Textlaufs eines Shapes relativ zur Grundlinie.  <br/> |[Zelle "Pos" (Abschnitt "Character")](pos-cell-character-section.md) <br/> |
|Size  <br/> |Bestimmt die Größe eines Textlaufs im Textblock des Shapes.  <br/> |[Zelle "Size" (Abschnitt "Character")](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Bestimmt, ob eine Textausführung durchgestrichen formatiert ist.  <br/> |[Zelle "Strikethru" (Abschnitt "Character")](strikethru-cell-character-section.md) <br/> |
|Format  <br/> |Zeigt die Zeichenformatierung an, die auf einen Bereich eines Textlaufs im Textblock des Shapes angewendet wird.  <br/> |[Zelle "Style" (Abschnitt "Character")](style-cell-character-section.md) <br/> |
   

