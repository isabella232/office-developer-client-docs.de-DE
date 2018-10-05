---
title: Wetter-Element (Weatherdata-Element) (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Gibt die Wetterbedingungen einen Speicherort an.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390660"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a>Wetter-Element (Weatherdata-Element) (Outlook Wetter Informationen-Schema)

Gibt die Wetterbedingungen einen Speicherort an.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|**Elementtyp** <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[WeatherData](weatherdata-element-outlook-weather-information-schema.md) <br/> ||Definiert das Wetter-Element.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[aktuelle](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die aktuelle Wettervorhersage an.  <br/> |
|[Planung](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Gibt an, die Wetterbedingungen zukünftigen mindestens drei Tage im Voraus einschließlich heute: heute, morgen, übermorgen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Zuweisung  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt die Quelle der Wetterinformationen.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|degreetype  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt die Maßeinheit für die Temperatur des Speicherorts beispielsweise Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt die URL des Bilds für den Speicherort.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|Zeitzone  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt den Offset GMT.  <br/> |Ein Wert zwischen-11 und 12 inklusive  <br/> |
|url  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt die URL für die Webseite des Diensts Wetter, die für den angegebenen Speicherort Wetterinformationen enthält.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt den Code, der mit dem Speicherort zum unterscheiden von mehreren Standorten mit dem gleichen Namen zugeordnet ist.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt den Namen des Speicherorts, der angezeigt wird im Dropdown-Steuerelement.  <br/> |Ein Wert, der den Typ xs:  <br/> |
   

