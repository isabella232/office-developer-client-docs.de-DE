---
title: Page_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 4bc5c0c4-3ee3-7f63-541a-1f1854d4201c
ms.openlocfilehash: 3a0153b724539136fe142c2489badcf9895af765
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537983"
---
# <a name="page_type-complextype-visio-xml"></a>Page_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
          <xs:complexType name="Page_Type">
          
          <xs:all>
    <xs:element name="PageSheet"  type="PageSheet_Type"
     minOccurs="0"
     maxOccurs="1"
    >
    </xs:element>
    
    <xs:element name="Rel"  type="Rel_Type"
     minOccurs="1"
     maxOccurs="1"
    >
    </xs:element>
    
      </xs:all>
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="NameU"
  type="xsd:string"
    />
    <xs:attribute name="IsCustomName"
  type="xsd:boolean"
    />
    <xs:attribute name="IsCustomNameU"
  type="xsd:boolean"
    />
    <xs:attribute name="Background"
  type="xsd:boolean"
    />
    <xs:attribute name="BackPage"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="ViewScale"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterX"
  type="xsd:double"
    />
    <xs:attribute name="ViewCenterY"
  type="xsd:double"
    />
    <xs:attribute name="ReviewerID"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AssociatedPage"
  type="xsd:unsignedInt"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> ||
|[Rel](rel-element-page_type-complextypevisio-xml.md) <br/> |[Rel_Type](rel_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AssociatedPage  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|Hintergrund  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des typs xsd:boolean.  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des typs xsd:boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des typs xsd:boolean.  <br/> |
|Name  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|NameU  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des xsd:double-Typs.  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des xsd:double-Typs.  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |Optional  <br/> ||Werte des xsd:double-Typs.  <br/> |
   

