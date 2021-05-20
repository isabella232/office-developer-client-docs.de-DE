---
title: Row-Element (Abschnitt "User-defined Cells") (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9fc27888-2809-aa29-4dbb-7e4f8a0c4758
description: Eine vom Benutzer angegebene Information, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.
ms.openlocfilehash: 1573fd6ab27cc1dbec9559552ec33d9a4ad19fd2
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538172"
---
# <a name="row-element-user-defined-cells-section-visio-xml"></a>Row-Element (Abschnitt "User-defined Cells") (Visio XML)

Eine vom Benutzer angegebene Information, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[UserRow_Type](userrow_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |document.xml, masters.xml, Master#.xml, pages.xml, Seite#.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Row" type="UserRow_Type" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Section](section-element-sheet_type-complextypevisio-xml.md) <br/> |[Section_Type](section_type-complextypevisio-xml.md) <br/> |Eine vom Benutzer angegebene Information, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Cell](cell-element-user-defined-cells-sectionvisio-xml.md) <br/> |[Cell_Type](cell_type-complextypevisio-xml.md) <br/> |Eine Eigenschaft eines benutzerdefinierten Informationsteils, auf die von anderen Zellen und Add-On-Tools verwiesen werden kann.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Del  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob eine Zeile, die andernfalls von einem Master-Shape geerbt würde, gelöscht wurde.  <br/> |Werte des typs xsd:boolean.  <br/> |
|IX  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Gibt den 1-basierten Bezeichner für die Zeile an. Er sollte unqiue und größer als andere Bezeichner im gleichen Abschnitt sein. Das IX-Attribut wird nur für die Abschnitte Character, Connection, Field, FillGradient, Geometry, Layer, LineGradient, Paragraph, Reviewer, Scratch und Tabs verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|LocalName  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachabhängigen Namen der Zeile an.  <br/> |Werte des xsd:string-Typs.  <br/> |
|N  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den eindeutigen sprachunabhängigen Namen der Zeile an. Das N-Attribut wird nur für die Abschnitte User, Property, Actions, Control, Connection, Hyperlink und ActionTag verwendet. Eine Zeile kann nur eines der IX- oder N-Attribute aufweisen.  <br/> |Werte des xsd:string-Typs.  <br/> |
|T  <br/> |xsd:string  <br/> |Optional  <br/> |Gibt den Typ des geometrischen Pfads an, der durch die Zeile dargestellt und in der Geometrievisualisierung verwendet wird. Das T-Attribut wird nur für den Abschnitt Geometry verwendet.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

