---
title: CommentEntry-Element (CommentList_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Gibt Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.
ms.openlocfilehash: 04e3042da6e0bd1337b9fd969daf8e4e7d234aed
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59582933"
---
# <a name="commententry-element-commentlist_type-complextype-visio-xml"></a>CommentEntry-Element (CommentList_Type complexType) (Visio XML)

Gibt Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentteile** <br/> |comments.xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Gibt die Kommentare in einer Zeichnung an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Ein 1-basierter Wert, der den Autor identifiziert.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Ein eindeutiger Wert, der den Kommentar auf einem Zeichenblatt identifiziert.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|Datum  <br/> |xsd:dateTime  <br/> |Erforderlich  <br/> |Gibt an, wann ein Kommentar erstellt wurde.  <br/> |Werte des Typs "xsd:dateTime".  <br/> |
|Fertig  <br/> |xsd:boolean  <br/> |Optional  <br/> |Gibt den aktuellen Status des Kommentars an.  <br/> |Werte des Typs "xsd:boolean".  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |Optional  <br/> |Gibt an, wann ein Kommentar zuletzt geändert wurde.  <br/> |Werte des Typs "xsd:dateTime".  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |Erforderlich  <br/> |Ein Wert, der das Zeichenblatt identifiziert, auf dem sich der Kommentar befindet.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> |Ein Wert, der die Form identifiziert, auf der sich der Kommentar befindet. Wenn keine ShapeID angegeben ist, bezieht sich der Kommentar auf das Zeichenblatt.  <br/> |Werte des Typs "xsd:unsignedInt".  <br/> |
   

