---
title: CurrentType complexType (Outlook-Wetter Informations Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Definiert die Parameter für die aktuellen Wetterbedingungen eines Standorts.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540987"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>CurrentType complexType (Outlook-Wetter Informations Schema)

Definiert die Parameter für die aktuellen Wetterbedingungen eines Standorts.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo. xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keine  <br/> |
   
## <a name="definition"></a>Definition

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs: Datum  <br/> |erforderlich  <br/> |Gibt das heutige Datum an.  <br/> |Ein Wert vom Typ xs: Date  <br/> |
|Tag  <br/> |xs: Zeichenfolge  <br/> |Optional  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|feelslike  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt die Temperatur an, wie sich das aktuelle Wetter anfühlt.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|Luftfeuchtigkeits  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt den aktuellen numerischen Feuchtewert an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|observationpoint  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt an, von wo die aktuellen Wetterinformationen beobachtet werden.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|Beobachtungszeit  <br/> |xs: Zeit  <br/> |erforderlich  <br/> |Gibt an, wann die aktuellen Wetterinformationen bei beobachtet werden.  <br/> |Ein Wert vom Typ xs: Time  <br/> |
|shortday  <br/> |xs: Zeichenfolge  <br/> |Optional  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|skycode  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt einen ganzzahligen Code für die aktuellen Wetterbedingungen an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|skytext  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter an, die die aktuellen Wetterbedingungen beschreiben.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|Temperatur  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt die aktuelle Temperatur des Standorts an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|winddisplay  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Eine Zeichenfolge, die die aktuellen Windbedingungen beschreibt.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|WindSpeed  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt den aktuellen numerischen Wind Geschwindigkeitswert an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
   

