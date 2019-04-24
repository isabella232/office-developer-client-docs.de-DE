---
title: Weather-Element (WeatherData-Element) (Outlook Weather Location Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Gibt den Speicherort an, an dem Wetterbedingungen gemeldet werden sollen.
ms.openlocfilehash: f6642b3f477b9fe45ed0e6a43efcd40e21559b7e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355209"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="650f9-103">Weather-Element (WeatherData-Element) (Outlook Weather Location Schema)</span><span class="sxs-lookup"><span data-stu-id="650f9-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="650f9-104">Gibt den Speicherort an, an dem Wetterbedingungen gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="650f9-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="650f9-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="650f9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="650f9-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="650f9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="650f9-107">weathertype</span><span class="sxs-lookup"><span data-stu-id="650f9-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="650f9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="650f9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="650f9-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="650f9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="650f9-110">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="650f9-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="650f9-111">Definition</span><span class="sxs-lookup"><span data-stu-id="650f9-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="650f9-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="650f9-112">Elements and attributes</span></span>

<span data-ttu-id="650f9-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="650f9-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="650f9-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="650f9-114">Parent elements</span></span>

|<span data-ttu-id="650f9-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="650f9-115">**Element**</span></span>|<span data-ttu-id="650f9-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="650f9-116">**Type**</span></span>|<span data-ttu-id="650f9-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="650f9-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="650f9-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="650f9-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="650f9-119">Definiert das wetterelement.</span><span class="sxs-lookup"><span data-stu-id="650f9-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="650f9-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="650f9-120">Child elements</span></span>

<span data-ttu-id="650f9-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="650f9-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="650f9-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="650f9-122">Attributes</span></span>

|<span data-ttu-id="650f9-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="650f9-123">**Attribute**</span></span>|<span data-ttu-id="650f9-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="650f9-124">**Type**</span></span>|<span data-ttu-id="650f9-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="650f9-125">**Required**</span></span>|<span data-ttu-id="650f9-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="650f9-126">**Description**</span></span>|<span data-ttu-id="650f9-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="650f9-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="650f9-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="650f9-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="650f9-129">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="650f9-129">xs:string</span></span>  <br/> |<span data-ttu-id="650f9-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="650f9-130">required</span></span>  <br/> |<span data-ttu-id="650f9-131">Gibt einen Code an, der dem Speicherort zugeordnet ist, um mehrere Speicherorte mit demselben Namen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="650f9-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="650f9-132">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="650f9-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="650f9-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="650f9-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="650f9-134">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="650f9-134">xs:string</span></span>  <br/> |<span data-ttu-id="650f9-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="650f9-135">required</span></span>  <br/> |<span data-ttu-id="650f9-136">Gibt den Namen des Speicherorts an.</span><span class="sxs-lookup"><span data-stu-id="650f9-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="650f9-137">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="650f9-137">A value of the type xs:string</span></span>  <br/> |
   

