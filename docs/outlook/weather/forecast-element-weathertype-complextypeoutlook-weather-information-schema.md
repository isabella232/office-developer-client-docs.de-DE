---
title: forecast-Element (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen vor, einschließlich heute: Heute, Morgen, Tag nach Morgen.'
ms.openlocfilehash: 51a4df8c1ee711cb10db70d631ef93edb7d1c356
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59549637"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a>forecast-Element (weatherType complexType) (Outlook Weather Information Schema)

Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen vor, einschließlich heute: Heute, Morgen, Tag nach Morgen.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Wetter](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die Wetterbedingungen eines Standorts an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |erforderlich  <br/> |Gibt das Datum für die Prognose an.  <br/> |Ein Wert vom Typ "xs:date"  <br/> |
|Tag  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Hoch  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die prognostizierte höchste Temperatur an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Niedrig  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die prognostizierte niedrigste Temperatur an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|precip  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt die prozentuale Wahrscheinlichkeit von Käufen an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|shortday  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt einen Code für die prognostizierten Bedingungen an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt ein bis zwei Wörter an, die die prognostizierten Bedingungen beschreiben.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
   

