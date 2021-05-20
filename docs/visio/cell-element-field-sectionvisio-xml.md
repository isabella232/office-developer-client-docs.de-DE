---
title: Cell-Element (Field Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1a51a5ca-6b68-d2d8-befb-2b1d9cda1b8e
description: Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.
ms.openlocfilehash: b3bae89d20a4defed591e95ce0155f70d806e6f2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540056"
---
# <a name="cell-element-field-section-visio-xml"></a>Cell-Element (Field Section) (Visio XML)

Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |master#.xml, page#.xml  <br/> |
   
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
|[Row-Element (Field Section)](row-element-field-sectionvisio-xml.md) <br/> |[FieldRow_Type](fieldrow_type-complextypevisio-xml.md) <br/> |Zeigt Funktionen und Formeln an, die über das Dialogfeld Feld in den Text des Shapes eingefügt werden.  <br/> |
   
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
|Kalender  <br/> |Bestimmt den Kalender, der für ein Textfeld verwendet wird, wenn der Datentyp Date ist.  <br/> |[Zelle "Calendar" (Abschnitt "Text Fields")](calendar-cell-text-fields-section.md) <br/> |
|Format  <br/> |Legt die Formatierung eines Textfelds in Form einer Zeichenfolge, einer Zahl, eines Datums oder einer Uhrzeit, einer Zeitdauer oder einer Währung fest.  <br/> |[Zelle "Format" (Abschnitt "Text Fields")](format-cell-text-fields-section.md) <br/> |
|ObjectKind  <br/> |Gibt den Textfeldtyp an.  <br/> |[Zelle "ObjectKind" (Abschnitt "Text Fields")](objectkind-cell-text-fields-section.md) <br/> |
|Typ  <br/> |Gibt einen Datentyp für den Textfeldwert an.  <br/> |[Zelle "Type" (Abschnitt "Text Fields")](type-cell-text-fields-section.md) <br/> |
|UICat  <br/> |Bestimmt die Kategorie eines eingefügten Felds. Diese Zelle wird von den Dialogfelder Feld- und Datenformat verwendet, um die Feld- und Kategorieinformationen zu bestimmen.  <br/> |[Zelle "UICategory" (Abschnitt "Text Fields")](uicategory-cell-text-fields-section.md) <br/> |
|UICod  <br/> |Bestimmt den Code eines eingefügten Felds. Diese Zelle wird von den Dialogfelder Feld- und Datenformat verwendet, um die Feld- und Kategorieinformationen zu bestimmen.  <br/> |[Zelle "UICode" (Abschnitt "Text Fields")](uicode-cell-text-fields-section.md) <br/> |
|UIFmt  <br/> |Bestimmt das Format eines eingefügten Felds. Diese Zelle wird von den Dialogfelder Feld- und Datenformat verwendet, um das Feld und  <br/> |[Zelle "UIFormat" (Abschnitt "Text Fields")](uiformat-cell-text-fields-section.md) <br/> |
|Wert  <br/> |Enthält die Funktion für ein Feld.  <br/> |[Zelle "Value" (Abschnitt "Text Fields")](value-cell-text-fields-section.md) <br/> |
   

