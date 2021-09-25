---
title: AuthorEntry-Element (AuthorList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Gibt Eigenschaften an, mit denen der Autor eines Kommentars in einer Zeichnung identifiziert wird.
ms.openlocfilehash: e8681a0425f7749924358ee088fd6499456b926d
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59578235"
---
# <a name="authorentry-element-authorlist_type-complextype-visio-xml"></a>AuthorEntry-Element (AuthorList_Type complexType) (Visio XML)

Gibt Eigenschaften an, mit denen der Autor eines Kommentars in einer Zeichnung identifiziert wird.
  
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Gibt die Autoren in einer Zeichnung an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> |Ein 1-basierter Wert, der den Autor identifiziert.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Initialen  <br/> |xsd:string  <br/> |Optional  <br/> |Die Initialen des Autors.  <br/> |Werte des Typs "xsd:string".  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> |Der Name des Autors.  <br/> |Werte des Typs "xsd:string".  <br/> |
|ResolutionID  <br/> |xsd:string  <br/> |Optional  <br/> |Ein eindeutiger Bezeichner für den Autor.  <br/> |Werte des Typs "xsd:string".  <br/> |
   

