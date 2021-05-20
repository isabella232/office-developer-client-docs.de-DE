---
title: forecastType complexType (Outlook Wetterinformationsschema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Definiert die Parameter zu den Wettervorhersagebedingungen eines Standorts.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540952"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a>forecastType complexType (Outlook Wetterinformationsschema)

Definiert die Parameter zu den Wettervorhersagebedingungen eines Standorts.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |getweatherinfo.xsd  <br/> |
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |erforderlich  <br/> |Gibt das Datum für die Planung an.  <br/> |Ein Wert vom Typ xs:date  <br/> |
|day  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ xs:string  <br/> |
|high  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die vorhergesagte höchste Temperatur an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|low  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die vorhergesagte niedrigste Temperatur an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|precip  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die prozentuale Wahrscheinlichkeit der Verfällung an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|shortday  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ xs:string  <br/> |
|skycodeday  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt einen Code für die vorhergesagten Bedingungen an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|skytextday  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter an, die die prognostizierten Bedingungen beschreiben.  <br/> |Ein Wert vom Typ xs:string  <br/> |
   

