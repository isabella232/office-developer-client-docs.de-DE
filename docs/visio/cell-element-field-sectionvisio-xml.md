---
title: Zellenelement (Feldabschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.
ms.openlocfilehash: 94c9807984ef0e327c1cc9f8449d1ea065fdd717
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796576"
---
# <a name="cell-element-field-section-visio-xml"></a>Zellenelement (Feldabschnitt) ("Visio XML")

Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[Zeilenelement (Feldabschnitt)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.  <br/> |
   
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
|Kalender  <br/> |Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date lautet.  <br/> |[Zelle "Calendar" (Abschnitt "Text Fields")](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.  <br/> |[Zelle "Format" (Abschnitt "Text Fields")](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Gibt den Textfeldtyp an.  <br/> |[Zelle "ObjectKind" (Abschnitt "Text Fields")](objectkind-cell-text-fields-section.md) <br/> |
|Typ  <br/> |Gibt einen Datentyp für den Textfeldwert an.  <br/> |[Zelle "Type" (Abschnitt "Text Fields")](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Bestimmt die Kategorie eines eingefügten Felds. Diese Zelle wird von Feld- und Format Dialogfelder verwendet, um die Informationen dar und die Kategorie zu bestimmen.  <br/> |[Zelle "UICategory" (Abschnitt "Text Fields")](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Bestimmt den Code eines eingefügten Felds. Diese Zelle wird von Feld- und Format Dialogfelder verwendet, um die Informationen dar und die Kategorie zu bestimmen.  <br/> |[Zelle "UICode" (Abschnitt "Text Fields")](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Bestimmt das Format eines eingefügten Felds. Diese Zelle wird durch die Format-Dialogfelder Feld- und das Feld bestimmt und  <br/> |[Zelle "UIFormat" (Abschnitt "Text Fields")](uiformat-cell-text-fields-section.md) <br/> |
|Wert  <br/> |Enthält die Funktion für ein Feld.  <br/> |[Zelle "Value" (Abschnitt "Text Fields")](value-cell-text-fields-section.md) <br/> |
   

