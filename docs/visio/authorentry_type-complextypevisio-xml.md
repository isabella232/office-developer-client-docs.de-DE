---
title: AuthorEntry_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6ea7b946-ecd3-1524-5e36-a2c35cb11d7a
ms.openlocfilehash: 39cf47915230b18d22db78f5470fd9c26b9c77ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796396"
---
# <a name="authorentrytype-complextype-visio-xml"></a>AuthorEntry_Type ComplexType ("Visio XML")

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
      <xs:complexType name="AuthorEntry_Type">
    <xs:attribute name="Name"
  type="xsd:string"
    />
    <xs:attribute name="Initials"
  type="xsd:string"
    />
    <xs:attribute name="ResolutionID"
  type="xsd:string"
    />
    <xs:attribute name="ID"
  type="xsd:unsignedInt"
     use="required"
    />
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|ID  <br/> |XSD:unsignedInt  <br/> |erforderlich  <br/> ||Werte des Typs Xsd:unsignedInt.  <br/> |
|Initialen  <br/> |XSD: String  <br/> |Optional  <br/> ||Werte des Typs xsd: String.  <br/> |
|Name  <br/> |XSD: String  <br/> |Optional  <br/> ||Werte des Typs xsd: String.  <br/> |
|ResolutionID  <br/> |XSD: String  <br/> |Optional  <br/> ||Werte des Typs xsd: String.  <br/> |
   

