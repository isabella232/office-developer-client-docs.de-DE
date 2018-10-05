---
title: Wetter-Element (Weatherdata-Element) (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: de3c35ef-84a3-b991-7c98-3eca720c9ba0
description: Gibt die Wetterbedingungen einen Speicherort an.
ms.openlocfilehash: 19e6669d51aa38d10587c6334aef0409f31baf58
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390660"
---
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="959c1-103">Wetter-Element (Weatherdata-Element) (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="959c1-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="959c1-104">Gibt die Wetterbedingungen einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="959c1-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="959c1-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="959c1-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="959c1-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="959c1-106">**Element type**</span></span> <br/> |[<span data-ttu-id="959c1-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="959c1-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="959c1-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="959c1-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="959c1-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="959c1-109">**Schema file**</span></span> <br/> |<span data-ttu-id="959c1-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="959c1-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="959c1-111">Definition</span><span class="sxs-lookup"><span data-stu-id="959c1-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="959c1-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="959c1-112">Elements and attributes</span></span>

<span data-ttu-id="959c1-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="959c1-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="959c1-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="959c1-114">Parent elements</span></span>

|<span data-ttu-id="959c1-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="959c1-115">**Element**</span></span>|<span data-ttu-id="959c1-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="959c1-116">**Type**</span></span>|<span data-ttu-id="959c1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="959c1-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="959c1-118">WeatherData</span><span class="sxs-lookup"><span data-stu-id="959c1-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="959c1-119">Definiert das Wetter-Element.</span><span class="sxs-lookup"><span data-stu-id="959c1-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="959c1-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="959c1-120">Child elements</span></span>

|<span data-ttu-id="959c1-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="959c1-121">**Element**</span></span>|<span data-ttu-id="959c1-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="959c1-122">**Type**</span></span>|<span data-ttu-id="959c1-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="959c1-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="959c1-124">aktuelle</span><span class="sxs-lookup"><span data-stu-id="959c1-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="959c1-125">currentType</span><span class="sxs-lookup"><span data-stu-id="959c1-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="959c1-126">Gibt die aktuelle Wettervorhersage an.</span><span class="sxs-lookup"><span data-stu-id="959c1-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="959c1-127">Planung</span><span class="sxs-lookup"><span data-stu-id="959c1-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="959c1-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="959c1-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="959c1-129">Gibt an, die Wetterbedingungen zukünftigen mindestens drei Tage im Voraus einschließlich heute: heute, morgen, übermorgen.</span><span class="sxs-lookup"><span data-stu-id="959c1-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="959c1-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="959c1-130">Attributes</span></span>

|<span data-ttu-id="959c1-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="959c1-131">**Attribute**</span></span>|<span data-ttu-id="959c1-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="959c1-132">**Type**</span></span>|<span data-ttu-id="959c1-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="959c1-133">**Required**</span></span>|<span data-ttu-id="959c1-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="959c1-134">**Description**</span></span>|<span data-ttu-id="959c1-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="959c1-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="959c1-136">Zuweisung</span><span class="sxs-lookup"><span data-stu-id="959c1-136">attribution</span></span>  <br/> |<span data-ttu-id="959c1-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="959c1-137">xs:string</span></span>  <br/> |<span data-ttu-id="959c1-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="959c1-138">required</span></span>  <br/> |<span data-ttu-id="959c1-139">Gibt die Quelle der Wetterinformationen.</span><span class="sxs-lookup"><span data-stu-id="959c1-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="959c1-140">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="959c1-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="959c1-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="959c1-141">degreetype</span></span>  <br/> |<span data-ttu-id="959c1-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="959c1-142">xs:string</span></span>  <br/> |<span data-ttu-id="959c1-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="959c1-143">required</span></span>  <br/> |<span data-ttu-id="959c1-144">Gibt die Maßeinheit für die Temperatur des Speicherorts beispielsweise Celsius.</span><span class="sxs-lookup"><span data-stu-id="959c1-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="959c1-145">C, F</span><span class="sxs-lookup"><span data-stu-id="959c1-145">C, F</span></span>  <br/> |
|<span data-ttu-id="959c1-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="959c1-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="959c1-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="959c1-147">xs:string</span></span>  <br/> |<span data-ttu-id="959c1-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="959c1-148">required</span></span>  <br/> |<span data-ttu-id="959c1-149">Gibt die URL des Bilds für den Speicherort.</span><span class="sxs-lookup"><span data-stu-id="959c1-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="959c1-150">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="959c1-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="959c1-151">Zeitzone</span><span class="sxs-lookup"><span data-stu-id="959c1-151">timezone</span></span>  <br/> |<span data-ttu-id="959c1-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="959c1-152">xs:integer</span></span>  <br/> |<span data-ttu-id="959c1-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="959c1-153">required</span></span>  <br/> |<span data-ttu-id="959c1-154">Gibt den Offset GMT.</span><span class="sxs-lookup"><span data-stu-id="959c1-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="959c1-155">Ein Wert zwischen-11 und 12 inklusive</span><span class="sxs-lookup"><span data-stu-id="959c1-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="959c1-156">url</span><span class="sxs-lookup"><span data-stu-id="959c1-156">url</span></span>  <br/> |<span data-ttu-id="959c1-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="959c1-157">xs:string</span></span>  <br/> |<span data-ttu-id="959c1-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="959c1-158">required</span></span>  <br/> |<span data-ttu-id="959c1-159">Gibt die URL für die Webseite des Diensts Wetter, die für den angegebenen Speicherort Wetterinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="959c1-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="959c1-160">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="959c1-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="959c1-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="959c1-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="959c1-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="959c1-162">xs:string</span></span>  <br/> |<span data-ttu-id="959c1-163">erforderlich</span><span class="sxs-lookup"><span data-stu-id="959c1-163">required</span></span>  <br/> |<span data-ttu-id="959c1-164">Gibt den Code, der mit dem Speicherort zum unterscheiden von mehreren Standorten mit dem gleichen Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="959c1-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="959c1-165">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="959c1-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="959c1-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="959c1-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="959c1-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="959c1-167">xs:string</span></span>  <br/> |<span data-ttu-id="959c1-168">erforderlich</span><span class="sxs-lookup"><span data-stu-id="959c1-168">required</span></span>  <br/> |<span data-ttu-id="959c1-169">Gibt den Namen des Speicherorts, der angezeigt wird im Dropdown-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="959c1-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="959c1-170">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="959c1-170">A value of the type xs:string</span></span>  <br/> |
   

