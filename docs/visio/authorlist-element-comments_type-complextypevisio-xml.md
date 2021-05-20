---
title: AuthorList-Element (Comments_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4b6950c4-7c03-6462-eeab-3176db9a8f7e
description: Gibt die Autoren von Kommentaren in einer Zeichnung an.
ms.openlocfilehash: c6e94c985d2728ba704a9159ec9bf3c4a2a72e95
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537857"
---
# <a name="authorlist-element-comments_type-complextype-visio-xml"></a>AuthorList-Element (Comments_Type complexType) (Visio XML)

Gibt die Autoren von Kommentaren in einer Zeichnung an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="AuthorList" type="AuthorList_Type" minOccurs="0" maxOccurs="1" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Kommentare](comments-element-comments_type-complextypevisio-xml.md) <br/> |[Comments_Type](comments_type-complextypevisio-xml.md) <br/> |Gibt die Kommentare in einer Zeichnung an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[AuthorEntry](authorentry-element-authorlist_type-complextypevisio-xml.md) <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |Gibt die Eigenschaften an, die den Autor eines Kommentars in einer Zeichnung identifizieren.  <br/> |
   
### <a name="attributes"></a>Attribute

Keine.
  

