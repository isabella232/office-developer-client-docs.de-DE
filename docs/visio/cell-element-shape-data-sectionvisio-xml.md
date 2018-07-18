---
title: Zellenelement (Abschnitt "Shape Data") ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 98643832-7861-385d-3a52-0060ea413e2e
description: Gibt eine Eigenschaft eines Shape-Daten an.
ms.openlocfilehash: 899b518f86979c831c0c05913420c7a62f0ea717
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796627"
---
# <a name="cell-element-shape-data-section-visio-xml"></a>Zellenelement (Abschnitt "Shape Data") ("Visio XML")

Gibt eine Eigenschaft eines Shape-Daten an.
  
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
|[Zeilenelement (Shape-Datenabschnitt)](row-element-shape-data-sectionvisio-xml.md) <br/> |[Shape-Datentyp](propertyrow_type-complextypevisio-xml.md) <br/> |Gibt ein Shape-Dateneingabe zum Zuordnen von Daten mit einer Form an.  <br/> |
   
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
|Kalender  <br/> |Gibt den Typ des Kalenders an, der verwendet wird, wenn ein Shape-Datenelement vom Typ Datum ist.  <br/> |[Zelle "Calendar" (Abschnitt "Shape Data")](calendar-cell-shape-data-section.md) <br/> |
|DataLinked  <br/> |Gibt an, ob die Zeile mit Shape-Daten derzeit an ein Feld in einem Datenrecordset verknüpft ist.  <br/> ||
|Format  <br/> |Gibt die Formatierung eines Shape-Datenelements an, bei dem es sich um eine Zeichenfolge, eine feste Liste, eine Zahl, eine variable Liste, ein Datum oder eine Uhrzeit, eine Zeitdauer oder eine Währung handeln kann.  <br/> |[Zelle "Format" (Abschnitt "Shape Data")](format-cell-shape-data-section.md) <br/> |
|Nicht sichtbare  <br/> |Gibt an, ob das Shape-Datenelement im Fenster Shape-Daten angezeigt wird.  <br/> |[Zelle "Invisible" (Abschnitt "Shape Data")](invisible-cell-shape-data-section.md) <br/> |
|Beschriftung  <br/> |Legt die Beschriftung fest, die Benutzern im Fenster Shape-Daten angezeigt wird. Eine Beschriftung besteht aus alphanumerischen Zeichen, einschließlich dem Unterstrich (_).  <br/> |[Zelle "Label" (Abschnitt "Shape Data")](label-cell-shape-data-section.md) <br/> |
|LangID  <br/> |Gibt die Sprache an, in der der Wert für die Shape-Daten eingegeben wurde.  <br/> |[Zelle "LangID" (Abschnitt "Shape Data")](langid-cell-shape-data-section.md) <br/> |
|Prompt  <br/> |Spezifiziert den Text der Beschreibung oder Anweisung, der als Tipp angezeigt wird, wenn der Mauszeiger über einem Wert im Fenster Shape-Daten platziert wird.  <br/> |[Zelle "Prompt" (Abschnitt "Shape Data")](prompt-cell-shape-data-section.md) <br/> |
|SortKey  <br/> |Enthält eine Zeichenfolge, die die Reihenfolge beeinflusst, in der Elemente im Fenster Shape-Daten aufgelistet werden.  <br/> |[Zelle "SortKey" (Abschnitt "Shape Data")](sortkey-cell-shape-data-section.md) <br/> |
|Typ  <br/> |Gibt einen Datentyp für den Shape-Datenwert an.  <br/> |[Zelle "Type" (Abschnitt "Shape Data")](type-cell-shape-data-section.md) <br/> |
|Wert  <br/> |Enthält den Wert des Shape-Datenelements, der in das Dialogfeld Shape-Daten definieren eingegeben wurde.  <br/> |[Zelle "Value" (Abschnitt "Shape Data")](value-cell-shape-data-section.md) <br/> |
|Vergewissern Sie sich  <br/> |Gibt an, ob der Benutzer aufgefordert wird, um Informationen zu benutzerdefinierten Eigenschaften für ein Shape einzugeben, wenn eine Instanz oder beim Duplizieren oder Kopieren der Form.  <br/> |Keine.  <br/> |
   

