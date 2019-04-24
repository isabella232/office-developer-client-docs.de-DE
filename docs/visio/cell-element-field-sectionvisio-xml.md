---
title: Cell-Element (Field section) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.
ms.openlocfilehash: f6c3c724b210ad579012ff58b93333e28c2a8cf1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356238"
---
# <a name="cell-element-field-section-visio-xml"></a>Cell-Element (Field section) (' Visio XML ')

Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Master #. XML, Page #. XML  <br/> |
   
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
|[Row-Element (Field section)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.  <br/> |
   
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
|Kalender  <br/> |Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date lautet.  <br/> |[Zelle "Calendar" (Abschnitt "Text Fields")](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.  <br/> |[Zelle "Format" (Abschnitt "Text Fields")](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Gibt den Textfeldtyp an.  <br/> |[Zelle "ObjectKind" (Abschnitt "Text Fields")](objectkind-cell-text-fields-section.md) <br/> |
|Typ  <br/> |Gibt einen Datentyp für den Textfeldwert an.  <br/> |[Zelle "Type" (Abschnitt "Text Fields")](type-cell-text-fields-section.md) <br/> |
|UICategory  <br/> |Bestimmt die Kategorie eines eingefügten Felds. Diese Zelle wird von den Dialogfeldern Feld und Datenformat verwendet, um die Feld-und Kategorien Informationen zu bestimmen.  <br/> |[Zelle "UICategory" (Abschnitt "Text Fields")](uicategory-cell-text-fields-section.md) <br/> |
|UICode  <br/> |Bestimmt den Code eines eingefügten Felds. Diese Zelle wird von den Dialogfeldern Feld und Datenformat verwendet, um die Feld-und Kategorien Informationen zu bestimmen.  <br/> |[Zelle "UICode" (Abschnitt "Text Fields")](uicode-cell-text-fields-section.md) <br/> |
|UIFormat  <br/> |Bestimmt das Format eines eingefügten Felds. Diese Zelle wird von den Dialogfeldern Feld und Datenformat verwendet, um das Feld zu bestimmen und  <br/> |[Zelle "UIFormat" (Abschnitt "Text Fields")](uiformat-cell-text-fields-section.md) <br/> |
|Wert  <br/> |Enthält die Funktion für ein Feld.  <br/> |[Zelle "Value" (Abschnitt "Text Fields")](value-cell-text-fields-section.md) <br/> |
   

