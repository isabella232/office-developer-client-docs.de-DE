---
title: Actions_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31070969-2091-d00e-5dd1-b9c6034f76d9
ms.openlocfilehash: 384b948c61f3b618d108db090721ea6768d69372
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538410"
---
# <a name="actions_type-complextype-visio-xml"></a>Actions_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Section_Type  <br/> |
   
## <a name="definition"></a>Definition

```XML
          <xs:complexType name="Actions_Type">
          
          <xs:complexContent>
          <xs:extension base="Section_Type">
          <xs:sequence minOccurs="0" maxOccurs="unbounded">
    <xs:element name="Row"  type="ActionsRow_Type"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:extension>
      </xs:complexContent>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Row](row-element-actions-sectionvisio-xml.md) <br/> |[ActionsRow_Type](actionsrow_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

Keine.
  

