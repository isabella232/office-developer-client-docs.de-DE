---
title: AuthorEntry-Element (AuthorList_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 21ca601b-27f0-b30b-a99e-56359bdf594c
description: Gibt Eigenschaften verwendet, um den Autor eines Kommentars in einer Zeichnung zu ermitteln.
ms.openlocfilehash: 905dbc5d08cfb2010c9d749e59584cc294e54e86
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796412"
---
# <a name="authorentry-element-authorlisttype-complextype-visio-xml"></a>AuthorEntry-Element (AuthorList_Type ComplexType) ("Visio XML")

Gibt Eigenschaften verwendet, um den Autor eines Kommentars in einer Zeichnung zu ermitteln.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[AuthorEntry_Type](authorentry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Comments.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="AuthorEntry" type="AuthorEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[AuthorList](authorlist-element-comments_type-complextypevisio-xml.md) <br/> |[AuthorList_Type](authorlist_type-complextypevisio-xml.md) <br/> |Gibt die Autoren in einer Zeichnung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Ein 1-basierte Wert, der Autor identifiziert.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Initialen  <br/> |XSD: String  <br/> |Optional  <br/> |Die Initialen des Autors.  <br/> |Werte des Typs xsd: String.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> |Der Name des Autors.  <br/> |Werte des Typs xsd: String.  <br/> |
|ResolutionID  <br/> |XSD: String  <br/> |Optional  <br/> |Ein eindeutiger Bezeichner für den Autor.  <br/> |Werte des Typs xsd: String.  <br/> |
   

