---
title: Row-Element (User-defined Cells Abschnitt) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Eine vom Benutzer angegebener Informationseinheit, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.
ms.openlocfilehash: 8852c1db31e9a9b8f0860c111da32de6d44dc7f5
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388014"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a>Row-Element (User-defined Cells Abschnitt) ("Visio XML")

Eine vom Benutzer angegebener Informationseinheit, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[UserRow_Type](userrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Document.XML, masters.xml, Master-Shape # .xml, pages.xml, Seite # .xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Eine vom Benutzer angegebener Informationseinheit, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Eine Eigenschaft eines vom Benutzer angegebener bestimmte Informationen, die auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ENTF  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die von einem master-Shape andernfalls geerbt werden würden gelöscht wurde.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|IX  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Gibt den Bezeichner eins für die Zeile. Es sollte eindeutigen sein und andere Bezeichner im gleichen Abschnitt größer. Das Attribut IX wird nur für die Zeichen, Verbindung, Feld, FillGradient, Geometrie, Layer, LineGradient, Absatz, Reviewer, neu und Registerkarten Abschnitte verwendet. Eine Zeile können Sie nur die Attribute IX oder N haben.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|LocalName  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt den eindeutigen Namen der Sprache ab der Zeile an.  <br/> |Werte des Typs xsd: String.  <br/> |
|N  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt die eindeutige sprachenunabhängige Name der Zeile an. Das N-Attribut wird nur für die Benutzer, Eigenschaften-, Aktionen, Steuerelement, Verbindung, Hyperlink und ActionTag Abschnitte verwendet. Eine Zeile können Sie nur die Attribute IX oder N haben.  <br/> |Werte des Typs xsd: String.  <br/> |
|T  <br/> |XSD: String  <br/> |Optional  <br/> |Gibt den Typ des geometrischen Pfads dargestellt durch die Zeile und in Geometrie Visualisierung verwendet. Das T-Attribut wird nur für den Abschnitt "Geometry" verwendet.  <br/> |Werte des Typs xsd: String.  <br/> |
   

