---
title: Forecast-Element (weathertype complexType) (Outlook Wetter Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen im Voraus an: heute, morgen, übermorgen.'
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339564"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>Forecast-Element (weathertype complexType) (Outlook Wetter Information-Schema)

Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen im Voraus an: heute, morgen, übermorgen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[forecasttype](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo. xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Wetter](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weathertype](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die Wetterbedingungen für einen Standort an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Datum  <br/> |xs: Datum  <br/> |erforderlich  <br/> |Gibt das Datum für die Prognose an.  <br/> |Ein Wert vom Typ xs: Date  <br/> |
|Tag  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|hohe  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt die prognostizierte höchste Temperatur an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|mit niedriger  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt die prognostizierte niedrigste Temperatur an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|Precip  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt die prozentuale Niederschlagswahrscheinlichkeit an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|shortday  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|skycodeday  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt einen Code für die prognostizierten Bedingungen an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|skytextday  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter an, in denen die prognostizierten Bedingungen beschrieben werden.  <br/> |Ein Wert vom Typ xs: String  <br/> |
   

