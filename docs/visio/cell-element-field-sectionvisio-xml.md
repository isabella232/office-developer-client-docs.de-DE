---
title: Zellenelement (Abschnitt "Field") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.
ms.openlocfilehash: fffa97458b083edc7df33c4a559fa987f2bb1bf9
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59594895"
---
# <a name="cell-element-field-section-visio-xml"></a>Zellenelement (Abschnitt "Field") (Visio XML)

Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Row-Element (Abschnitt "Field")](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.  <br/> |
   
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
|Kalender  <br/> |Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date ist.  <br/> |[Zelle "Calendar" (Abschnitt "Text Fields")](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.  <br/> |[Zelle "Format" (Abschnitt "Text Fields")](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Gibt den Textfeldtyp an.  <br/> |[Zelle "ObjectKind" (Abschnitt "Text Fields")](objectkind-cell-text-fields-section.md) <br/> |
|Typ  <br/> |Gibt einen Datentyp für den Textfeldwert an.  <br/> |[Zelle "Type" (Abschnitt "Text Fields")](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Bestimmt die Kategorie eines eingefügten Felds. Diese Zelle wird von den Dialogfeldern Feld und Datenformat verwendet, um die Feld- und Kategorieinformationen zu bestimmen.  <br/> |[Zelle "UICategory" (Abschnitt "Text Fields")](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Bestimmt den Code eines eingefügten Felds. Diese Zelle wird von den Dialogfeldern Feld und Datenformat verwendet, um die Feld- und Kategorieinformationen zu bestimmen.  <br/> |[Zelle "UICode" (Abschnitt "Text Fields")](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Bestimmt das Format eines eingefügten Felds. Diese Zelle wird von den Dialogfeldern feld- und datenformat verwendet, um das Feld und  <br/> |[Zelle "UIFormat" (Abschnitt "Text Fields")](uiformat-cell-text-fields-section.md) <br/> |
|Wert  <br/> |Enthält die Funktion für ein Feld.  <br/> |[Zelle "Value" (Abschnitt "Text Fields")](value-cell-text-fields-section.md) <br/> |
   

