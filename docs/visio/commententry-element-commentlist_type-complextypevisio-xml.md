---
title: CommentEntry-Element (CommentList_Type ComplexType) ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: b0653622-fa94-4889-68c2-94f3e7a83119
description: Gibt Eigenschaften verwendet, um einen Kommentar in einer Zeichnung zu identifizieren.
ms.openlocfilehash: b2ab1925c8b3b9a9c2d67ac48c1db1768f5916b2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796666"
---
# <a name="commententry-element-commentlisttype-complextype-visio-xml"></a>CommentEntry-Element (CommentList_Type ComplexType) ("Visio XML")

Gibt Eigenschaften verwendet, um einen Kommentar in einer Zeichnung zu identifizieren.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[CommentEntry_Type](commententry_type-complextypevisio-xml.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Schemadatei** <br/> |VisioSchema15.xsd  <br/> |
|**Dokumentbausteine** <br/> |Comments.Xml  <br/> |
   
## <a name="definition"></a>Definition

```XML
< xs:element name="CommentEntry" type="CommentEntry_Type" minOccurs="0" maxOccurs="unbounded" >
< /xs:element >
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[CommentList](commentlist-element-comments_type-complextypevisio-xml.md) <br/> |[CommentList_Type](commentlist_type-complextypevisio-xml.md) <br/> |Gibt die Kommentare in einer Zeichnung.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AutorID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Ein 1-basierte Wert, der Autor identifiziert.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|CommentID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Ein eindeutiger Wert, der den Kommentar in ein Zeichenblatt identifiziert.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|Datum  <br/> |XSD: DateTime  <br/> |erforderlich  <br/> |Gibt an, wann ein Kommentar erstellt wurde.  <br/> |Werte des Typs xsd: DateTime.  <br/> |
|Fertig  <br/> |XSD: Boolean  <br/> |Optional  <br/> |Gibt den aktuellen Status des Kommentars.  <br/> |Werte des Typs xsd: Boolean.  <br/> |
|EditDate  <br/> |XSD: DateTime  <br/> |Optional  <br/> |Gibt an, wann ein Kommentar zuletzt geändert wurde.  <br/> |Werte des Typs xsd: DateTime.  <br/> |
|PageID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> |Ein Wert, der das Zeichenblatt identifiziert ist der Kommentar auf.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
|ShapeID  <br/> |XSD:unsignedInt  <br/> |Optional  <br/> |Ein Wert, der das Shape identifiziert wird der Kommentar auf. Wenn keine ShapeID angegeben ist, bezieht sich auf dem Zeichenblatt der Kommentar.  <br/> |Werte des Typs Xsd:unsignedInt.  <br/> |
   

