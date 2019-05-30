---
title: WeatherData-Element (Outlook-Wetter Standort Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Definiert das Weather-Element.
ms.openlocfilehash: 65dd0ee5686fb773479c8b63a43f51bff67fd2f7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540931"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="bf0b6-103">WeatherData-Element (Outlook-Wetter Standort Schema)</span><span class="sxs-lookup"><span data-stu-id="bf0b6-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="bf0b6-104">Definiert das Weather-Element.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="bf0b6-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="bf0b6-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bf0b6-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="bf0b6-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="bf0b6-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="bf0b6-107">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="bf0b6-108">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="bf0b6-108">**Schema file**</span></span> <br/> |<span data-ttu-id="bf0b6-109">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="bf0b6-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="bf0b6-110">Definition</span><span class="sxs-lookup"><span data-stu-id="bf0b6-110">Definition</span></span>

```XML
    <xs:element name="weatherdata"
    >
          <xs:complexType>
          <xs:sequence>
    <xs:element name="weather"
     type="weatherType" maxOccurs="unbounded"
      >
    </xs:element>
    
      </xs:sequence>
      </xs:complexType>
    </xs:element>
    
```

## <a name="elements-and-attributes"></a><span data-ttu-id="bf0b6-111">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="bf0b6-111">Elements and attributes</span></span>

<span data-ttu-id="bf0b6-112">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="bf0b6-113">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bf0b6-113">Parent elements</span></span>

<span data-ttu-id="bf0b6-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="bf0b6-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="bf0b6-115">Child elements</span></span>

|<span data-ttu-id="bf0b6-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="bf0b6-116">**Element**</span></span>|<span data-ttu-id="bf0b6-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="bf0b6-117">**Type**</span></span>|<span data-ttu-id="bf0b6-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf0b6-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="bf0b6-119">Wetter</span><span class="sxs-lookup"><span data-stu-id="bf0b6-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="bf0b6-120">weathertype</span><span class="sxs-lookup"><span data-stu-id="bf0b6-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="bf0b6-121">Gibt den Ort an, an dem das Wetter gemeldet werden soll.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="bf0b6-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="bf0b6-122">Attributes</span></span>

<span data-ttu-id="bf0b6-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="bf0b6-123">None.</span></span>
  

