---
title: DataConnection_Type complexType (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 8d0020f26a3b8360e4af0194310f9a137717d415
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59563070"
---
# <a name="dataconnection_type-complextype-visio-xml"></a>DataConnection_Type complexType (Visio XML)

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |xsd:boolean  <br/> |Optional  <br/> ||Werte des Typs "xsd:boolean".  <br/> |
|Befehl  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|ConnectionString  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|FileName  <br/> |xsd:string  <br/> |erforderlich  <br/> ||Werte des Typs "xsd:string".  <br/> |
|FriendlyName  <br/> |xsd:string  <br/> |Optional  <br/> ||Werte des Typs "xsd:string".  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |erforderlich  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
|Timeout  <br/> |xsd:unsignedInt  <br/> |Optional  <br/> ||Werte des Typs "xsd:unsignedInt".  <br/> |
   

