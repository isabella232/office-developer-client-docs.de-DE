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
ms.openlocfilehash: c618b753ddf8a72fce270800675982f1a7f7af5b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796097"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="9ff4e-103">Forecast-Element (WeatherType ComplexType) (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="9ff4e-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="9ff4e-104">Gibt an, die Wetterbedingungen zukünftigen mindestens drei Tage im Voraus einschließlich heute: heute, morgen, übermorgen.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9ff4e-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9ff4e-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9ff4e-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-106">**Element type**</span></span> <br/> |[<span data-ttu-id="9ff4e-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="9ff4e-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="9ff4e-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="9ff4e-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-109">**Schema file**</span></span> <br/> |<span data-ttu-id="9ff4e-110">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="9ff4e-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="9ff4e-111">Definition</span><span class="sxs-lookup"><span data-stu-id="9ff4e-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="9ff4e-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="9ff4e-112">Elements and attributes</span></span>

<span data-ttu-id="9ff4e-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="9ff4e-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ff4e-114">Parent elements</span></span>

|<span data-ttu-id="9ff4e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-115">**Element**</span></span>|<span data-ttu-id="9ff4e-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-116">**Type**</span></span>|<span data-ttu-id="9ff4e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="9ff4e-118">Wetterbericht</span><span class="sxs-lookup"><span data-stu-id="9ff4e-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="9ff4e-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="9ff4e-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="9ff4e-120">Gibt die Wetterbedingungen einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9ff4e-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9ff4e-121">Child elements</span></span>

<span data-ttu-id="9ff4e-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9ff4e-123">Attribute</span><span class="sxs-lookup"><span data-stu-id="9ff4e-123">Attributes</span></span>

|<span data-ttu-id="9ff4e-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-124">**Attribute**</span></span>|<span data-ttu-id="9ff4e-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-125">**Type**</span></span>|<span data-ttu-id="9ff4e-126">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-126">**Required**</span></span>|<span data-ttu-id="9ff4e-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-127">**Description**</span></span>|<span data-ttu-id="9ff4e-128">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="9ff4e-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="9ff4e-129">date</span><span class="sxs-lookup"><span data-stu-id="9ff4e-129">date</span></span>  <br/> |<span data-ttu-id="9ff4e-130">xs: Date</span><span class="sxs-lookup"><span data-stu-id="9ff4e-130">xs:date</span></span>  <br/> |<span data-ttu-id="9ff4e-131">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ff4e-131">required</span></span>  <br/> |<span data-ttu-id="9ff4e-132">Gibt das Datum für die Planung.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="9ff4e-133">Ein Wert, der den Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="9ff4e-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="9ff4e-134">Tag</span><span class="sxs-lookup"><span data-stu-id="9ff4e-134">day</span></span>  <br/> |<span data-ttu-id="9ff4e-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff4e-135">xs:string</span></span>  <br/> |<span data-ttu-id="9ff4e-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ff4e-136">required</span></span>  <br/> |<span data-ttu-id="9ff4e-137">Gibt einen Tag für die Planung.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="9ff4e-138">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="9ff4e-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9ff4e-139">hohe</span><span class="sxs-lookup"><span data-stu-id="9ff4e-139">high</span></span>  <br/> |<span data-ttu-id="9ff4e-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9ff4e-140">xs:integer</span></span>  <br/> |<span data-ttu-id="9ff4e-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ff4e-141">required</span></span>  <br/> |<span data-ttu-id="9ff4e-142">Gibt die höchste prognostizierten Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="9ff4e-143">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="9ff4e-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9ff4e-144">Niedrig</span><span class="sxs-lookup"><span data-stu-id="9ff4e-144">low</span></span>  <br/> |<span data-ttu-id="9ff4e-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9ff4e-145">xs:integer</span></span>  <br/> |<span data-ttu-id="9ff4e-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ff4e-146">required</span></span>  <br/> |<span data-ttu-id="9ff4e-147">Gibt die geplanten niedrigsten Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="9ff4e-148">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="9ff4e-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9ff4e-149">precip</span><span class="sxs-lookup"><span data-stu-id="9ff4e-149">precip</span></span>  <br/> |<span data-ttu-id="9ff4e-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9ff4e-150">xs:integer</span></span>  <br/> |<span data-ttu-id="9ff4e-151">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ff4e-151">required</span></span>  <br/> |<span data-ttu-id="9ff4e-152">Gibt die Möglichkeit Prozentsatz Niederschlagsmenge an.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="9ff4e-153">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="9ff4e-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9ff4e-154">shortday</span><span class="sxs-lookup"><span data-stu-id="9ff4e-154">shortday</span></span>  <br/> |<span data-ttu-id="9ff4e-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff4e-155">xs:string</span></span>  <br/> |<span data-ttu-id="9ff4e-156">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ff4e-156">required</span></span>  <br/> |<span data-ttu-id="9ff4e-157">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="9ff4e-158">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="9ff4e-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="9ff4e-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="9ff4e-159">skycodeday</span></span>  <br/> |<span data-ttu-id="9ff4e-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="9ff4e-160">xs:integer</span></span>  <br/> |<span data-ttu-id="9ff4e-161">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ff4e-161">required</span></span>  <br/> |<span data-ttu-id="9ff4e-162">Gibt einen Code für die geplanten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="9ff4e-163">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="9ff4e-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="9ff4e-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="9ff4e-164">skytextday</span></span>  <br/> |<span data-ttu-id="9ff4e-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="9ff4e-165">xs:string</span></span>  <br/> |<span data-ttu-id="9ff4e-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="9ff4e-166">required</span></span>  <br/> |<span data-ttu-id="9ff4e-167">Gibt ein bis zwei Wörter, die die geplanten Bedingungen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="9ff4e-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="9ff4e-168">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="9ff4e-168">A value of the type xs:string</span></span>  <br/> |
   

