---
title: aktuelle Element (WeatherType ComplexType) (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Gibt die aktuelle Wettervorhersage an.
ms.openlocfilehash: 12265c463f0f1bba15c9bf1723cbbea6c505dba9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796090"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>aktuelle Element (WeatherType ComplexType) (Outlook Wetter Informationen-Schema)

Gibt die aktuelle Wettervorhersage an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo.xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="current"      type="currentType">
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
|date  <br/> |xs: Date  <br/> |erforderlich  <br/> |Heutiges Datum angibt.  <br/> |Ein Wert, der den Typ xs: Date  <br/> |
|Tag  <br/> |xs:string  <br/> |Optional  <br/> |Gibt einen Tag für die Planung.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|feelslike  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die Temperatur des wie ist mit das aktuelle Wetter wie an.  <br/> |Der Wert der Type-xs  <br/> |
|Luftfeuchtigkeit  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt den aktuellen Luftfeuchtigkeit numerischen Wert.  <br/> |Der Wert der Type-xs  <br/> |
|observationpoint  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt an, in dem die aktuelle Wetterinformationen aus beobachtet wird.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|observationtime  <br/> |xs: Time  <br/> |erforderlich  <br/> |Gibt an, wenn die aktuelle Wetterinformationen unter beobachtet wird.  <br/> |Ein Wert, der den Typ xs: Time  <br/> |
|shortday  <br/> |xs:string  <br/> |Optional  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|skycode  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt einen ganze Zahl Code für die aktuelle Wettervorhersage.  <br/> |Der Wert der Type-xs  <br/> |
|skytext  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter, die aktuelle Wetterbericht beschreibt.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|Temperatur  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die aktuelle Temperatur des Speicherorts an.  <br/> |Der Wert der Type-xs  <br/> |
|winddisplay  <br/> |xs:string  <br/> |erforderlich  <br/> |Eine Zeichenfolge, die die aktuelle Wind Bedingungen beschreibt.  <br/> |Ein Wert, der den Typ xs:  <br/> |
|windspeed  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt den aktuellen Wert der numerische Wind Geschwindigkeit.  <br/> |Der Wert der Type-xs  <br/> |
   

