---
title: weatherType complexType (Outlook Weather Location Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f8054fd9-85ba-fcf6-c96d-a54095d5238c
description: Definiert die Parameter für die Wetterbedingungen eines Standorts.
ms.openlocfilehash: 2f5080102379ec250c33983a93a76be7a2a7b8df
ms.sourcegitcommit: a1d9041c20256616c9c183f7d1049142a7ac6991
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59619274"
---
# <a name="weathertype-complextype-outlook-weather-location-schema"></a>weatherType complexType (Outlook Weather Location Schema)

Definiert die Parameter für die Wetterbedingungen eines Standorts.
  
## <a name="type-information"></a>Informationen zum Typ

|||
|:-----|:-----|
|**Namespace** <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|**Schemadatei** <br/> |getweatherlocation.xsd  <br/> |
|**Erweiterungsbasis** <br/> |Keines  <br/> |
   
## <a name="definition"></a>Definition

```XML
       <xs:complexType name="weatherType">
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a>Elemente und Attribute

Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz,** **minOccurs,** **maxOccurs** und **Auswahl,** lesen Sie den Definitionsabschnitt. 
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Typ**|**Erforderlich**|**Beschreibung**|**Mögliche Werte**|
|:-----|:-----|:-----|:-----|:-----|
|weatherlocationcode  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt einen Code an, der dem Speicherort zugeordnet ist, um mehrere Speicherorte mit demselben Namen zu unterscheiden.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
|weatherlocationname  <br/> |xs:string  <br/> |Erforderlich  <br/> |Gibt den Namen des Speicherorts an.  <br/> |Ein Wert vom Typ "xs:string"  <br/> |
   

