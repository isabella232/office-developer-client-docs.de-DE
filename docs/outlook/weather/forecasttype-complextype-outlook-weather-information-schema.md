---
title: ForecastType ComplexType (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Definiert die Parameter für die Vorhersage Wetter Formatierungen einen Speicherort an.
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796091"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>ForecastType ComplexType (Outlook Wetter Informationen-Schema)

Definiert die Parameter für die Vorhersage Wetter Formatierungen einen Speicherort an.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt. 
  
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
   

