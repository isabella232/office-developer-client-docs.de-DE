---
title: aktuelles Element (weatherType complexType) (Outlook Wetterinformationsschema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Gibt die aktuellen Wetterbedingungen an.
ms.openlocfilehash: 1303212da1336112599ae5328498cca0d4ab5f89
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541008"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>aktuelles Element (weatherType complexType) (Outlook Wetterinformationsschema)

Gibt die aktuellen Wetterbedingungen an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |getweatherinfo.xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="current"      type="currentType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Wetter](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die Wetterbedingungen eines Standorts an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |erforderlich  <br/> |Gibt das heutige Datum an.  <br/> |Ein Wert vom Typ xs:date  <br/> |
|day  <br/> |xs:string  <br/> |Optional  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ xs:string  <br/> |
|feelslike  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die Temperatur an, wie sich das aktuelle Wetter anfühlt.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Feuchtigkeit  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt den aktuellen numerischen Feuchtigkeitswert an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|observationpoint  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt an, wo die aktuellen Wetterinformationen beobachtet werden.  <br/> |Ein Wert vom Typ xs:string  <br/> |
|observationtime  <br/> |xs:time  <br/> |erforderlich  <br/> |Gibt an, wann die aktuellen Wetterinformationen beobachtet werden.  <br/> |Ein Wert vom Typ xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |Optional  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ xs:string  <br/> |
|skycode  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt einen ganzzahligen Code für die aktuellen Wetterbedingungen an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|skytext  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter an, die aktuelle Wetterbedingungen beschreiben.  <br/> |Ein Wert vom Typ xs:string  <br/> |
|temperatur  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die aktuelle Temperatur des Standorts an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |erforderlich  <br/> |Eine Zeichenfolge, die die aktuellen Windbedingungen beschreibt.  <br/> |Ein Wert vom Typ xs:string  <br/> |
|windspeed  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt den aktuellen numerischen Windgeschwindigkeitswert an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
   

