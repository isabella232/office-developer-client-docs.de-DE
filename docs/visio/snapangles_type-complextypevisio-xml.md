---
title: SnapAngles_Type ComplexType ("Visio XML")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 1110a656-d8cd-19d0-1af0-31a6675bf89b
ms.openlocfilehash: 9934150dbca6e7a2787335a7afd939dcb48a4a15
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798141"
---
# <a name="snapanglestype-complextype-visio-xml"></a>SnapAngles_Type ComplexType ("Visio XML")

## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/visio/2011/1/core  <br/> |
|**Schemadatei** <br/> |VisioSchema15-2012-06-05.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
          <xs:complexType name="SnapAngles_Type">
          
          <xs:sequence>
    <xs:element name="SnapAngle"  type="SnapAngle_Type"
     minOccurs="0"
     maxOccurs="unbounded"
    >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
      
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[SnapAngle](snapangle-element-snapangles_type-complextypevisio-xml.md) <br/> |[SnapAngle_Type](snapangle_type-complextypevisio-xml.md) <br/> ||
   
### <a name="attributes"></a>Attribute

Keine.
  

