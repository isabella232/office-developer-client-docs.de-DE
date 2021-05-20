---
title: wetterelement (weatherdata-Element) (Outlook Wetterinformationsschema)
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
# <a name="weather-element-weatherdata-element-outlook-weather-information-schema"></a><span data-ttu-id="16551-103">wetterelement (weatherdata-Element) (Outlook Wetterinformationsschema)</span><span class="sxs-lookup"><span data-stu-id="16551-103">weather element (weatherdata element) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="16551-104">Gibt die Wetterbedingungen eines Standorts an.</span><span class="sxs-lookup"><span data-stu-id="16551-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="16551-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="16551-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="16551-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="16551-106">**Element type**</span></span> <br/> |[<span data-ttu-id="16551-107">weatherType</span><span class="sxs-lookup"><span data-stu-id="16551-107">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="16551-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="16551-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="16551-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="16551-109">**Schema file**</span></span> <br/> |<span data-ttu-id="16551-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="16551-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="16551-111">Definition</span><span class="sxs-lookup"><span data-stu-id="16551-111">Definition</span></span>

```XML
<xs:element name="weather"      type="weatherType">
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="16551-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="16551-112">Elements and attributes</span></span>

<span data-ttu-id="16551-113">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="16551-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="16551-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16551-114">Parent elements</span></span>

|<span data-ttu-id="16551-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="16551-115">**Element**</span></span>|<span data-ttu-id="16551-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="16551-116">**Type**</span></span>|<span data-ttu-id="16551-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16551-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16551-118">weatherdata</span><span class="sxs-lookup"><span data-stu-id="16551-118">weatherdata</span></span>](weatherdata-element-outlook-weather-information-schema.md) <br/> ||<span data-ttu-id="16551-119">Definiert das Wetterelement.</span><span class="sxs-lookup"><span data-stu-id="16551-119">Defines the weather element.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="16551-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="16551-120">Child elements</span></span>

|<span data-ttu-id="16551-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="16551-121">**Element**</span></span>|<span data-ttu-id="16551-122">**Typ**</span><span class="sxs-lookup"><span data-stu-id="16551-122">**Type**</span></span>|<span data-ttu-id="16551-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16551-123">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="16551-124">current</span><span class="sxs-lookup"><span data-stu-id="16551-124">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="16551-125">currentType</span><span class="sxs-lookup"><span data-stu-id="16551-125">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="16551-126">Gibt die aktuellen Wetterbedingungen an.</span><span class="sxs-lookup"><span data-stu-id="16551-126">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="16551-127">forecast</span><span class="sxs-lookup"><span data-stu-id="16551-127">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="16551-128">forecastType</span><span class="sxs-lookup"><span data-stu-id="16551-128">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="16551-129">Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: Heute, Morgen, Tag nach Morgen.</span><span class="sxs-lookup"><span data-stu-id="16551-129">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="16551-130">Attribute</span><span class="sxs-lookup"><span data-stu-id="16551-130">Attributes</span></span>

|<span data-ttu-id="16551-131">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="16551-131">**Attribute**</span></span>|<span data-ttu-id="16551-132">**Typ**</span><span class="sxs-lookup"><span data-stu-id="16551-132">**Type**</span></span>|<span data-ttu-id="16551-133">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="16551-133">**Required**</span></span>|<span data-ttu-id="16551-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="16551-134">**Description**</span></span>|<span data-ttu-id="16551-135">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="16551-135">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="16551-136">attribution</span><span class="sxs-lookup"><span data-stu-id="16551-136">attribution</span></span>  <br/> |<span data-ttu-id="16551-137">xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-137">xs:string</span></span>  <br/> |<span data-ttu-id="16551-138">erforderlich</span><span class="sxs-lookup"><span data-stu-id="16551-138">required</span></span>  <br/> |<span data-ttu-id="16551-139">Gibt die Quelle der Wetterinformationen an.</span><span class="sxs-lookup"><span data-stu-id="16551-139">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="16551-140">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-140">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="16551-141">degreetype</span><span class="sxs-lookup"><span data-stu-id="16551-141">degreetype</span></span>  <br/> |<span data-ttu-id="16551-142">xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-142">xs:string</span></span>  <br/> |<span data-ttu-id="16551-143">erforderlich</span><span class="sxs-lookup"><span data-stu-id="16551-143">required</span></span>  <br/> |<span data-ttu-id="16551-144">Gibt die Einheit für die Temperatur des Standorts an, z. B. "Celsius".</span><span class="sxs-lookup"><span data-stu-id="16551-144">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="16551-145">C, F</span><span class="sxs-lookup"><span data-stu-id="16551-145">C, F</span></span>  <br/> |
|<span data-ttu-id="16551-146">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="16551-146">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="16551-147">xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-147">xs:string</span></span>  <br/> |<span data-ttu-id="16551-148">erforderlich</span><span class="sxs-lookup"><span data-stu-id="16551-148">required</span></span>  <br/> |<span data-ttu-id="16551-149">Gibt die URL des Bilds für den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="16551-149">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="16551-150">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-150">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="16551-151">Zeitzone</span><span class="sxs-lookup"><span data-stu-id="16551-151">timezone</span></span>  <br/> |<span data-ttu-id="16551-152">xs:integer</span><span class="sxs-lookup"><span data-stu-id="16551-152">xs:integer</span></span>  <br/> |<span data-ttu-id="16551-153">erforderlich</span><span class="sxs-lookup"><span data-stu-id="16551-153">required</span></span>  <br/> |<span data-ttu-id="16551-154">Gibt den GMT-Offset an.</span><span class="sxs-lookup"><span data-stu-id="16551-154">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="16551-155">Ein Wert zwischen -11 und einschließlich 12</span><span class="sxs-lookup"><span data-stu-id="16551-155">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="16551-156">url</span><span class="sxs-lookup"><span data-stu-id="16551-156">url</span></span>  <br/> |<span data-ttu-id="16551-157">xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-157">xs:string</span></span>  <br/> |<span data-ttu-id="16551-158">erforderlich</span><span class="sxs-lookup"><span data-stu-id="16551-158">required</span></span>  <br/> |<span data-ttu-id="16551-159">Gibt die URL für die Webseite des Wetterdiensts an, die Wetterinformationen für den angegebenen Standort enthält.</span><span class="sxs-lookup"><span data-stu-id="16551-159">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="16551-160">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-160">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="16551-161">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="16551-161">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="16551-162">xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-162">xs:string</span></span>  <br/> |<span data-ttu-id="16551-163">erforderlich</span><span class="sxs-lookup"><span data-stu-id="16551-163">required</span></span>  <br/> |<span data-ttu-id="16551-164">Gibt den Code an, der dem Speicherort zugeordnet ist, der zum Unterscheiden mehrerer Speicherorte mit demselben Namen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="16551-164">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="16551-165">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-165">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="16551-166">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="16551-166">weatherlocationname</span></span>  <br/> |<span data-ttu-id="16551-167">xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-167">xs:string</span></span>  <br/> |<span data-ttu-id="16551-168">erforderlich</span><span class="sxs-lookup"><span data-stu-id="16551-168">required</span></span>  <br/> |<span data-ttu-id="16551-169">Gibt den Namen des Speicherorts an, der im Dropdownsteuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="16551-169">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="16551-170">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="16551-170">A value of the type xs:string</span></span>  <br/> |
   

