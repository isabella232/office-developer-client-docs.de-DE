---
title: Forecast-Element (WeatherType ComplexType) (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Gibt an, die Wetterbedingungen zukünftigen mindestens drei Tage im Voraus einschließlich heute: heute, morgen, übermorgen.'
ms.openlocfilehash: c618b753ddf8a72fce270800675982f1a7f7af5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796097"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>Forecast-Element (WeatherType ComplexType) (Outlook Wetter Informationen-Schema)

Gibt an, die Wetterbedingungen zukünftigen mindestens drei Tage im Voraus einschließlich heute: heute, morgen, übermorgen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Wetterbericht](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die Wetterbedingungen einen Speicherort an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs: Date  <br/> |erforderlich  <br/> |Gibt das Datum für die Planung.  <br/> |Ein Wert, der den Typ xs: Date  <br/> |
|Tag  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt einen Tag für die Planung.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|hohe  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die höchste prognostizierten Temperatur an.  <br/> |Der Wert der Type-xs  <br/> |
|Niedrig  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die geplanten niedrigsten Temperatur an.  <br/> |Der Wert der Type-xs  <br/> |
|precip  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die Möglichkeit Prozentsatz Niederschlagsmenge an.  <br/> |Der Wert der Type-xs  <br/> |
|shortday  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt einen Code für die geplanten Bedingungen an.  <br/> |Der Wert der Type-xs  <br/> |
|skytextday  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter, die die geplanten Bedingungen zu beschreiben.  <br/> |Ein Wert, der den Typ xs:  <br/> |
   

