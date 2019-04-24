---
title: WeatherData-Element (Outlook Weather Location Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 14e0c469-31dc-fbe2-0d45-da602df04f13
description: Definiert das wetterelement.
ms.openlocfilehash: ade57264fab592d3314aa9a3376e129a5f3719c0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355034"
---
# <a name="weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="1b16d-103">WeatherData-Element (Outlook Weather Location Schema)</span><span class="sxs-lookup"><span data-stu-id="1b16d-103">weatherdata element (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="1b16d-104">Definiert das wetterelement.</span><span class="sxs-lookup"><span data-stu-id="1b16d-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1b16d-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1b16d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1b16d-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1b16d-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="1b16d-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1b16d-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="1b16d-108">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1b16d-108">**Schema file**</span></span> <br/> |<span data-ttu-id="1b16d-109">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="1b16d-109">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1b16d-110">Definition</span><span class="sxs-lookup"><span data-stu-id="1b16d-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="1b16d-111">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1b16d-111">Elements and attributes</span></span>

<span data-ttu-id="1b16d-112">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="1b16d-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1b16d-113">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b16d-113">Parent elements</span></span>

<span data-ttu-id="1b16d-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b16d-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1b16d-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1b16d-115">Child elements</span></span>

|<span data-ttu-id="1b16d-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1b16d-116">**Element**</span></span>|<span data-ttu-id="1b16d-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1b16d-117">**Type**</span></span>|<span data-ttu-id="1b16d-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1b16d-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1b16d-119">Wetter</span><span class="sxs-lookup"><span data-stu-id="1b16d-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-location-schema.md) <br/> |[<span data-ttu-id="1b16d-120">weathertype</span><span class="sxs-lookup"><span data-stu-id="1b16d-120">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |<span data-ttu-id="1b16d-121">Gibt den Speicherort an, an dem Wetterbedingungen gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b16d-121">Specifies the location to report weather on.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="1b16d-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="1b16d-122">Attributes</span></span>

<span data-ttu-id="1b16d-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="1b16d-123">None.</span></span>
  

