---
title: WeatherData-Element (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Definiert das Wetter-Element.
ms.openlocfilehash: 689c390f621d18f680de9635c3d82711300f8030
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796199"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="a382e-103">WeatherData-Element (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="a382e-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="a382e-104">Definiert das Wetter-Element.</span><span class="sxs-lookup"><span data-stu-id="a382e-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a382e-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a382e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a382e-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="a382e-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="a382e-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a382e-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="a382e-108">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a382e-108">**Schema file**</span></span> <br/> |<span data-ttu-id="a382e-109">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="a382e-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a382e-110">Definition</span><span class="sxs-lookup"><span data-stu-id="a382e-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType">
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="a382e-111">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a382e-111">Elements and attributes</span></span>

<span data-ttu-id="a382e-112">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="a382e-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a382e-113">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a382e-113">Parent elements</span></span>

<span data-ttu-id="a382e-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="a382e-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a382e-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a382e-115">Child elements</span></span>

|<span data-ttu-id="a382e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="a382e-116">**Element**</span></span>|<span data-ttu-id="a382e-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a382e-117">**Type**</span></span>|<span data-ttu-id="a382e-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a382e-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a382e-119">Wetterbericht</span><span class="sxs-lookup"><span data-stu-id="a382e-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="a382e-120">weatherType</span><span class="sxs-lookup"><span data-stu-id="a382e-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="a382e-121">Gibt die Wetterbedingungen einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="a382e-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a382e-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="a382e-122">Attributes</span></span>

<span data-ttu-id="a382e-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="a382e-123">None.</span></span>
  

