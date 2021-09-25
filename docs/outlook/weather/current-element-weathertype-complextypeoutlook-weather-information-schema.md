---
title: current-Element (weatherType complexType) (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d592a396-f935-c44c-409f-b849c327cfbd
description: Gibt die aktuellen Wetterbedingungen an.
ms.openlocfilehash: 616c891eb2b941e6376b2845e0844f0b43eb39e1
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59604033"
---
# <a name="current-element-weathertype-complextype-outlook-weather-information-schema"></a>current-Element (weatherType complexType) (Outlook Weather Information Schema)

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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Wetter](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[weatherType](weathertype-complextype-outlook-weather-information-schema.md) <br/> |Gibt die Wetterbedingungen eines Standorts an.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |erforderlich  <br/> |Gibt das heutige Datum an.  <br/> |Ein Wert vom Typ "xs:date"  <br/> |
|Tag  <br/> |xs:string  <br/> |Optional  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|"feelslike"  <br/> |xs:integer  <br/> |erforderlich  <br/> |Gibt die Temperatur des aktuellen Wetters an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Feuchtigkeit  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt den aktuellen numerischen Feuchtigkeitswert an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Beobachtungspunkt  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt an, von wo die aktuellen Wetterinformationen beobachtet werden.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Beobachtungszeit  <br/> |xs:time  <br/> |Erforderlich  <br/> |Gibt an, wann die aktuellen Wetterinformationen beobachtet werden.  <br/> |Ein Wert vom Typ xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |Optional  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|skycode  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt einen ganzzahligen Code für die aktuellen Wetterbedingungen an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Skytext  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter zur Beschreibung der aktuellen Wetterbedingungen an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Temperatur  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt die aktuelle Temperatur der Position an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |Erforderlich  <br/> |Eine Zeichenfolge, die die aktuellen Windbedingungen beschreibt.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Windgeschwindigkeit  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt den aktuellen numerischen Windgeschwindigkeitswert an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
   

