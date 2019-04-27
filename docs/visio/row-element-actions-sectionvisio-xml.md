---
title: Zeilenelement (Abschnitt "Actions") (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5141589b-10f3-f908-56d2-206244f449fb
description: Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.
ms.openlocfilehash: 509fd06a77419bf684b214ff5a5d16f24a1f4a84
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/26/2019
ms.locfileid: "32356420"
---
# <a name="row-element-actions-section-visio-xml"></a>Zeilenelement (Abschnitt "Actions") (' Visio XML ')

Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |"Masters. xml", "Master #. xml", "pages. xml", "page #. xml"  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="ActionsRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Enthält Zeilen, die Menüelemente in einem Kontext- oder Aktionstagmenü eines Shapes oder Zeichenblatts beschreiben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-actions-rowvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Gibt eine Eigenschaft einer Aktion an, die einem benutzerdefinierten Befehl in einem Kontext-oder aktionstagmenü zugeordnet ist.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ENTF  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|IX  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Gibt den 1-basierten Bezeichner für die Zeile an. Sie sollte unqiue und größer sein als andere Bezeichner im gleichen Abschnitt. Das Attribut IX wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Rezensent, Scratch und Tabs verwendet. Eine Zeile kann nur eines der Attribute IX oder N aufweisen.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|LocalName  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den eindeutigen sprachenabhängigen Namen der Zeile an.  <br/> |Werte des XSD: String-Typs.  <br/> |
|N  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet. Eine Zeile kann nur eines der Attribute IX oder N aufweisen.  <br/> |Werte des XSD: String-Typs.  <br/> |
|T  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Gibt den Typ des durch die Zeile dargestellten geometrischen Pfads an und wird in der Geometrie Visualisierung verwendet. Das T-Attribut wird nur für den Abschnitt Geometry verwendet.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

