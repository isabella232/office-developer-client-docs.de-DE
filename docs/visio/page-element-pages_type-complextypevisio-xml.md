---
title: Page-Element (Pages_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Enthält Elemente, mit denen eine Seite im Dokument definiert wird.
ms.openlocfilehash: f32cf3ed7bbf1e68ddca3fc8f5a1c50ce45fe73e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538025"
---
# <a name="page-element-pagestype-complextype-visio-xml"></a>Page-Element (Pages_Type complexType) (Visio XML)

Enthält Elemente, mit denen eine Seite im Dokument definiert wird.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |Pages. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Enthält die **Seiten** Elemente für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die das Seitenblatt für ein **Seiten** Element definieren.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Hintergrund  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Ein Flag, das angibt, ob es sich bei der Seite um eine Hintergrundseite handelt.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|BackPage  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die ID der Hintergrundseite dieser Seite.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Iscustomname  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der Name vom Benutzer angepasst wurde.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|IsCustomNameU  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name vom Benutzer angepasst wurde.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs XSD: String.  <br/> |
|NameU  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der universelle Name des-Elements.  <br/> |Werte des Typs XSD: String.  <br/> |
|ReviewerID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Die ID des Reviewers, der der Markupüberlagerung zugeordnet ist.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ViewCenterX  <br/> |XSD: Double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, den eine neue Ansicht (Fenster) beim anfänglichen öffnen annimmt.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ViewCenterY  <br/> |XSD: Double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, den eine neue Ansicht (Fenster) beim anfänglichen öffnen annimmt.  <br/> |Werte des Typs XSD: Double.  <br/> |
|ViewScale  <br/> |XSD: Double  <br/> |Optional  <br/> |Der Standard Vergrößerungsfaktor, der verwendet wird, wenn eine neue Ansicht (Fenster) der Seite geöffnet wird. Beispiel: 1 = 100%; 1,5 = 150% usw.  <br/> |Werte des Typs XSD: Double.  <br/> |
   

