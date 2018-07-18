---
title: Zellenelement (Hyperlinkzeile) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
ms.openlocfilehash: b664f5e0ac7cfe27b7198dd59b1b8be1af276db7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796584"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Zellenelement (Hyperlinkzeile) ("Visio XML")

Enthält die Informationen für einen einzelnen Hyperlink, der mit einer Form verknüpft ist. Ein Shape enthält **eine Zeile für jeden Hyperlink** . 
  
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
|[Zeilenelement (Linkabschnitt)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Enthält die Informationen für einen einzelnen Hyperlink, der mit einer Form verknüpft ist. Ein Shape enthält **eine Zeile für jeden Hyperlink** .  <br/> |
   
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
|Adresse  <br/> |Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.  <br/> |[Zelle "Address" (Abschnitt "Hyperlinks")](address-cell-hyperlinks-section.md) <br/> |
|Standard  <br/> |Legt den Standardhyperlink für ein Shape oder Zeichenblatt.  <br/> |[Zelle "Default" (Abschnitt "Hyperlinks")](default-cell-hyperlinks-section.md) <br/> |
|Beschreibung  <br/> |Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.  <br/> |[Zelle "Description" (Abschnitt "Hyperlinks")](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Stellt eine Zeichenfolge, die Informationen für die Auflösung einer URL, beispielsweise die Koordinaten einer Imagemap übergibt.  <br/> |[Zelle "ExtraInfo" (Abschnitt "Hyperlinks")](extrainfo-cell-hyperlinks-section.md) <br/> |
|Frame  <br/> |Stellt den Namen eines Zielframes dar, wenn die Anwendung als aktives Dokument in einer Containeranwendung geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.  <br/> |[Zelle "Frame" (Abschnitt "Hyperlinks")](frame-cell-hyperlinks-section.md) <br/> |
|Nicht sichtbare  <br/> |Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird.  <br/> |[Zelle "Invisible" (Abschnitt "Hyperlinks")](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.  <br/> |[Zelle "NewWindow" (Abschnitt "Hyperlinks")](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.  <br/> |[Zelle "SortKey" (Abschnitt "Hyperlinks")](sortkey-cell-hyperlinks-section.md) <br/> |
|SubAddress  <br/> |Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.  <br/> |[Zelle "SubAddress" (Abschnitt "Hyperlinks")](subaddress-cell-hyperlinks-section.md) <br/> |
   

