---
title: Current-Element (weathertype complexType) (Outlook-Wetter Informations Schema)
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
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>Current-Element (weathertype complexType) (Outlook-Wetter Informations Schema)

Gibt die aktuellen Wetterbedingungen an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |GetWeatherInfo. xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="current"      type="currentType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Wetter](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weathertype](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die Wetterbedingungen eines Standorts an.  <br/> |
   
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
   

