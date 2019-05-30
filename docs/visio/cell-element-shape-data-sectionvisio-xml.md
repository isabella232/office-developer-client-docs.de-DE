---
title: Cell-Element (Shape Data Section) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Gibt eine Eigenschaft der Shape-Daten an.
ms.openlocfilehash: 3a6238f19f27d001d3c9eebcbcec720822a0ed40
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539376"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Cell-Element (Shape Data Section) (Visio XML)

Gibt eine Eigenschaft der Shape-Daten an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Master #. XML, Seite #. XML  <br/> |
   
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
|[Row-Element (Shape-Datenabschnitt)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Shape-daten_type](propertyrow_type-complextypevisio-xml.md) <br/> |Gibt eine Shape-Dateneingabe für das Zuordnen von Daten zu einer Form an.  <br/> |
   
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
|Kalender  <br/> |Gibt den Typ des Kalenders an, der verwendet wird, wenn ein Shape-Datenelement vom Typ Datum ist.  <br/> |[Zelle "Calendar" (Abschnitt "Shape Data")](calendar-cell-shape-data-section.md) <br/> |
|Datalinked  <br/> |Gibt an, ob die Zeile Shape-Daten derzeit mit einem Feld in einem Datenrecordset verknüpft ist.  <br/> ||
|Format  <br/> |Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.  <br/> |[Zelle "Format" (Abschnitt "Shape Data")](format-cell-shape-data-section.md) <br/> |
|Invisible  <br/> |Gibt an, ob das Shape-Datenelement im Fenster Shape-Daten angezeigt wird.  <br/> |[Zelle "Invisible" (Abschnitt "Shape Data")](invisible-cell-shape-data-section.md) <br/> |
|Label  <br/> |Legt die Beschriftung fest, die Benutzern im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).  <br/> |[Zelle "Label" (Abschnitt "Shape Data")](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Shape Data")](langid-cell-shape-data-section.md) <br/> |
|Eingabeaufforderung  <br/> |Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster Shape-Daten platziert wird.  <br/> |[Zelle "Prompt" (Abschnitt "Shape Data")](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster Shape-Daten aufgelistet werden.  <br/> |[Zelle "SortKey" (Abschnitt "Shape Data")](sortkey-cell-shape-data-section.md) <br/> |
|Typ  <br/> |Gibt einen Datentyp für den Shape-Datenwert an.  <br/> |[Zelle "Type" (Abschnitt "Shape Data")](type-cell-shape-data-section.md) <br/> |
|Wert  <br/> |Enthält den Wert des Shape-Datenelements, der in das Dialogfeld Shape-Daten definieren eingegeben wurde.  <br/> |[Zelle "Value" (Abschnitt "Shape Data")](value-cell-shape-data-section.md) <br/> |
|Überprüfen  <br/> |Gibt an, ob der Benutzer beim Erstellen einer Instanz oder beim Duplizieren oder Kopieren der Form benutzerdefinierte Eigenschafteninformationen für eine Form eingeben soll.  <br/> |None.  <br/> |
   

