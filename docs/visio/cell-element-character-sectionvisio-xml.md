---
title: Cell-Element (Character Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Gibt ein Formatierungsattribut für die Textlauf eines Shapes an, z. B. Schriftart, Farbe, Formatvorlage, Groß-/Klein- oder Position relativ zur Grundlinie oder Punktgröße.
ms.openlocfilehash: a7d67aa3c53f3a4c673151afc991202904f0557b
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540084"
---
# <a name="cell-element-character-section-visio-xml"></a>Cell-Element (Character Section) (Visio XML)

Gibt ein Formatierungsattribut für die Textlauf eines Shapes an, z. B. Schriftart, Farbe, Formatvorlage, Groß-/Klein- oder Position relativ zur Grundlinie oder Punktgröße.
  
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
|[Row-Element (Character Section)](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Gibt ein Formatierungsattribut für die Textlauf eines Shapes an, z. B. Schriftart, Farbe, Formatvorlage, Groß-/Klein- oder Position relativ zur Grundlinie oder Punktgröße.  <br/> |
   
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
|AsianFont  <br/> |Enthält die Aufzählung der Schriftart, die zum Formatieren einer Textlauf mit asiatischen Zeichen verwendet wird.  <br/> |[Zelle "AsianFont" (Abschnitt "Character")](asianfont-cell-character-section.md) <br/> |
|Fall  <br/> |Bestimmt den Fall der Textlauf eines Shapes.  <br/> |[Zelle "Case" (Abschnitt "Character")](case-cell-character-section.md) <br/> |
|Farbe  <br/> |Bestimmt die Farbe, die für die Textlauf eines Shapes verwendet wird.  <br/> |[Zelle "Color" (Abschnitt "Character")](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Bestimmt den Grad der Transparenz für die Textlauffarbe eines Layers oder Shapes von 0 (vollständig undurchsichtig) bis 1 (vollständig transparent).  <br/> |Keine.  <br/> |
|ComplexScriptFont  <br/> |Enthält die Nummer der Schriftart, die zum Formatieren einer Textlauf aus komplexen Skriptzeichen verwendet wird.  <br/> |[Zelle "ComplexScriptFont" (Abschnitt "Character")](complexscriptfont-cell-character-section.md) <br/> |
|ComplexScriptSize  <br/> |Die Schriftgröße, die zum Formatieren einer Textlauf aus komplexen Skriptzeichen verwendet wird.  <br/> |[Zelle "ComplexScriptSize" (Abschnitt "Character")](complexscriptsize-cell-character-section.md) <br/> |
|DblUnderline  <br/> |Bestimmt, ob der Bereich einer Textlauf-Ausführung eine doppelte Unterstreichung darunter hat.  <br/> |[Zelle "DoubleULine" (Abschnitt "Character")](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Bestimmt, ob eine Textdurchführung als doppelter Durchstrich formatiert ist.  <br/> |[Zelle "DoubleStrikethrough" (Abschnitt "Character")](doublestrikethrough-cell-character-section.md) <br/> |
|Schriftart  <br/> |Represents the number of the font used to format a text run.  <br/> |[Zelle "Font" (Abschnitt "Character")](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Gibt die Schriftbreite an.  <br/> |Keine.  <br/> |
|LangID  <br/> |Gibt die Sprache an, in der ein Textlauf eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Character")](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Gibt den Abstand zwischen zwei oder mehr Zeichen an. Dieser Platz kann in 1/20 Pkt-Schritten hinzugefügt oder abgezogen werden.  <br/> |Keine.  <br/> |
|Überline  <br/> |Bestimmt, ob eine Textlaufzeile eine Zeile darüber hat.  <br/> |[Zelle "Overline" (Abschnitt "Character")](overline-cell-character-section.md) <br/> |
|Pos  <br/> |Bestimmt die Position des Textlaufs eines Shapes relativ zur Grundlinie.  <br/> |[Zelle "Pos" (Abschnitt "Character")](pos-cell-character-section.md) <br/> |
|Size  <br/> |Bestimmt die Größe eines Textes, der im Textblock des Shapes ausgeführt wird.  <br/> |[Zelle "Size" (Abschnitt "Character")](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Bestimmt, ob eine Textdurchführung als durchgestrichen formatiert ist.  <br/> |[Zelle "Strikethru" (Abschnitt "Character")](strikethru-cell-character-section.md) <br/> |
|Format  <br/> |Zeigt die Zeichenformatierung an, die auf einen Textbereich angewendet wird, der im Textblock des Shapes ausgeführt wird.  <br/> |[Zelle "Style" (Abschnitt "Character")](style-cell-character-section.md) <br/> |
   

