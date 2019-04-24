---
title: Weather-Element (WeatherData-Element) (Outlook Wetter Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Gibt die Wetterbedingungen für einen Standort an.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355146"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="a4b80-103">Weather-Element (WeatherData-Element) (Outlook Wetter Information-Schema)</span><span class="sxs-lookup"><span data-stu-id="a4b80-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="a4b80-104">Gibt die Wetterbedingungen für einen Standort an.</span><span class="sxs-lookup"><span data-stu-id="a4b80-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a4b80-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a4b80-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4b80-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="a4b80-106">**Element type**</span></span> <br/> |[<span data-ttu-id="a4b80-107">weathertype</span><span class="sxs-lookup"><span data-stu-id="a4b80-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="a4b80-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="a4b80-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="a4b80-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="a4b80-109">**Schema file**</span></span> <br/> |<span data-ttu-id="a4b80-110">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="a4b80-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="a4b80-111">Definition</span><span class="sxs-lookup"><span data-stu-id="a4b80-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="a4b80-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="a4b80-112">Elements and attributes</span></span>

<span data-ttu-id="a4b80-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="a4b80-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="a4b80-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4b80-114">Parent elements</span></span>

|<span data-ttu-id="a4b80-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4b80-115">**Element**</span></span>|<span data-ttu-id="a4b80-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a4b80-116">**Type**</span></span>|<span data-ttu-id="a4b80-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4b80-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4b80-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="a4b80-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="a4b80-119">Definiert das wetterelement.</span><span class="sxs-lookup"><span data-stu-id="a4b80-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a4b80-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4b80-120">Child elements</span></span>

|<span data-ttu-id="a4b80-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4b80-121">**Element**</span></span>|<span data-ttu-id="a4b80-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a4b80-122">**Type**</span></span>|<span data-ttu-id="a4b80-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4b80-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="a4b80-124">aktuellen</span><span class="sxs-lookup"><span data-stu-id="a4b80-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="a4b80-125">currentType</span><span class="sxs-lookup"><span data-stu-id="a4b80-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="a4b80-126">Gibt die aktuellen Wetterbedingungen an.</span><span class="sxs-lookup"><span data-stu-id="a4b80-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="a4b80-127">Prognose</span><span class="sxs-lookup"><span data-stu-id="a4b80-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="a4b80-128">forecasttype</span><span class="sxs-lookup"><span data-stu-id="a4b80-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="a4b80-129">Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen im Voraus an: heute, morgen, übermorgen.</span><span class="sxs-lookup"><span data-stu-id="a4b80-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="a4b80-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="a4b80-130">Attributes</span></span>

|<span data-ttu-id="a4b80-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a4b80-131">**Attribute**</span></span>|<span data-ttu-id="a4b80-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="a4b80-132">**Type**</span></span>|<span data-ttu-id="a4b80-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="a4b80-133">**Required**</span></span>|<span data-ttu-id="a4b80-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4b80-134">**Description**</span></span>|<span data-ttu-id="a4b80-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="a4b80-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a4b80-136">Attribution</span><span class="sxs-lookup"><span data-stu-id="a4b80-136">attribution</span></span>  <br/> |<span data-ttu-id="a4b80-137">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4b80-137">xs:string</span></span>  <br/> |<span data-ttu-id="a4b80-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a4b80-138">required</span></span>  <br/> |<span data-ttu-id="a4b80-139">Gibt die Quelle der Wetterinformationen an.</span><span class="sxs-lookup"><span data-stu-id="a4b80-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="a4b80-140">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="a4b80-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a4b80-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="a4b80-141">degreetype</span></span>  <br/> |<span data-ttu-id="a4b80-142">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4b80-142">xs:string</span></span>  <br/> |<span data-ttu-id="a4b80-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a4b80-143">required</span></span>  <br/> |<span data-ttu-id="a4b80-144">Gibt die Einheit für die Temperatur des Standorts an, beispielsweise Celsius.</span><span class="sxs-lookup"><span data-stu-id="a4b80-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="a4b80-145">C, F</span><span class="sxs-lookup"><span data-stu-id="a4b80-145">C, F</span></span>  <br/> |
|<span data-ttu-id="a4b80-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="a4b80-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="a4b80-147">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4b80-147">xs:string</span></span>  <br/> |<span data-ttu-id="a4b80-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a4b80-148">required</span></span>  <br/> |<span data-ttu-id="a4b80-149">Gibt die URL des Bilds für den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="a4b80-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="a4b80-150">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="a4b80-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a4b80-151">TimeZone</span><span class="sxs-lookup"><span data-stu-id="a4b80-151">timezone</span></span>  <br/> |<span data-ttu-id="a4b80-152">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="a4b80-152">xs:integer</span></span>  <br/> |<span data-ttu-id="a4b80-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a4b80-153">required</span></span>  <br/> |<span data-ttu-id="a4b80-154">Gibt den GMT-Offset an.</span><span class="sxs-lookup"><span data-stu-id="a4b80-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="a4b80-155">Ein Wert zwischen-11 und 12 inklusive</span><span class="sxs-lookup"><span data-stu-id="a4b80-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="a4b80-156">url</span><span class="sxs-lookup"><span data-stu-id="a4b80-156">url</span></span>  <br/> |<span data-ttu-id="a4b80-157">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4b80-157">xs:string</span></span>  <br/> |<span data-ttu-id="a4b80-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a4b80-158">required</span></span>  <br/> |<span data-ttu-id="a4b80-159">Gibt die URL für die Webseite des Wetter Diensts an, die Wetterinformationen für den angegebenen Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="a4b80-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="a4b80-160">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="a4b80-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a4b80-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="a4b80-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="a4b80-162">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4b80-162">xs:string</span></span>  <br/> |<span data-ttu-id="a4b80-163">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a4b80-163">required</span></span>  <br/> |<span data-ttu-id="a4b80-164">Gibt den Code an, der dem Speicherort zugeordnet ist, an dem mehrere Standorte mit demselben Namen unterschieden werden.</span><span class="sxs-lookup"><span data-stu-id="a4b80-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="a4b80-165">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="a4b80-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="a4b80-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="a4b80-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="a4b80-167">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="a4b80-167">xs:string</span></span>  <br/> |<span data-ttu-id="a4b80-168">erforderlich</span><span class="sxs-lookup"><span data-stu-id="a4b80-168">required</span></span>  <br/> |<span data-ttu-id="a4b80-169">Gibt den Namen des Speicherorts an, der im Dropdown-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a4b80-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="a4b80-170">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="a4b80-170">A value of the type xs:string</span></span>  <br/> |
   

