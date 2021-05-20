---
title: Page-Element (Pages_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Enthält Elemente, die eine Seite im Dokument definieren.
ms.openlocfilehash: f32cf3ed7bbf1e68ddca3fc8f5a1c50ce45fe73e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538025"
---
# <a name="page-element-pages_type-complextype-visio-xml"></a>Page-Element (Pages_Type complexType) (Visio XML)

Enthält Elemente, die eine Seite im Dokument definieren.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |pages.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Enthält die **Page-Elemente** für das Dokument.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Enthält Elemente, die das Seitenblatt für ein **Page-Element** definieren.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Hintergrund  <br/> |xsd:boolean  <br/> |Optional  <br/> |Ein Flag, das angibt, ob es sich bei der Seite um eine Hintergrundseite handelt.  <br/> |Werte des typs xsd:boolean.  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID der Hintergrundseite dieser Seite.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der Name vom Benutzer angepasst wurde.  <br/> |Werte des xsd:Boolean-Typs.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name vom Benutzer angepasst wurde.  <br/> |Werte des xsd:Boolean-Typs.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des xsd:string-Typs.  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des Prüfers, der der Markupüberlagerung zugeordnet ist.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, den eine neue Ansicht (Fenster) beim ersten Öffnen annimmt.  <br/> |Werte des xsd:double-Typs.  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, den eine neue Ansicht (Fenster) beim ersten Öffnen annimmt.  <br/> |Werte des xsd:double-Typs.  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |Optional  <br/> |Der Standardmäßige Vergrößerungsfaktor, der verwendet werden soll, wenn eine neue Ansicht (Fenster) der Seite geöffnet wird. Beispiel: 1 = 100 %; 1,5 = 150 %, und so weiter.  <br/> |Werte des xsd:double-Typs.  <br/> |
   

