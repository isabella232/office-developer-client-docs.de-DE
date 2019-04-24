---
title: Forecast-Element (weathertype complexType) (Outlook Wetter Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen im Voraus an: heute, morgen, übermorgen.'
ms.openlocfilehash: 01604796d4460cc14005ee00ea6b8f46f04d4742
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339564"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="e49cb-103">Forecast-Element (weathertype complexType) (Outlook Wetter Information-Schema)</span><span class="sxs-lookup"><span data-stu-id="e49cb-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="e49cb-104">Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen im Voraus an: heute, morgen, übermorgen.</span><span class="sxs-lookup"><span data-stu-id="e49cb-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e49cb-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e49cb-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e49cb-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="e49cb-106">**Element type**</span></span> <br/> |[<span data-ttu-id="e49cb-107">forecasttype</span><span class="sxs-lookup"><span data-stu-id="e49cb-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="e49cb-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="e49cb-108">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="e49cb-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="e49cb-109">**Schema file**</span></span> <br/> |<span data-ttu-id="e49cb-110">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="e49cb-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="e49cb-111">Definition</span><span class="sxs-lookup"><span data-stu-id="e49cb-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="e49cb-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="e49cb-112">Elements and attributes</span></span>

<span data-ttu-id="e49cb-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="e49cb-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="e49cb-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e49cb-114">Parent elements</span></span>

|<span data-ttu-id="e49cb-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e49cb-115">**Element**</span></span>|<span data-ttu-id="e49cb-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e49cb-116">**Type**</span></span>|<span data-ttu-id="e49cb-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e49cb-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="e49cb-118">Wetter</span><span class="sxs-lookup"><span data-stu-id="e49cb-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="e49cb-119">weathertype</span><span class="sxs-lookup"><span data-stu-id="e49cb-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="e49cb-120">Gibt die Wetterbedingungen für einen Standort an.</span><span class="sxs-lookup"><span data-stu-id="e49cb-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e49cb-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e49cb-121">Child elements</span></span>

<span data-ttu-id="e49cb-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="e49cb-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e49cb-123">Attribute</span><span class="sxs-lookup"><span data-stu-id="e49cb-123">Attributes</span></span>

|<span data-ttu-id="e49cb-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e49cb-124">**Attribute**</span></span>|<span data-ttu-id="e49cb-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="e49cb-125">**Type**</span></span>|<span data-ttu-id="e49cb-126">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="e49cb-126">**Required**</span></span>|<span data-ttu-id="e49cb-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e49cb-127">**Description**</span></span>|<span data-ttu-id="e49cb-128">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="e49cb-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="e49cb-129">Datum</span><span class="sxs-lookup"><span data-stu-id="e49cb-129">date</span></span>  <br/> |<span data-ttu-id="e49cb-130">xs: Datum</span><span class="sxs-lookup"><span data-stu-id="e49cb-130">xs:date</span></span>  <br/> |<span data-ttu-id="e49cb-131">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e49cb-131">required</span></span>  <br/> |<span data-ttu-id="e49cb-132">Gibt das Datum für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="e49cb-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="e49cb-133">Ein Wert vom Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="e49cb-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="e49cb-134">Tag</span><span class="sxs-lookup"><span data-stu-id="e49cb-134">day</span></span>  <br/> |<span data-ttu-id="e49cb-135">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e49cb-135">xs:string</span></span>  <br/> |<span data-ttu-id="e49cb-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e49cb-136">required</span></span>  <br/> |<span data-ttu-id="e49cb-137">Gibt einen Tag für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="e49cb-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="e49cb-138">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="e49cb-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="e49cb-139">hohe</span><span class="sxs-lookup"><span data-stu-id="e49cb-139">high</span></span>  <br/> |<span data-ttu-id="e49cb-140">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="e49cb-140">xs:integer</span></span>  <br/> |<span data-ttu-id="e49cb-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e49cb-141">required</span></span>  <br/> |<span data-ttu-id="e49cb-142">Gibt die prognostizierte höchste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="e49cb-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="e49cb-143">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="e49cb-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="e49cb-144">mit niedriger</span><span class="sxs-lookup"><span data-stu-id="e49cb-144">low</span></span>  <br/> |<span data-ttu-id="e49cb-145">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="e49cb-145">xs:integer</span></span>  <br/> |<span data-ttu-id="e49cb-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e49cb-146">required</span></span>  <br/> |<span data-ttu-id="e49cb-147">Gibt die prognostizierte niedrigste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="e49cb-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="e49cb-148">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="e49cb-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="e49cb-149">Precip</span><span class="sxs-lookup"><span data-stu-id="e49cb-149">precip</span></span>  <br/> |<span data-ttu-id="e49cb-150">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="e49cb-150">xs:integer</span></span>  <br/> |<span data-ttu-id="e49cb-151">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e49cb-151">required</span></span>  <br/> |<span data-ttu-id="e49cb-152">Gibt die prozentuale Niederschlagswahrscheinlichkeit an.</span><span class="sxs-lookup"><span data-stu-id="e49cb-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="e49cb-153">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="e49cb-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="e49cb-154">shortday</span><span class="sxs-lookup"><span data-stu-id="e49cb-154">shortday</span></span>  <br/> |<span data-ttu-id="e49cb-155">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e49cb-155">xs:string</span></span>  <br/> |<span data-ttu-id="e49cb-156">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e49cb-156">required</span></span>  <br/> |<span data-ttu-id="e49cb-157">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="e49cb-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="e49cb-158">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="e49cb-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="e49cb-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="e49cb-159">skycodeday</span></span>  <br/> |<span data-ttu-id="e49cb-160">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="e49cb-160">xs:integer</span></span>  <br/> |<span data-ttu-id="e49cb-161">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e49cb-161">required</span></span>  <br/> |<span data-ttu-id="e49cb-162">Gibt einen Code für die prognostizierten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="e49cb-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="e49cb-163">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="e49cb-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="e49cb-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="e49cb-164">skytextday</span></span>  <br/> |<span data-ttu-id="e49cb-165">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="e49cb-165">xs:string</span></span>  <br/> |<span data-ttu-id="e49cb-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="e49cb-166">required</span></span>  <br/> |<span data-ttu-id="e49cb-167">Gibt ein bis zwei Wörter an, in denen die prognostizierten Bedingungen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="e49cb-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="e49cb-168">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="e49cb-168">A value of the type xs:string</span></span>  <br/> |
   

