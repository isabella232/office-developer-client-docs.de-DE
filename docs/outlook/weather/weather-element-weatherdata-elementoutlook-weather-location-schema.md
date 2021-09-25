---
title: weather-Element (weatherdata-Element) (Outlook Weather Location Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Gibt den Ort an, an dem Wetter gemeldet werden soll.
ms.openlocfilehash: 89b384579e1bfce38f75f573c642323db9d60cb5
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59570750"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a>weather-Element (weatherdata-Element) (Outlook Weather Location Schema)

Gibt den Ort an, an dem Wetter gemeldet werden soll.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|**Elementtyp** <br/> |[weatherType](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Schemadatei** <br/> |getweatherlocation.xsd  <br/> |
   
## <a name="definition"></a>Definition

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Typ**|**Beschreibung**|
|:-----|:-----|:-----|
|[Wetterdaten](weatherdata-element-outlook-weather-location-schema.md) <br/> ||Definiert das Wetterelement.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt einen Code an, der dem Speicherort zugeordnet ist, um mehrere Speicherorte mit demselben Namen zu unterscheiden.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |erforderlich  <br/> |Gibt den Namen des Speicherorts an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
   

