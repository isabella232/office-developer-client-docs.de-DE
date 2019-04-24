---
title: WeatherData-Element (Outlook Weather Location Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Definiert das wetterelement.
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355034"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a>WeatherData-Element (Outlook Weather Location Schema)

Definiert das wetterelement.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> ||
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Schemadatei** <br/> |getweatherlocation. xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Wetter](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[weathertype](weathertype-complextype-outlook-weather-location-schema.md) <br/> |Gibt den Speicherort an, an dem Wetterbedingungen gemeldet werden sollen.  <br/> |
   
### <a name="attributes"></a>Attribute

Keine.
  

