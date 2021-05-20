---
title: Cell-Element (Abschnitt "Shape Data") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Gibt eine Eigenschaft der Shapedaten an.
ms.openlocfilehash: 3a6238f19f27d001d3c9eebcbcec720822a0ed40
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539376"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Cell-Element (Abschnitt "Shape Data") (Visio XML)

Gibt eine Eigenschaft der Shapedaten an.
  
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
|[Row-Element (Abschnitt "Shape Data")](row-element-shape-data-sectionvisio-xml.md) <br/> |[Shape-Data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |Gibt einen Shapedateneintrag zum Zuordnen von Daten zu einer Form an.  <br/> |
   
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
|Kalender  <br/> |Gibt den Typ des Kalenders an, der verwendet wird, wenn ein Shape-Datenelement vom Typ Datum ist.  <br/> |[Zelle "Calendar" (Abschnitt "Shape Data")](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Gibt an, ob die Zeile Shape Data derzeit mit einem Feld in einem Datendatensatz verknüpft ist.  <br/> ||
|Format  <br/> |Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.  <br/> |[Zelle "Format" (Abschnitt "Shape Data")](format-cell-shape-data-section.md) <br/> |
|Invisible  <br/> |Gibt an, ob das Shape-Datenelement im Fenster Shape-Daten angezeigt wird.  <br/> |[Zelle "Invisible" (Abschnitt "Shape Data")](invisible-cell-shape-data-section.md) <br/> |
|Bezeichnung  <br/> |Legt die Beschriftung fest, die Benutzern im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).  <br/> |[Zelle "Label" (Abschnitt "Shape Data")](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Shape Data")](langid-cell-shape-data-section.md) <br/> |
|Eingabeaufforderung  <br/> |Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster Shape-Daten platziert wird.  <br/> |[Zelle "Prompt" (Abschnitt "Shape Data")](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster Shape-Daten aufgelistet werden.  <br/> |[Zelle "SortKey" (Abschnitt "Shape Data")](sortkey-cell-shape-data-section.md) <br/> |
|Typ  <br/> |Gibt einen Datentyp für den Shape-Datenwert an.  <br/> |[Zelle "Type" (Abschnitt "Shape Data")](type-cell-shape-data-section.md) <br/> |
|Wert  <br/> |Enthält den Wert des Shape-Datenelements, der in das Dialogfeld Shape-Daten definieren eingegeben wurde.  <br/> |[Zelle "Value" (Abschnitt "Shape Data")](value-cell-shape-data-section.md) <br/> |
|Überprüfen  <br/> |Gibt an, ob der Benutzer abgefragt wird, um benutzerdefinierte Eigenschafteninformationen für ein Shape eingibt, wenn eine Instanz erstellt oder das Shape dupliziert oder kopiert wird.  <br/> |None.  <br/> |
   

