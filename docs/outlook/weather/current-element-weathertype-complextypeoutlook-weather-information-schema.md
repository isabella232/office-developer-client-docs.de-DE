---
title: Current-Element (weathertype complexType) (Outlook Wetter Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Gibt die aktuellen Wetterbedingungen an.
ms.openlocfilehash: ce92bdd49ee37f939748586c2d63d8a664f664d2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32351471"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>Current-Element (weathertype complexType) (Outlook Wetter Information-Schema)

Gibt die aktuellen Wetterbedingungen an.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[currentType](currenttype-complextype-outlook-weather-information-schema.md) <br/> |
|**Namespace** <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
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
|[Wetter](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weathertype](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die Wetterbedingungen für einen Standort an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|Datum  <br/> |xs: Datum  <br/> |erforderlich  <br/> |Gibt das heutige Datum an.  <br/> |Ein Wert vom Typ xs: Date  <br/> |
|Tag  <br/> |xs: Zeichenfolge  <br/> |Optional  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|feelslike  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt die Temperatur des aktuellen Wetters an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|Feuchtigkeit  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt den aktuellen numerischen Feuchtewert an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|observationpoint  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt an, von wo die aktuellen Wetterinformationen beobachtet werden.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|Beobachtungszeit  <br/> |xs: Zeit  <br/> |erforderlich  <br/> |Gibt an, wann die aktuellen Wetterinformationen unter beobachtet werden.  <br/> |Ein Wert vom Typ xs: Time  <br/> |
|shortday  <br/> |xs: Zeichenfolge  <br/> |Optional  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|skycode  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt einen ganzzahligen Code für die aktuellen Wetterbedingungen an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|skytext  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter an, in denen die aktuellen Wetterbedingungen beschrieben werden.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|Temperatur  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt die aktuelle Temperatur des Standorts an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
|winddisplay  <br/> |xs: Zeichenfolge  <br/> |erforderlich  <br/> |Eine Zeichenfolge, die die aktuellen Windbedingungen beschreibt.  <br/> |Ein Wert vom Typ xs: String  <br/> |
|WindSpeed  <br/> |xs: Integer  <br/> |erforderlich  <br/> |Gibt den aktuellen numerischen Wind Geschwindigkeitswert an.  <br/> |Ein Wert vom Typ xs: Integer  <br/> |
   

