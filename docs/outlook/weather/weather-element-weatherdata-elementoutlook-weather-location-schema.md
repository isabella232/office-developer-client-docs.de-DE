---
title: Weather-Element (WeatherData-Element) (Outlook-Wetter Standort Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1127956a-37aa-c39e-60b4-343dcc4ead82
description: Gibt den Ort an, an dem das Wetter gemeldet werden soll.
ms.openlocfilehash: a907fb9df02d88d317a73e409ea8738273eb2cb1
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539012"
---
# <a name="weather-element-weatherdata-element-outlook-weather-location-schema"></a><span data-ttu-id="6fed8-103">Weather-Element (WeatherData-Element) (Outlook-Wetter Standort Schema)</span><span class="sxs-lookup"><span data-stu-id="6fed8-103">weather element (weatherdata element) (Outlook Weather Location Schema)</span></span>

<span data-ttu-id="6fed8-104">Gibt den Ort an, an dem das Wetter gemeldet werden soll.</span><span class="sxs-lookup"><span data-stu-id="6fed8-104">Specifies the location to report weather on.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="6fed8-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="6fed8-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6fed8-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="6fed8-106">**Element type**</span></span> <br/> |[<span data-ttu-id="6fed8-107">weathertype</span><span class="sxs-lookup"><span data-stu-id="6fed8-107">weatherType</span></span>](weathertype-complextype-outlook-weather-location-schema.md) <br/> |
|<span data-ttu-id="6fed8-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6fed8-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherlocation.xsd  <br/> |
|<span data-ttu-id="6fed8-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6fed8-109">**Schema file**</span></span> <br/> |<span data-ttu-id="6fed8-110">getweatherlocation. xsd</span><span class="sxs-lookup"><span data-stu-id="6fed8-110">getweatherlocation.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6fed8-111">Definition</span><span class="sxs-lookup"><span data-stu-id="6fed8-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType" maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="6fed8-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6fed8-112">Elements and attributes</span></span>

<span data-ttu-id="6fed8-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6fed8-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="6fed8-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fed8-114">Parent elements</span></span>

|<span data-ttu-id="6fed8-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="6fed8-115">**Element**</span></span>|<span data-ttu-id="6fed8-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6fed8-116">**Type**</span></span>|<span data-ttu-id="6fed8-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fed8-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="6fed8-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="6fed8-118">weatherdata</span></span>](weatherdata-element-outlook-weather-location-schema.md) <br/> ||<span data-ttu-id="6fed8-119">Definiert das Weather-Element.</span><span class="sxs-lookup"><span data-stu-id="6fed8-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="6fed8-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6fed8-120">Child elements</span></span>

<span data-ttu-id="6fed8-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="6fed8-121">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6fed8-122">Attribute</span><span class="sxs-lookup"><span data-stu-id="6fed8-122">Attributes</span></span>

|<span data-ttu-id="6fed8-123">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6fed8-123">**Attribute**</span></span>|<span data-ttu-id="6fed8-124">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6fed8-124">**Type**</span></span>|<span data-ttu-id="6fed8-125">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6fed8-125">**Required**</span></span>|<span data-ttu-id="6fed8-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6fed8-126">**Description**</span></span>|<span data-ttu-id="6fed8-127">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6fed8-127">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6fed8-128">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="6fed8-128">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="6fed8-129">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6fed8-129">xs:string</span></span>  <br/> |<span data-ttu-id="6fed8-130">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6fed8-130">required</span></span>  <br/> |<span data-ttu-id="6fed8-131">Gibt einen Code an, der dem Speicherort zugeordnet ist, um mehrere Standorte mit dem gleichen Namen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="6fed8-131">Specifies a code that is associated with the location to distinguish multiple locations with the same name.</span></span>  <br/> |<span data-ttu-id="6fed8-132">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="6fed8-132">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6fed8-133">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="6fed8-133">weatherlocationname</span></span>  <br/> |<span data-ttu-id="6fed8-134">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="6fed8-134">xs:string</span></span>  <br/> |<span data-ttu-id="6fed8-135">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6fed8-135">required</span></span>  <br/> |<span data-ttu-id="6fed8-136">Gibt den Namen des Speicherorts an.</span><span class="sxs-lookup"><span data-stu-id="6fed8-136">Specifies the name of the location.</span></span>  <br/> |<span data-ttu-id="6fed8-137">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="6fed8-137">A value of the type xs:string</span></span>  <br/> |
   

