---
title: WeatherType ComplexType (Outlook Wetter Speicherort-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Definiert die Parameter Wetter Bedingungen von einem Speicherort an.
ms.openlocfilehash: c3d640789cb68891878c3dca5210ab9dea280180
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387713"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>WeatherType ComplexType (Outlook Wetter Speicherort-Schema)

Definiert die Parameter Wetter Bedingungen von einem Speicherort an.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Schemadatei** <br/> |getweatherlocation.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt einen Code, der den Speicherort zum unterscheiden von mehreren Standorten mit dem gleichen Namen zugeordnet ist.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt den Namen des Speicherorts.  <br/> |Ein Wert, der den Typ xs:  <br/> |
   

