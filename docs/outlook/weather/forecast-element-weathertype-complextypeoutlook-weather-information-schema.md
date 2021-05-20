---
title: forecast-Element (weatherType complexType) (Outlook Wetterinformationsschema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9124fa30-d58b-8354-91e9-8d2237a8251d
description: 'Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: Heute, Morgen, Tag nach Morgen.'
ms.openlocfilehash: 5e442ee5995bbd51c5e518162286bc199a625dbd
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540980"
---
# <a name="forecast-element-weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="38b90-103">forecast-Element (weatherType complexType) (Outlook Wetterinformationsschema)</span><span class="sxs-lookup"><span data-stu-id="38b90-103">forecast element (weatherType complexType) (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="38b90-104">Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: Heute, Morgen, Tag nach Morgen.</span><span class="sxs-lookup"><span data-stu-id="38b90-104">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="38b90-105">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="38b90-105">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="38b90-106">**Elementtyp**</span><span class="sxs-lookup"><span data-stu-id="38b90-106">**Element type**</span></span> <br/> |[<span data-ttu-id="38b90-107">forecastType</span><span class="sxs-lookup"><span data-stu-id="38b90-107">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |
|<span data-ttu-id="38b90-108">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="38b90-108">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="38b90-109">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="38b90-109">**Schema file**</span></span> <br/> |<span data-ttu-id="38b90-110">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="38b90-110">getweatherinfo.xsd</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="38b90-111">Definition</span><span class="sxs-lookup"><span data-stu-id="38b90-111">Definition</span></span>

```XML
<xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  

```

## <a name="elements-and-attributes"></a><span data-ttu-id="38b90-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="38b90-112">Elements and attributes</span></span>

<span data-ttu-id="38b90-113">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="38b90-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="parent-elements"></a><span data-ttu-id="38b90-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38b90-114">Parent elements</span></span>

|<span data-ttu-id="38b90-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="38b90-115">**Element**</span></span>|<span data-ttu-id="38b90-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="38b90-116">**Type**</span></span>|<span data-ttu-id="38b90-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38b90-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="38b90-118">Wetter</span><span class="sxs-lookup"><span data-stu-id="38b90-118">weather</span></span>](weather-element-weatherdata-elementoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="38b90-119">weatherType</span><span class="sxs-lookup"><span data-stu-id="38b90-119">weatherType</span></span>](weathertype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="38b90-120">Gibt die Wetterbedingungen eines Standorts an.</span><span class="sxs-lookup"><span data-stu-id="38b90-120">Specifies the weather conditions of a location.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="38b90-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="38b90-121">Child elements</span></span>

<span data-ttu-id="38b90-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="38b90-122">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="38b90-123">Attribute</span><span class="sxs-lookup"><span data-stu-id="38b90-123">Attributes</span></span>

|<span data-ttu-id="38b90-124">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="38b90-124">**Attribute**</span></span>|<span data-ttu-id="38b90-125">**Typ**</span><span class="sxs-lookup"><span data-stu-id="38b90-125">**Type**</span></span>|<span data-ttu-id="38b90-126">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="38b90-126">**Required**</span></span>|<span data-ttu-id="38b90-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="38b90-127">**Description**</span></span>|<span data-ttu-id="38b90-128">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="38b90-128">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="38b90-129">date</span><span class="sxs-lookup"><span data-stu-id="38b90-129">date</span></span>  <br/> |<span data-ttu-id="38b90-130">xs:date</span><span class="sxs-lookup"><span data-stu-id="38b90-130">xs:date</span></span>  <br/> |<span data-ttu-id="38b90-131">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b90-131">required</span></span>  <br/> |<span data-ttu-id="38b90-132">Gibt das Datum für die Planung an.</span><span class="sxs-lookup"><span data-stu-id="38b90-132">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="38b90-133">Ein Wert vom Typ xs:date</span><span class="sxs-lookup"><span data-stu-id="38b90-133">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="38b90-134">day</span><span class="sxs-lookup"><span data-stu-id="38b90-134">day</span></span>  <br/> |<span data-ttu-id="38b90-135">xs:string</span><span class="sxs-lookup"><span data-stu-id="38b90-135">xs:string</span></span>  <br/> |<span data-ttu-id="38b90-136">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b90-136">required</span></span>  <br/> |<span data-ttu-id="38b90-137">Gibt einen Tag für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="38b90-137">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="38b90-138">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="38b90-138">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="38b90-139">high</span><span class="sxs-lookup"><span data-stu-id="38b90-139">high</span></span>  <br/> |<span data-ttu-id="38b90-140">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38b90-140">xs:integer</span></span>  <br/> |<span data-ttu-id="38b90-141">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b90-141">required</span></span>  <br/> |<span data-ttu-id="38b90-142">Gibt die vorhergesagte höchste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="38b90-142">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="38b90-143">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="38b90-143">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="38b90-144">low</span><span class="sxs-lookup"><span data-stu-id="38b90-144">low</span></span>  <br/> |<span data-ttu-id="38b90-145">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38b90-145">xs:integer</span></span>  <br/> |<span data-ttu-id="38b90-146">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b90-146">required</span></span>  <br/> |<span data-ttu-id="38b90-147">Gibt die vorhergesagte niedrigste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="38b90-147">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="38b90-148">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="38b90-148">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="38b90-149">precip</span><span class="sxs-lookup"><span data-stu-id="38b90-149">precip</span></span>  <br/> |<span data-ttu-id="38b90-150">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38b90-150">xs:integer</span></span>  <br/> |<span data-ttu-id="38b90-151">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b90-151">required</span></span>  <br/> |<span data-ttu-id="38b90-152">Gibt die prozentuale Wahrscheinlichkeit der Verfällung an.</span><span class="sxs-lookup"><span data-stu-id="38b90-152">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="38b90-153">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="38b90-153">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="38b90-154">shortday</span><span class="sxs-lookup"><span data-stu-id="38b90-154">shortday</span></span>  <br/> |<span data-ttu-id="38b90-155">xs:string</span><span class="sxs-lookup"><span data-stu-id="38b90-155">xs:string</span></span>  <br/> |<span data-ttu-id="38b90-156">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b90-156">required</span></span>  <br/> |<span data-ttu-id="38b90-157">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="38b90-157">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="38b90-158">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="38b90-158">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="38b90-159">skycodeday</span><span class="sxs-lookup"><span data-stu-id="38b90-159">skycodeday</span></span>  <br/> |<span data-ttu-id="38b90-160">xs:integer</span><span class="sxs-lookup"><span data-stu-id="38b90-160">xs:integer</span></span>  <br/> |<span data-ttu-id="38b90-161">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b90-161">required</span></span>  <br/> |<span data-ttu-id="38b90-162">Gibt einen Code für die vorhergesagten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="38b90-162">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="38b90-163">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="38b90-163">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="38b90-164">skytextday</span><span class="sxs-lookup"><span data-stu-id="38b90-164">skytextday</span></span>  <br/> |<span data-ttu-id="38b90-165">xs:string</span><span class="sxs-lookup"><span data-stu-id="38b90-165">xs:string</span></span>  <br/> |<span data-ttu-id="38b90-166">erforderlich</span><span class="sxs-lookup"><span data-stu-id="38b90-166">required</span></span>  <br/> |<span data-ttu-id="38b90-167">Gibt ein bis zwei Wörter an, die die prognostizierten Bedingungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="38b90-167">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="38b90-168">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="38b90-168">A value of the type xs:string</span></span>  <br/> |
   

