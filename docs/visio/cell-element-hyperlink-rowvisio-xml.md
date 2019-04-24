---
title: Cell-Element (Hyperlink-Zeile) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: d2089db4-39eb-06d3-d2f8-9465baef5c75
description: Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine Hyperlink-Zeile.
ms.openlocfilehash: 6644dc70f3d3616e5c20587db4eabaaf773c31d3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356063"
---
# <a name="cell-element-hyperlink-row-visio-xml"></a>Cell-Element (Hyperlink-Zeile) (' Visio XML ')

Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine **Hyperlink** -Zeile. 
  
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
|[Row-Element (Hyperlink-Abschnitt)](row-element-hyperlink-sectionvisio-xml.md) <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |Enthält die Informationen für einen einzelnen Hyperlink, der einem Shape zugeordnet ist. Ein Shape enthält für jeden Hyperlink eine **Hyperlink** -Zeile.  <br/> |
   
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
|Adresse  <br/> |Legt eine aufzurufende URL-Adresse, einen Dateinamen oder einen UNC-Pfad fest.  <br/> |[Zelle "Address" (Abschnitt "Hyperlinks")](address-cell-hyperlinks-section.md) <br/> |
|Standard  <br/> |Legt den Standardhyperlink für ein Shape oder eine Seite fest.  <br/> |[Zelle "Default" (Abschnitt "Hyperlinks")](default-cell-hyperlinks-section.md) <br/> |
|Beschreibung  <br/> |Stellt eine beschreibende Textzeichenfolge für einen Hyperlink dar.  <br/> |[Zelle "Description" (Abschnitt "Hyperlinks")](description-cell-hyperlinks-section.md) <br/> |
|ExtraInfo  <br/> |Stellt eine Zeichenfolge dar, die Informationen für die Auflösung einer URL enthält (z. B. die Koordinaten einer Imagemap).  <br/> |[Zelle "ExtraInfo" (Abschnitt "Hyperlinks")](extrainfo-cell-hyperlinks-section.md) <br/> |
|Rahmen  <br/> |Stellt den Namen eines Zielframes dar, wenn die Anwendung als aktives Dokument in einer Containeranwendung geöffnet ist. Der Standardwert ist eine leere Zeichenfolge.  <br/> |[Zelle "Frame" (Abschnitt "Hyperlinks")](frame-cell-hyperlinks-section.md) <br/> |
|Unsichtbar  <br/> |Gibt an, ob im Kontextmenü eines Shapes oder einer Seite ein Hyperlink angezeigt wird.  <br/> |[Zelle "Invisible" (Abschnitt "Hyperlinks")](invisible-cell-hyperlinks-section.md) <br/> |
|NewWindow  <br/> |Gibt an, ob der Hyperlink in einem neuen Fenster geöffnet werden soll.  <br/> |[Zelle "NewWindow" (Abschnitt "Hyperlinks")](newwindow-cell-hyperlinks-section.md) <br/> |
|SortKey  <br/> |Eine Nummer, mit der die Reihenfolge der Hyperlinks im Kontextmenü angegeben wird.  <br/> |[Zelle "SortKey" (Abschnitt "Hyperlinks")](sortkey-cell-hyperlinks-section.md) <br/> |
|SubAddress  <br/> |Gibt eine Position im Zieldokument an, mit der eine Verknüpfung hergestellt werden kann.  <br/> |[Zelle "SubAddress" (Abschnitt "Hyperlinks")](subaddress-cell-hyperlinks-section.md) <br/> |
   

