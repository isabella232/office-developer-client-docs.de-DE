---
title: CommentEntry_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6d9e99b8-fcd6-f36b-960e-bcf3a23afe04
ms.openlocfilehash: 840f660d72acbda052d4729846d8a26686d82b2a
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540126"
---
# <a name="commententry_type-complextype-visio-xml"></a>CommentEntry_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |xsd:string  <br/> |
   
## <a name="definition"></a>Definition

```XML
      <xs:complexType name="CommentEntry_Type">
        <xs:complexContent>
        <xs:extension base="xsd:string">
      
    <xs:attribute name="AuthorID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="PageID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="ShapeID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="Date"
  type="xsd:dateTime"
     use="required"
    />
    <xs:attribute name="EditDate"
  type="xsd:dateTime"
    />
    <xs:attribute name="Done"
  type="xsd:boolean"
    />
    <xs:attribute name="CommentID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="AutoCommentType"
  type="xsd:unsignedInt"
    />
        </xs:extension>
        </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AuthorID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|AutoCommentType  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|CommentID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|Datum  <br/> |xsd:dateTime  <br/> |erforderlich  <br/> ||Werte des xsd:dateTime-Typs.  <br/> |
|Fertig  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des typs xsd:boolean.  <br/> |
|EditDate  <br/> |xsd:dateTime  <br/> |Optional  <br/> ||Werte des xsd:dateTime-Typs.  <br/> |
|PageID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|ShapeID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
   

