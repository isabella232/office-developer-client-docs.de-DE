---
title: AuthorEntry-Element (AuthorList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Gibt die Eigenschaften an, die zum Identifizieren des Autors eines Kommentars in einer Zeichnung verwendet werden.
ms.openlocfilehash: 81e5121a953102c7d2e3a5383ae9bc775af4ba41
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338626"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>AuthorEntry-Element (AuthorList_Type complexType) (' Visio XML ')

Gibt die Eigenschaften an, die zum Identifizieren des Autors eines Kommentars in einer Zeichnung verwendet werden.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |comments. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Gibt die Autoren in einer Zeichnung an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Ein 1-basierter Wert, der den Autor identifiziert.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Initialen  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Die Initialen des Autors.  <br/> |Werte des XSD: String-Typs.  <br/> |
|Name  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Der Name des Autors.  <br/> |Werte des XSD: String-Typs.  <br/> |
|Lösungs-Nr  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> |Ein eindeutiger Bezeichner für den Autor.  <br/> |Werte des XSD: String-Typs.  <br/> |
   

