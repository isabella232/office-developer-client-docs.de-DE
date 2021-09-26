---
title: forecastType complexType (Outlook Wetterinformationsschema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Definiert die Parameter für die wettervorhersagen Wetterbedingungen eines Standorts.
ms.openlocfilehash: 815f7131fc4869a7015c0fee15d0e8d68d0905dc
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619316"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (Outlook Wetterinformationsschema)

Definiert die Parameter für die wettervorhersagen Wetterbedingungen eines Standorts.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |getweatherinfo.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |erforderlich  <br/> |Gibt das Datum für die Prognose an.  <br/> |Ein Wert vom Typ "xs:date"  <br/> |
|Tag  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Hoch  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt die prognostizierte höchste Temperatur an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Niedrig  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die prognostizierte niedrigste Temperatur an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|precip  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die prozentuale Wahrscheinlichkeit von Käufen an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|shortday  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt einen Code für die prognostizierten Bedingungen an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt ein bis zwei Wörter an, die die prognostizierten Bedingungen beschreiben.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
   

