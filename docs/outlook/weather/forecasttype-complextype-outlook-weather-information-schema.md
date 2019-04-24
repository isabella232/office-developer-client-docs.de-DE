---
title: forecasttype complexType (Outlook Wetter Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Definiert die Parameter für die Wettervorhersage für einen Standort.
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361145"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecasttype complexType (Outlook Wetter Information-Schema)

Definiert die Parameter für die Wettervorhersage für einen Standort.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo. xsd  <br/> |
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

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
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
   

