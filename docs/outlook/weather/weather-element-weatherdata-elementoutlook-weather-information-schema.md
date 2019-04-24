---
title: Weather-Element (WeatherData-Element) (Outlook Wetter Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Gibt die Wetterbedingungen für einen Standort an.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355146"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>Weather-Element (WeatherData-Element) (Outlook Wetter Information-Schema)

Gibt die Wetterbedingungen für einen Standort an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[weathertype](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo. xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Definiert das wetterelement.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[aktuellen](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die aktuellen Wetterbedingungen an.  <br/> |
|[Prognose](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecasttype](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen im Voraus an: heute, morgen, übermorgen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Attribution  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt die Quelle der Wetterinformationen an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|degreetype  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt die Einheit für die Temperatur des Standorts an, beispielsweise Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt die URL des Bilds für den Speicherort an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|TimeZone  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt den GMT-Offset an.  <br/> |Ein Wert zwischen-11 und 12 inklusive  <br/> |
|url  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt die URL für die Webseite des Wetter Diensts an, die Wetterinformationen für den angegebenen Speicherort enthält.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|weatherlocationcode  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den Code an, der dem Speicherort zugeordnet ist, an dem mehrere Standorte mit demselben Namen unterschieden werden.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|weatherlocationname  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den Namen des Speicherorts an, der im Dropdown-Steuerelement angezeigt wird.  <br/> |Ein Wert vom Typ xs: String  <br/> |
   

