---
title: weatherType complexType (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Gibt die Wetterbedingungen eines Standorts an.
ms.openlocfilehash: 56d4364e521cadd9a3a7062a0caf2cb82dcbd079
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59616187"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a>weatherType complexType (Outlook Weather Information Schema)

Gibt die Wetterbedingungen eines Standorts an.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |getweatherinfo.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Aktuellen](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die aktuellen Wetterbedingungen an.  <br/> |
|[Prognose](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[forecastType](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen vor, einschließlich heute: Heute, Morgen, Tag nach Morgen.  <br/> |
   
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Attribution  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt die Quelle der Wetterinformationen an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Grad  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt die Einheit für die Temperatur des Standorts an, z. B. Celsius.  <br/> |C, F  <br/> |
|imagerelativeurl  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt die URL des Bilds für den Speicherort an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Zeitzone  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt den GMT-Offset an.  <br/> |Ein Wert zwischen -11 und einschließlich 12  <br/> |
|url  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt die URL für die Webseite des Wetterdiensts an, die Wetterinformationen für den angegebenen Ort enthält.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|weatherlocationcode  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt den Code an, der dem Speicherort zugeordnet ist, der verwendet wird, um mehrere Speicherorte mit demselben Namen zu unterscheiden.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt den Namen des Speicherorts an, der im Dropdownsteuerelement angezeigt wird.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
   

