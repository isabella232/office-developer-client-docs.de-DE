---
title: Cell-Element (Shape Data Section) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Gibt eine Eigenschaft der Shape-Daten an.
ms.openlocfilehash: 5e0c79d9439fb3800a277e039143060eec708b11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339543"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Cell-Element (Shape Data Section) (' Visio XML ')

Gibt eine Eigenschaft der Shape-Daten an.
  
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
|[Row-Element (Shape Data Section)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Shape-data_Type](propertyrow_type-complextypevisio-xml.md) <br/> |Gibt einen Shape-Dateneintrag zum Zuordnen von Daten zu einer Form an.  <br/> |
   
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
|Kalender  <br/> |Gibt den Typ des Kalenders an, der verwendet wird, wenn ein Shape-Datenelement vom Typ Datum ist.  <br/> |[Zelle "Calendar" (Abschnitt "Shape Data")](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Gibt an, ob Shape-Datenzeile derzeit mit einem Feld in einem datenRecordset verknüpft ist.  <br/> ||
|Format  <br/> |Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.  <br/> |[Zelle "Format" (Abschnitt "Shape Data")](format-cell-shape-data-section.md) <br/> |
|Unsichtbar  <br/> |Gibt an, ob das Shape-Datenelement im Fenster Shape-Daten angezeigt wird.  <br/> |[Zelle "Invisible" (Abschnitt "Shape Data")](invisible-cell-shape-data-section.md) <br/> |
|Label  <br/> |Legt die Beschriftung fest, die Benutzern im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).  <br/> |[Zelle "Label" (Abschnitt "Shape Data")](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Shape Data")](langid-cell-shape-data-section.md) <br/> |
|Eingabeaufforderung  <br/> |Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster Shape-Daten platziert wird.  <br/> |[Zelle "Prompt" (Abschnitt "Shape Data")](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster Shape-Daten aufgelistet werden.  <br/> |[Zelle "SortKey" (Abschnitt "Shape Data")](sortkey-cell-shape-data-section.md) <br/> |
|Typ  <br/> |Gibt einen Datentyp für den Shape-Datenwert an.  <br/> |[Zelle "Type" (Abschnitt "Shape Data")](type-cell-shape-data-section.md) <br/> |
|Wert  <br/> |Enthält den Wert des Shape-Datenelements, der in das Dialogfeld Shape-Daten definieren eingegeben wurde.  <br/> |[Zelle "Value" (Abschnitt "Shape Data")](value-cell-shape-data-section.md) <br/> |
|Prüfen  <br/> |Gibt an, ob der Benutzer zum Eingeben von benutzerdefinierten Eigenschaftsinformationen für ein Shape gefragt wird, wenn eine Instanz erstellt oder die Form dupliziert oder kopiert wird.  <br/> |None.  <br/> |
   

