---
title: currentType complexType (Outlook Weather Information Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Definiert die Parameter zu den aktuellen Wetterbedingungen eines Standorts.
ms.openlocfilehash: 42ee25ed01bf748e40b72d4ef9c0c6c62e72af09
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619365"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a>currentType complexType (Outlook Weather Information Schema)

Definiert die Parameter zu den aktuellen Wetterbedingungen eines Standorts.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|**Schemadatei** <br/> |getweatherinfo.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
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

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|date  <br/> |xs:date  <br/> |erforderlich  <br/> |Gibt das heutige Datum an.  <br/> |Ein Wert vom Typ "xs:date"  <br/> |
|Tag  <br/> |xs:string  <br/> |Optional  <br/> |Gibt einen Tag für die Prognose an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|"feelslike"  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt die Temperatur des aktuellen Wetters an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Feuchtigkeit  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt den aktuellen numerischen Feuchtigkeitswert an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Beobachtungspunkt  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt an, von wo die aktuellen Wetterinformationen beobachtet werden.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Beobachtungszeit  <br/> |xs:time  <br/> |Erforderlich  <br/> |Gibt an, wann die aktuellen Wetterinformationen beobachtet werden.  <br/> |Ein Wert vom Typ xs:time  <br/> |
|shortday  <br/> |xs:string  <br/> |Optional  <br/> |Gibt einen Tag in abgekürzter Form an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|skycode  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt einen ganzzahligen Code für die aktuellen Wetterbedingungen an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|Skytext  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt ein bis zwei Wörter zur Beschreibung der aktuellen Wetterbedingungen an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Temperatur  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt die aktuelle Temperatur der Position an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
|winddisplay  <br/> |xs:string  <br/> |Erforderlich  <br/> |Eine Zeichenfolge, die die aktuellen Windbedingungen beschreibt.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|Windgeschwindigkeit  <br/> |xs:integer  <br/> |Erforderlich  <br/> |Gibt den aktuellen numerischen Windgeschwindigkeitswert an.  <br/> |Ein Wert vom Typ xs:integer  <br/> |
   

