---
title: WeatherData-Element (Outlook Weather Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 84b16927-964e-24be-feaa-e0c11cf062f3
description: Definiert das wetterelement.
ms.openlocfilehash: 2273f7ce6c6a04464ea3da430661c3d6f410cc9f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355076"
---
# <a name="weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="c3429-103">WeatherData-Element (Outlook Weather Information-Schema)</span><span class="sxs-lookup"><span data-stu-id="c3429-103">weatherdata element (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="c3429-104">Definiert das wetterelement.</span><span class="sxs-lookup"><span data-stu-id="c3429-104">Defines the weather element.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c3429-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c3429-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c3429-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="c3429-106">**Element type**</span></span> <br/> ||
|<span data-ttu-id="c3429-107">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="c3429-107">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="c3429-108">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="c3429-108">**Schema file**</span></span> <br/> |<span data-ttu-id="c3429-109">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="c3429-109">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="c3429-110">Definition</span><span class="sxs-lookup"><span data-stu-id="c3429-110">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="c3429-111">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="c3429-111">Elements and attributes</span></span>

<span data-ttu-id="c3429-112">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="c3429-112">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="c3429-113">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c3429-113">Parent elements</span></span>

<span data-ttu-id="c3429-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3429-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c3429-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c3429-115">Child elements</span></span>

|<span data-ttu-id="c3429-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c3429-116">**Element**</span></span>|<span data-ttu-id="c3429-117">**Typ**</span><span class="sxs-lookup"><span data-stu-id="c3429-117">**Type**</span></span>|<span data-ttu-id="c3429-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c3429-118">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="c3429-119">Wetter</span><span class="sxs-lookup"><span data-stu-id="c3429-119">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="c3429-120">weathertype</span><span class="sxs-lookup"><span data-stu-id="c3429-120">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="c3429-121">Gibt die Wetterbedingungen für einen Standort an.</span><span class="sxs-lookup"><span data-stu-id="c3429-121">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="c3429-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="c3429-122">Attributes</span></span>

<span data-ttu-id="c3429-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="c3429-123">None.</span></span>
  

