---
title: Weather-Element (WeatherData-Element) (Outlook-Wetter Informations Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Gibt die Wetterbedingungen eines Standorts an.
ms.openlocfilehash: 18669dfc4636c28e03a582bc0c8df512aa38a4e4
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541267"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="97b0d-103">Weather-Element (WeatherData-Element) (Outlook-Wetter Informations Schema)</span><span class="sxs-lookup"><span data-stu-id="97b0d-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="97b0d-104">Gibt die Wetterbedingungen eines Standorts an.</span><span class="sxs-lookup"><span data-stu-id="97b0d-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="97b0d-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="97b0d-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97b0d-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="97b0d-106">**Element type**</span></span> <br/> |[<span data-ttu-id="97b0d-107">weathertype</span><span class="sxs-lookup"><span data-stu-id="97b0d-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="97b0d-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="97b0d-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="97b0d-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="97b0d-109">**Schema file**</span></span> <br/> |<span data-ttu-id="97b0d-110">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="97b0d-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="97b0d-111">Definition</span><span class="sxs-lookup"><span data-stu-id="97b0d-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="97b0d-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="97b0d-112">Elements and attributes</span></span>

<span data-ttu-id="97b0d-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="97b0d-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="97b0d-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97b0d-114">Parent elements</span></span>

|<span data-ttu-id="97b0d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="97b0d-115">**Element**</span></span>|<span data-ttu-id="97b0d-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="97b0d-116">**Type**</span></span>|<span data-ttu-id="97b0d-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97b0d-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="97b0d-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="97b0d-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="97b0d-119">Definiert das Weather-Element.</span><span class="sxs-lookup"><span data-stu-id="97b0d-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="97b0d-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97b0d-120">Child elements</span></span>

|<span data-ttu-id="97b0d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="97b0d-121">**Element**</span></span>|<span data-ttu-id="97b0d-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="97b0d-122">**Type**</span></span>|<span data-ttu-id="97b0d-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97b0d-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="97b0d-124">aktuellen</span><span class="sxs-lookup"><span data-stu-id="97b0d-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="97b0d-125">currentType</span><span class="sxs-lookup"><span data-stu-id="97b0d-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="97b0d-126">Gibt die aktuellen Wetterbedingungen an.</span><span class="sxs-lookup"><span data-stu-id="97b0d-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="97b0d-127">Prognose</span><span class="sxs-lookup"><span data-stu-id="97b0d-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="97b0d-128">forecasttype</span><span class="sxs-lookup"><span data-stu-id="97b0d-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="97b0d-129">Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: heute, morgen, Tag nach morgen.</span><span class="sxs-lookup"><span data-stu-id="97b0d-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="97b0d-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="97b0d-130">Attributes</span></span>

|<span data-ttu-id="97b0d-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="97b0d-131">**Attribute**</span></span>|<span data-ttu-id="97b0d-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="97b0d-132">**Type**</span></span>|<span data-ttu-id="97b0d-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="97b0d-133">**Required**</span></span>|<span data-ttu-id="97b0d-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97b0d-134">**Description**</span></span>|<span data-ttu-id="97b0d-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="97b0d-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="97b0d-136">Attribution</span><span class="sxs-lookup"><span data-stu-id="97b0d-136">attribution</span></span>  <br/> |<span data-ttu-id="97b0d-137">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="97b0d-137">xs:string</span></span>  <br/> |<span data-ttu-id="97b0d-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b0d-138">required</span></span>  <br/> |<span data-ttu-id="97b0d-139">Gibt die Quelle der Wetterinformationen an.</span><span class="sxs-lookup"><span data-stu-id="97b0d-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="97b0d-140">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="97b0d-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="97b0d-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="97b0d-141">degreetype</span></span>  <br/> |<span data-ttu-id="97b0d-142">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="97b0d-142">xs:string</span></span>  <br/> |<span data-ttu-id="97b0d-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b0d-143">required</span></span>  <br/> |<span data-ttu-id="97b0d-144">Gibt die Einheit für die Temperatur des Standorts an, beispielsweise Celsius.</span><span class="sxs-lookup"><span data-stu-id="97b0d-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="97b0d-145">C, F</span><span class="sxs-lookup"><span data-stu-id="97b0d-145">C, F</span></span>  <br/> |
|<span data-ttu-id="97b0d-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="97b0d-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="97b0d-147">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="97b0d-147">xs:string</span></span>  <br/> |<span data-ttu-id="97b0d-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b0d-148">required</span></span>  <br/> |<span data-ttu-id="97b0d-149">Gibt die URL des Bilds für den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="97b0d-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="97b0d-150">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="97b0d-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="97b0d-151">TimeZone</span><span class="sxs-lookup"><span data-stu-id="97b0d-151">timezone</span></span>  <br/> |<span data-ttu-id="97b0d-152">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="97b0d-152">xs:integer</span></span>  <br/> |<span data-ttu-id="97b0d-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b0d-153">required</span></span>  <br/> |<span data-ttu-id="97b0d-154">Gibt den GMT-Offset an.</span><span class="sxs-lookup"><span data-stu-id="97b0d-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="97b0d-155">Ein Wert zwischen-11 und 12 inklusive</span><span class="sxs-lookup"><span data-stu-id="97b0d-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="97b0d-156">url</span><span class="sxs-lookup"><span data-stu-id="97b0d-156">url</span></span>  <br/> |<span data-ttu-id="97b0d-157">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="97b0d-157">xs:string</span></span>  <br/> |<span data-ttu-id="97b0d-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b0d-158">required</span></span>  <br/> |<span data-ttu-id="97b0d-159">Gibt die URL für die Webseite des Wetter Diensts an, die Wetterinformationen für den angegebenen Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="97b0d-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="97b0d-160">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="97b0d-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="97b0d-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="97b0d-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="97b0d-162">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="97b0d-162">xs:string</span></span>  <br/> |<span data-ttu-id="97b0d-163">erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b0d-163">required</span></span>  <br/> |<span data-ttu-id="97b0d-164">Gibt den Code an, der dem Speicherort zugeordnet ist, der verwendet wird, um mehrere Standorte mit demselben Namen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="97b0d-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="97b0d-165">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="97b0d-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="97b0d-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="97b0d-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="97b0d-167">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="97b0d-167">xs:string</span></span>  <br/> |<span data-ttu-id="97b0d-168">erforderlich</span><span class="sxs-lookup"><span data-stu-id="97b0d-168">required</span></span>  <br/> |<span data-ttu-id="97b0d-169">Gibt den Namen des Speicherorts an, der im Dropdown-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="97b0d-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="97b0d-170">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="97b0d-170">A value of the type xs:string</span></span>  <br/> |
   

