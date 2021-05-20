---
title: DataConnection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 44dceee9a9ef43557e9bc02828f91c2c29d345d6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539649"
---
# <a name="dataconnection_type-complextype-visio-xml"></a>DataConnection_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
      <xs:complexType name="DataConnection_Type">
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
    <xs:attribute name="FileName"
  type="xsd:string"
     use="required"
    />
    <xs:attribute name="ConnectionString"
  type="xsd:string"
    />
    <xs:attribute name="Command"
  type="xsd:string"
    />
    <xs:attribute name="FriendlyName"
  type="xsd:string"
    />
    <xs:attribute name="Timeout"
  type="xsd:unsignedInt"
    />
    <xs:attribute name="AlwaysUseConnectionFile"
  type="xsd:boolean"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des typs xsd:boolean.  <br/> |
|Get-Help  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|FileName  <br/> |xsd:string  <br/> |erforderlich  <br/> ||Werte des xsd:string-Typs.  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des xsd:string-Typs.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des xsd:unsignedInt-Typs.  <br/> |
   

