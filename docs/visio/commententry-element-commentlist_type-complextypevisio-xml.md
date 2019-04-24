---
title: CommentEntry-Element (CommentList_Type complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Gibt die Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.
ms.openlocfilehash: 79d15b95f986826a4848c2dfbb003255d3482134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329540"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>CommentEntry-Element (CommentList_Type complexType) (' Visio XML ')

Gibt die Eigenschaften an, die zum Identifizieren eines Kommentars in einer Zeichnung verwendet werden.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15. xsd  <br/> |
|**Dokumentteile** <br/> |comments. XML  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Kommentarlist](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Gibt die Kommentare in einer Zeichnung an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Ein 1-basierter Wert, der den Autor identifiziert.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Kommentar-Nr.  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Ein eindeutiger Wert, der den Kommentar in einem Zeichenblatt identifiziert.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|Datum  <br/> |XSD: dateTime  <br/> |erforderlich  <br/> |Gibt an, wann ein Kommentar erstellt wurde.  <br/> |Werte des XSD: dateTime-Typs.  <br/> |
|Fertig  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt den aktuellen Status des Kommentars an.  <br/> |Werte des XSD: Boolean-Typs.  <br/> |
|EditDate  <br/> |XSD: dateTime  <br/> |Optional  <br/> |Gibt an, wann ein Kommentar zuletzt geändert wurde.  <br/> |Werte des XSD: dateTime-Typs.  <br/> |
|PageID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> |Ein Wert, der das Zeichenblatt identifiziert, in dem der Kommentar angezeigt wird.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
|ShapeID  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> |Ein Wert, der die Form identifiziert, in der sich der Kommentar befindet. Wenn kein Shape-Wert angegeben ist, verweist der Kommentar auf das Zeichenblatt.  <br/> |Werte des XSD: unsignedInt-Typs.  <br/> |
   

