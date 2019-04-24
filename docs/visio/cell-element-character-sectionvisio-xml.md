---
title: Cell-Element (Abschnitt "Character") (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6b452591-cf0c-9e1c-c203-e9cf608d3cc3
description: Gibt ein Formatierungs Attribut für den Textlauf einer Form an, beispielsweise Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Basislinie oder Punktgröße.
ms.openlocfilehash: 6dd895b33353944d27abb0d64a6a6df64ca19896
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356084"
---
# <a name="cell-element-character-section-visio-xml"></a>Cell-Element (Abschnitt "Character") (' Visio XML ')

Gibt ein Formatierungs Attribut für den Textlauf einer Form an, beispielsweise Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Basislinie oder Punktgröße.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Document. XML, Master #. XML, Page #. XML  <br/> |
   
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
|[Zeilenelement (Abschnitt "Character")](row-element-character-sectionvisio-xml.md) <br/> |[CharacterRow_Type](characterrow_type-complextypevisio-xml.md) <br/> |Gibt ein Formatierungs Attribut für den Textlauf einer Form an, beispielsweise Schriftart, Farbe, Formatvorlage, Groß-/Kleinschreibung, Position relativ zur Basislinie oder Punktgröße.  <br/> |
   
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
|"AsianFont  <br/> |Enthält die Enumeration der Schriftart, die zum Formatieren eines Textlaufs mit asiatischen Zeichen verwendet wird.  <br/> |[Zelle "AsianFont" (Abschnitt "Character")](asianfont-cell-character-section.md) <br/> |
|Fall  <br/> |Bestimmt die Groß-/Kleinschreibung beim Ausführen eines Shape-Texts.  <br/> |[Zelle "Case" (Abschnitt "Character")](case-cell-character-section.md) <br/> |
|Farbe  <br/> |Bestimmt die Farbe, die für den Textlauf einer Form verwendet wird.  <br/> |[Zelle "Color" (Abschnitt "Character")](color-cell-character-section.md) <br/> |
|ColorTrans  <br/> |Bestimmt den Grad der Transparenz für die Text Lauf Farbe einer Ebene oder eines Shapes von 0 (vollständig deckend) bis 1 (vollständig transparent).  <br/> |Keine.  <br/> |
|"ComplexScriptFont  <br/> |Enthält die Nummer der Schriftart, die zum Formatieren eines Textlaufs mit komplexen Skript Zeichen verwendet wird.  <br/> |[Zelle "ComplexScriptFont" (Abschnitt "Character")](complexscriptfont-cell-character-section.md) <br/> |
|Zelle ComplexScriptSize  <br/> |Die Größe der Schriftart, die zum Formatieren eines Textlaufs mit komplexen Skript Zeichen verwendet wird.  <br/> |[Zelle "ComplexScriptSize" (Abschnitt "Character")](complexscriptsize-cell-character-section.md) <br/> |
|DoubleULine  <br/> |Bestimmt, ob der Range eines Textlaufs darunter doppelt unterstrichen wird.  <br/> |[Zelle "DoubleULine" (Abschnitt "Character")](doubleuline-cell-character-section.md) <br/> |
|DoubleStrikethrough  <br/> |Bestimmt, ob ein Textlauf Doppelt durchgestrichen formatiert ist.  <br/> |[Zelle "DoubleStrikethrough" (Abschnitt "Character")](doublestrikethrough-cell-character-section.md) <br/> |
|Font  <br/> |Stellt die Nummer der Schriftart dar, die zum Formatieren eines Textlaufs verwendet wird.  <br/> |[Zelle "Font" (Abschnitt "Character")](font-cell-character-section.md) <br/> |
|FontScale  <br/> |Gibt die Schriftbreite an.  <br/> |Keine.  <br/> |
|LangID  <br/> |Gibt die Sprache an, in der ein Textlauf eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Character")](langid-cell-character-section.md) <br/> |
|Letterspace  <br/> |Gibt den Abstand zwischen zwei oder mehr Zeichen an. Dieser Platz kann in 1/20 Pkt-Schritten hinzugefügt oder abgezogen werden.  <br/> |Keine.  <br/> |
|Overline  <br/> |Bestimmt, ob ein Textlauf über eine Zeile verfügt.  <br/> |[Zelle "Overline" (Abschnitt "Character")](overline-cell-character-section.md) <br/> |
|POS  <br/> |Bestimmt die Position des Text Laufs einer Form relativ zur Basislinie.  <br/> |[Zelle "Pos" (Abschnitt "Character")](pos-cell-character-section.md) <br/> |
|Größe  <br/> |Bestimmt die Größe eines Textlaufs im Text Block des Shapes.  <br/> |[Zelle "Size" (Abschnitt "Character")](size-cell-character-section.md) <br/> |
|Strikethru  <br/> |Bestimmt, ob ein Textlauf als durchgestrichen formatiert ist.  <br/> |[Zelle "Strikethru" (Abschnitt "Character")](strikethru-cell-character-section.md) <br/> |
|Format  <br/> |Zeigt die Zeichenformatierung an, die auf einen Range eines Textlaufs im Text Block der Form angewendet wird.  <br/> |[Zelle "Style" (Abschnitt "Character")](style-cell-character-section.md) <br/> |
   

