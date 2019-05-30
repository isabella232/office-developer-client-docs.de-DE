---
title: Weather-Element (WeatherData-Element) (Outlook-Wetter Informations Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Gibt die Wetterbedingungen eines Standorts an.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541267"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>Weather-Element (WeatherData-Element) (Outlook-Wetter Informations Schema)

Gibt die Wetterbedingungen eines Standorts an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[weathertype](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
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
|[WeatherData](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Definiert das Weather-Element.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[aktuellen](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die aktuellen Wetterbedingungen an.  <br/> |
|[Prognose](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecasttype](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: heute, morgen, Tag nach morgen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Attribution  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt die Quelle der Wetterinformationen an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|degreetype  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt die Einheit für die Temperatur des Standorts an, beispielsweise Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt die URL des Bilds für den Speicherort an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|TimeZone  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt den GMT-Offset an.  <br/> |Ein Wert zwischen-11 und 12 inklusive  <br/> |
|url  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt die URL für die Webseite des Wetter Diensts an, die Wetterinformationen für den angegebenen Speicherort enthält.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|weatherlocationcode  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den Code an, der dem Speicherort zugeordnet ist, der verwendet wird, um mehrere Standorte mit demselben Namen zu unterscheiden.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|weatherlocationname  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt den Namen des Speicherorts an, der im Dropdown-Steuerelement angezeigt wird.  <br/> |Ein Wert vom Typ xs: String  <br/> |
   

