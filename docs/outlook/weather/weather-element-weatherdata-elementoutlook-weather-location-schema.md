---
title: Weather-Element (WeatherData-Element) (Outlook-Wetter Standort Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Gibt den Ort an, an dem das Wetter gemeldet werden soll.
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539012"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>Weather-Element (WeatherData-Element) (Outlook-Wetter Standort Schema)

Gibt den Ort an, an dem das Wetter gemeldet werden soll.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[weathertype](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Schemadatei** <br/> |getweatherlocation. xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Definiert das Weather-Element.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt einen Code an, der dem Speicherort zugeordnet ist, um mehrere Standorte mit dem gleichen Namen zu unterscheiden.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|weatherlocationname  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den Namen des Speicherorts an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
   

