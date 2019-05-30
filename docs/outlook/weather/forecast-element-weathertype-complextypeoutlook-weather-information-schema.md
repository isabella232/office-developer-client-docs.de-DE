---
title: Forecast-Element (weathertype complexType) (Outlook-Wetter Informations Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: heute, morgen, Tag nach morgen.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540980"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="17129-103">Forecast-Element (weathertype complexType) (Outlook-Wetter Informations Schema)</span><span class="sxs-lookup"><span data-stu-id="17129-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="17129-104">Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: heute, morgen, Tag nach morgen.</span><span class="sxs-lookup"><span data-stu-id="17129-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17129-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="17129-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17129-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="17129-106">**Element type**</span></span> <br/> |[<span data-ttu-id="17129-107">forecasttype</span><span class="sxs-lookup"><span data-stu-id="17129-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="17129-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="17129-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="17129-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="17129-109">**Schema file**</span></span> <br/> |<span data-ttu-id="17129-110">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="17129-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="17129-111">Definition</span><span class="sxs-lookup"><span data-stu-id="17129-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="17129-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="17129-112">Elements and attributes</span></span>

<span data-ttu-id="17129-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="17129-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="17129-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17129-114">Parent elements</span></span>

|<span data-ttu-id="17129-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="17129-115">**Element**</span></span>|<span data-ttu-id="17129-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="17129-116">**Type**</span></span>|<span data-ttu-id="17129-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17129-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="17129-118">Wetter</span><span class="sxs-lookup"><span data-stu-id="17129-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="17129-119">weathertype</span><span class="sxs-lookup"><span data-stu-id="17129-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="17129-120">Gibt die Wetterbedingungen eines Standorts an.</span><span class="sxs-lookup"><span data-stu-id="17129-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="17129-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17129-121">Child elements</span></span>

<span data-ttu-id="17129-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="17129-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17129-123">Attribute</span><span class="sxs-lookup"><span data-stu-id="17129-123">Attributes</span></span>

|<span data-ttu-id="17129-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="17129-124">**Attribute**</span></span>|<span data-ttu-id="17129-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="17129-125">**Type**</span></span>|<span data-ttu-id="17129-126">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="17129-126">**Required**</span></span>|<span data-ttu-id="17129-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17129-127">**Description**</span></span>|<span data-ttu-id="17129-128">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="17129-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="17129-129">date</span><span class="sxs-lookup"><span data-stu-id="17129-129">date</span></span>  <br/> |<span data-ttu-id="17129-130">xs: Datum</span><span class="sxs-lookup"><span data-stu-id="17129-130">xs:date</span></span>  <br/> |<span data-ttu-id="17129-131">erforderlich</span><span class="sxs-lookup"><span data-stu-id="17129-131">required</span></span>  <br/> |<span data-ttu-id="17129-132">Gibt das Datum für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="17129-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="17129-133">Ein Wert vom Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="17129-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="17129-134">Tag</span><span class="sxs-lookup"><span data-stu-id="17129-134">day</span></span>  <br/> |<span data-ttu-id="17129-135">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="17129-135">xs:string</span></span>  <br/> |<span data-ttu-id="17129-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="17129-136">required</span></span>  <br/> |<span data-ttu-id="17129-137">Gibt einen Tag für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="17129-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="17129-138">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="17129-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="17129-139">hohe</span><span class="sxs-lookup"><span data-stu-id="17129-139">high</span></span>  <br/> |<span data-ttu-id="17129-140">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="17129-140">xs:integer</span></span>  <br/> |<span data-ttu-id="17129-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="17129-141">required</span></span>  <br/> |<span data-ttu-id="17129-142">Gibt die prognostizierte höchste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="17129-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="17129-143">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="17129-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="17129-144">niedrigen</span><span class="sxs-lookup"><span data-stu-id="17129-144">low</span></span>  <br/> |<span data-ttu-id="17129-145">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="17129-145">xs:integer</span></span>  <br/> |<span data-ttu-id="17129-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="17129-146">required</span></span>  <br/> |<span data-ttu-id="17129-147">Gibt die prognostizierte niedrigste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="17129-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="17129-148">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="17129-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="17129-149">Precip</span><span class="sxs-lookup"><span data-stu-id="17129-149">precip</span></span>  <br/> |<span data-ttu-id="17129-150">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="17129-150">xs:integer</span></span>  <br/> |<span data-ttu-id="17129-151">erforderlich</span><span class="sxs-lookup"><span data-stu-id="17129-151">required</span></span>  <br/> |<span data-ttu-id="17129-152">Gibt den Prozentsatz der Niederschlagswahrscheinlichkeit an.</span><span class="sxs-lookup"><span data-stu-id="17129-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="17129-153">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="17129-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="17129-154">shortday</span><span class="sxs-lookup"><span data-stu-id="17129-154">shortday</span></span>  <br/> |<span data-ttu-id="17129-155">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="17129-155">xs:string</span></span>  <br/> |<span data-ttu-id="17129-156">erforderlich</span><span class="sxs-lookup"><span data-stu-id="17129-156">required</span></span>  <br/> |<span data-ttu-id="17129-157">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="17129-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="17129-158">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="17129-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="17129-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="17129-159">skycodeday</span></span>  <br/> |<span data-ttu-id="17129-160">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="17129-160">xs:integer</span></span>  <br/> |<span data-ttu-id="17129-161">erforderlich</span><span class="sxs-lookup"><span data-stu-id="17129-161">required</span></span>  <br/> |<span data-ttu-id="17129-162">Gibt einen Code für die prognostizierten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="17129-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="17129-163">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="17129-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="17129-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="17129-164">skytextday</span></span>  <br/> |<span data-ttu-id="17129-165">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="17129-165">xs:string</span></span>  <br/> |<span data-ttu-id="17129-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="17129-166">required</span></span>  <br/> |<span data-ttu-id="17129-167">Gibt ein bis zwei Wörter an, die die prognostizierten Bedingungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="17129-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="17129-168">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="17129-168">A value of the type xs:string</span></span>  <br/> |
   

