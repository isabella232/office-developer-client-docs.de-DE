---
title: weathertype complexType (Outlook Wetter Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Gibt die Wetterbedingungen für einen Standort an.
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355041"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a>weathertype complexType (Outlook Wetter Information-Schema)

Gibt die Wetterbedingungen für einen Standort an.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo. xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
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
   

