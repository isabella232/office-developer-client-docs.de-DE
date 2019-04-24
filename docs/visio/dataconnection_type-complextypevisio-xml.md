---
title: DataConnection_Type complexType (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 13683c47-2bc8-1345-ed0e-4175a06ea452
ms.openlocfilehash: 0253bf261868ec335bcc295c479cdfc98da79490
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32344604"
---
# <a name="dataconnectiontype-complextype-visio-xml"></a>DataConnection_Type complexType (' Visio XML ')

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06 -05. xsd  <br/> |
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

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|AlwaysUseConnectionFile  <br/> |XSD: Boolean  <br/> |Optional  <br/> ||Werte des XSD: Boolean-Typs.  <br/> |
|Befehl  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|ConnectionString  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|FileName  <br/> |XSD: Zeichenfolge  <br/> |erforderlich  <br/> ||Werte des XSD: String-Typs.  <br/> |
|FriendlyName  <br/> |XSD: Zeichenfolge  <br/> |Optional  <br/> ||Werte des XSD: String-Typs.  <br/> |
|ID  <br/> |XSD: unsignedInt  <br/> |erforderlich  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
|Timeout  <br/> |XSD: unsignedInt  <br/> |Optional  <br/> ||Werte des XSD: unsignedInt-Typs.  <br/> |
   

