---
title: AuthorEntry-Element (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Gibt Eigenschaften an, die zum Identifizieren des Autors eines Kommentars in einer Zeichnung verwendet werden.
ms.openlocfilehash: 29dc4459d0df3b914d61140cb2c5f33cc3e1306e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537906"
---
# <a name="authorentry-element-authorlist_type-complextype-visio-xml"></a>AuthorEntry-Element (AuthorList_Type complexType) (Visio XML)

Gibt Eigenschaften an, die zum Identifizieren des Autors eines Kommentars in einer Zeichnung verwendet werden.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Gibt die Autoren in einer Zeichnung an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Ein einbasierter Wert, der den Autor identifiziert.  <br/> |Werte des xsd:unsignedInt-Typs.  <br/> |
|Initialen  <br/> |xsd:string  <br/> |Optional  <br/> |Die Initialen des Autors.  <br/> |Werte des xsd:string-Typs.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Autors.  <br/> |Werte des xsd:string-Typs.  <br/> |
|ResolutionID  <br/> |xsd:string  <br/> |Optional  <br/> |Ein eindeutiger Bezeichner für den Autor.  <br/> |Werte des xsd:string-Typs.  <br/> |
   

