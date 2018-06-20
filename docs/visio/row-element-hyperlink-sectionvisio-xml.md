---
title: Row-Element (Hyperlink Abschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f87cd7a4-b9de-5fb1-20ec-90759c966bd9
description: Enthält Elemente zum Erstellen mehrerer Liniensprünge zwischen einem Shape oder Zeichenblatt und einem anderen Zeichenblatt, einer anderen Datei oder einer Website.
ms.openlocfilehash: ea2428ffbefa9ac2bf592e37d10c0089e72f6ef1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797935"
---
# <a name="row-element-hyperlink-section-visio-xml"></a>Row-Element (Hyperlink Abschnitt) ("Visio XML")

Enthält Elemente zum Erstellen mehrerer Liniensprünge zwischen einem Shape oder Zeichenblatt und einem anderen Zeichenblatt, einer anderen Datei oder einer Website.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[HyperlinkRow_Type](hyperlinkrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |# .xml Master, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="HyperlinkRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Enthält Elemente zum Erstellen mehrerer Liniensprünge zwischen einem Shape oder Zeichenblatt und einem anderen Zeichenblatt, einer anderen Datei oder einer Website.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-hyperlink-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Enthält die Informationen für einen einzelnen Hyperlink, der mit einer Form verknüpft ist  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ENTF  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt den Bezeichner eins für die Zeile. Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet. Eine Zeile können Sie nur die Attribute IX oder N haben.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt den eindeutigen Namen der Sprache ab der Zeile an.  <br/> |Werte des Typs xsd: String.  <br/> |
|N  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet. Eine Zeile können Sie nur die Attribute IX oder N haben.  <br/> |Werte des Typs xsd: String.  <br/> |
|T  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet. Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.  <br/> |Werte des Typs xsd: String.  <br/> |
   

