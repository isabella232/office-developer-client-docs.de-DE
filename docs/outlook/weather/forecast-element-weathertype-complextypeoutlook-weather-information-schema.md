---
title: Forecast-Element (WeatherType ComplexType) (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Gibt an, die Wetterbedingungen zukünftigen mindestens drei Tage im Voraus einschließlich heute: heute, morgen, übermorgen.'
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398325"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="1acf9-103">Forecast-Element (WeatherType ComplexType) (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="1acf9-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="1acf9-104">Gibt an, die Wetterbedingungen zukünftigen mindestens drei Tage im Voraus einschließlich heute: heute, morgen, übermorgen.</span><span class="sxs-lookup"><span data-stu-id="1acf9-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1acf9-105">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="1acf9-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1acf9-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="1acf9-106">**Element type**</span></span> <br/> |[<span data-ttu-id="1acf9-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="1acf9-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="1acf9-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="1acf9-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="1acf9-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="1acf9-109">**Schema file**</span></span> <br/> |<span data-ttu-id="1acf9-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="1acf9-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="1acf9-111">Definition</span><span class="sxs-lookup"><span data-stu-id="1acf9-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="1acf9-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="1acf9-112">Elements and attributes</span></span>

<span data-ttu-id="1acf9-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="1acf9-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="1acf9-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1acf9-114">Parent elements</span></span>

|<span data-ttu-id="1acf9-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="1acf9-115">**Element**</span></span>|<span data-ttu-id="1acf9-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1acf9-116">**Type**</span></span>|<span data-ttu-id="1acf9-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1acf9-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="1acf9-118">Wetterbericht</span><span class="sxs-lookup"><span data-stu-id="1acf9-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="1acf9-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="1acf9-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="1acf9-120">Gibt die Wetterbedingungen einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="1acf9-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1acf9-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1acf9-121">Child elements</span></span>

<span data-ttu-id="1acf9-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="1acf9-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1acf9-123">Attribute</span><span class="sxs-lookup"><span data-stu-id="1acf9-123">Attributes</span></span>

|<span data-ttu-id="1acf9-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1acf9-124">**Attribute**</span></span>|<span data-ttu-id="1acf9-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="1acf9-125">**Type**</span></span>|<span data-ttu-id="1acf9-126">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="1acf9-126">**Required**</span></span>|<span data-ttu-id="1acf9-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1acf9-127">**Description**</span></span>|<span data-ttu-id="1acf9-128">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="1acf9-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="1acf9-129">date</span><span class="sxs-lookup"><span data-stu-id="1acf9-129">date</span></span>  <br/> |<span data-ttu-id="1acf9-130">xs: Date</span><span class="sxs-lookup"><span data-stu-id="1acf9-130">xs:date</span></span>  <br/> |<span data-ttu-id="1acf9-131">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1acf9-131">required</span></span>  <br/> |<span data-ttu-id="1acf9-132">Gibt das Datum für die Planung.</span><span class="sxs-lookup"><span data-stu-id="1acf9-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="1acf9-133">Ein Wert, der den Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="1acf9-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="1acf9-134">Tag</span><span class="sxs-lookup"><span data-stu-id="1acf9-134">day</span></span>  <br/> |<span data-ttu-id="1acf9-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="1acf9-135">xs:string</span></span>  <br/> |<span data-ttu-id="1acf9-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1acf9-136">required</span></span>  <br/> |<span data-ttu-id="1acf9-137">Gibt einen Tag für die Planung.</span><span class="sxs-lookup"><span data-stu-id="1acf9-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="1acf9-138">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="1acf9-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="1acf9-139">hohe</span><span class="sxs-lookup"><span data-stu-id="1acf9-139">high</span></span>  <br/> |<span data-ttu-id="1acf9-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1acf9-140">xs:integer</span></span>  <br/> |<span data-ttu-id="1acf9-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1acf9-141">required</span></span>  <br/> |<span data-ttu-id="1acf9-142">Gibt die höchste prognostizierten Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="1acf9-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="1acf9-143">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="1acf9-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="1acf9-144">Niedrig</span><span class="sxs-lookup"><span data-stu-id="1acf9-144">low</span></span>  <br/> |<span data-ttu-id="1acf9-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1acf9-145">xs:integer</span></span>  <br/> |<span data-ttu-id="1acf9-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1acf9-146">required</span></span>  <br/> |<span data-ttu-id="1acf9-147">Gibt die geplanten niedrigsten Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="1acf9-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="1acf9-148">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="1acf9-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="1acf9-149">precip</span><span class="sxs-lookup"><span data-stu-id="1acf9-149">precip</span></span>  <br/> |<span data-ttu-id="1acf9-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1acf9-150">xs:integer</span></span>  <br/> |<span data-ttu-id="1acf9-151">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1acf9-151">required</span></span>  <br/> |<span data-ttu-id="1acf9-152">Gibt die Möglichkeit Prozentsatz Niederschlagsmenge an.</span><span class="sxs-lookup"><span data-stu-id="1acf9-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="1acf9-153">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="1acf9-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="1acf9-154">shortday</span><span class="sxs-lookup"><span data-stu-id="1acf9-154">shortday</span></span>  <br/> |<span data-ttu-id="1acf9-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="1acf9-155">xs:string</span></span>  <br/> |<span data-ttu-id="1acf9-156">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1acf9-156">required</span></span>  <br/> |<span data-ttu-id="1acf9-157">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="1acf9-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="1acf9-158">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="1acf9-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="1acf9-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="1acf9-159">skycodeday</span></span>  <br/> |<span data-ttu-id="1acf9-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="1acf9-160">xs:integer</span></span>  <br/> |<span data-ttu-id="1acf9-161">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1acf9-161">required</span></span>  <br/> |<span data-ttu-id="1acf9-162">Gibt einen Code für die geplanten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="1acf9-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="1acf9-163">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="1acf9-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="1acf9-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="1acf9-164">skytextday</span></span>  <br/> |<span data-ttu-id="1acf9-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="1acf9-165">xs:string</span></span>  <br/> |<span data-ttu-id="1acf9-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="1acf9-166">required</span></span>  <br/> |<span data-ttu-id="1acf9-167">Gibt ein bis zwei Wörter, die die geplanten Bedingungen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="1acf9-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="1acf9-168">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="1acf9-168">A value of the type xs:string</span></span>  <br/> |
   

