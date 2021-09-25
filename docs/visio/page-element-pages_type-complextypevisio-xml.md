---
title: Page-Element (Pages_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Enthält Elemente, die eine Seite im Dokument definieren.
ms.openlocfilehash: acdc74fa35480dccdd240030e59eafd57114b080
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59573796"
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
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
|Hintergrund  <br/> |xsd:boolean  <br/> |Optional  <br/> |Ein Kennzeichen, das angibt, ob es sich bei der Seite um eine Hintergrundseite handelt.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID der Hintergrundseite dieser Seite.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Die eindeutige ID des Elements innerhalb des übergeordneten Elements.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der Name vom Benutzer angepasst wurde.  <br/> |Werte des Typs "xsd:Boolean".  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt an, ob der universelle Name vom Benutzer angepasst wurde.  <br/> |Werte des Typs "xsd:Boolean".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Elements.  <br/> |Werte des Typs "xsd:string".  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> |Der universelle Name des Elements.  <br/> |Werte des Typs "xsd:string".  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Die ID des Prüfers, der der Markupüberlagerung zugeordnet ist.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, von der eine neue Ansicht (fenster) beim ersten Öffnen ausgeht.  <br/> |Werte des Typs "xsd:double".  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |Optional  <br/> |**ViewCenterX** und **ViewCenterY** geben einen Mittelpunkt auf einer Seite an, von der eine neue Ansicht (fenster) beim ersten Öffnen ausgeht.  <br/> |Werte des Typs "xsd:double".  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |Optional  <br/> |Der standardmäßige Vergrößerungsfaktor, der beim Öffnen einer neuen Ansicht (eines Fensters) der Seite verwendet werden soll. Beispiel: 1 = 100 %; 1,5 = 150 % usw.  <br/> |Werte des Typs "xsd:double".  <br/> |
   

