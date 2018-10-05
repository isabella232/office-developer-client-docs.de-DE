---
title: CurrentType ComplexType (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Definiert die Parameter über die aktuelle Wettervorhersage von einem Speicherort an.
ms.openlocfilehash: 16d3e23375f68315c9b9f3a7e914d93f4fec9d0a
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387034"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="0ebf4-103">CurrentType ComplexType (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="0ebf4-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="0ebf4-104">Definiert die Parameter über die aktuelle Wettervorhersage von einem Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="0ebf4-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0ebf4-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0ebf4-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0ebf4-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="0ebf4-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0ebf4-107">**Schema file**</span></span> <br/> |<span data-ttu-id="0ebf4-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="0ebf4-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="0ebf4-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0ebf4-109">**Extension base**</span></span> <br/> |<span data-ttu-id="0ebf4-110">Keine</span><span class="sxs-lookup"><span data-stu-id="0ebf4-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0ebf4-111">Definition</span><span class="sxs-lookup"><span data-stu-id="0ebf4-111">Definition</span></span>

```XML
       <xs:complexType name="currentType">
     <xs:attribute name="winddisplay"   type="xs:string"      use="required"     />
     <xs:attribute name="windspeed"   type="xs:integer"      use="required"     />
     <xs:attribute name="humidity"   type="xs:integer"      use="required"     />
     <xs:attribute name="feelslike"   type="xs:integer"      use="required"     />
     <xs:attribute name="observationpoint"   type="xs:string"      use="required"     />
     <xs:attribute name="observationtime"   type="xs:time"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="skytext"   type="xs:string"      use="required"     />
     <xs:attribute name="skycode"   type="xs:integer"      use="required"     />
     <xs:attribute name="temperature"   type="xs:integer"      use="required"     />
     <xs:attribute name="shortday"   type="xs:string"      use="optional"     />
     <xs:attribute name="day"   type="xs:string"      use="optional"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="0ebf4-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0ebf4-112">Elements and attributes</span></span>

<span data-ttu-id="0ebf4-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0ebf4-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0ebf4-114">Child elements</span></span>

<span data-ttu-id="0ebf4-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0ebf4-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="0ebf4-116">Attributes</span></span>

|<span data-ttu-id="0ebf4-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0ebf4-117">**Attribute**</span></span>|<span data-ttu-id="0ebf4-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0ebf4-118">**Type**</span></span>|<span data-ttu-id="0ebf4-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0ebf4-119">**Required**</span></span>|<span data-ttu-id="0ebf4-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0ebf4-120">**Description**</span></span>|<span data-ttu-id="0ebf4-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0ebf4-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0ebf4-122">date</span><span class="sxs-lookup"><span data-stu-id="0ebf4-122">date</span></span>  <br/> |<span data-ttu-id="0ebf4-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="0ebf4-123">xs:date</span></span>  <br/> |<span data-ttu-id="0ebf4-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-124">required</span></span>  <br/> |<span data-ttu-id="0ebf4-125">Heutiges Datum angibt.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="0ebf4-126">Ein Wert, der den Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="0ebf4-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="0ebf4-127">Tag</span><span class="sxs-lookup"><span data-stu-id="0ebf4-127">day</span></span>  <br/> |<span data-ttu-id="0ebf4-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="0ebf4-128">xs:string</span></span>  <br/> |<span data-ttu-id="0ebf4-129">Optional</span><span class="sxs-lookup"><span data-stu-id="0ebf4-129">optional</span></span>  <br/> |<span data-ttu-id="0ebf4-130">Gibt einen Tag für die Planung.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="0ebf4-131">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0ebf4-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0ebf4-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="0ebf4-132">feelslike</span></span>  <br/> |<span data-ttu-id="0ebf4-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0ebf4-133">xs:integer</span></span>  <br/> |<span data-ttu-id="0ebf4-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-134">required</span></span>  <br/> |<span data-ttu-id="0ebf4-135">Gibt die Temperatur des wie ist mit das aktuelle Wetter wie an.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="0ebf4-136">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="0ebf4-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="0ebf4-137">Luftfeuchtigkeit</span><span class="sxs-lookup"><span data-stu-id="0ebf4-137">humidity</span></span>  <br/> |<span data-ttu-id="0ebf4-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0ebf4-138">xs:integer</span></span>  <br/> |<span data-ttu-id="0ebf4-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-139">required</span></span>  <br/> |<span data-ttu-id="0ebf4-140">Gibt den aktuellen Luftfeuchtigkeit numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="0ebf4-141">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="0ebf4-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="0ebf4-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="0ebf4-142">observationpoint</span></span>  <br/> |<span data-ttu-id="0ebf4-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="0ebf4-143">xs:string</span></span>  <br/> |<span data-ttu-id="0ebf4-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-144">required</span></span>  <br/> |<span data-ttu-id="0ebf4-145">Gibt an, in dem die aktuelle Wetterinformationen aus beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="0ebf4-146">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0ebf4-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0ebf4-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="0ebf4-147">observationtime</span></span>  <br/> |<span data-ttu-id="0ebf4-148">xs: Time</span><span class="sxs-lookup"><span data-stu-id="0ebf4-148">xs:time</span></span>  <br/> |<span data-ttu-id="0ebf4-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-149">required</span></span>  <br/> |<span data-ttu-id="0ebf4-150">Gibt an, wenn die aktuelle Wetterinformationen unter beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="0ebf4-151">Ein Wert, der den Typ xs: Time</span><span class="sxs-lookup"><span data-stu-id="0ebf4-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="0ebf4-152">shortday</span><span class="sxs-lookup"><span data-stu-id="0ebf4-152">shortday</span></span>  <br/> |<span data-ttu-id="0ebf4-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="0ebf4-153">xs:string</span></span>  <br/> |<span data-ttu-id="0ebf4-154">Optional</span><span class="sxs-lookup"><span data-stu-id="0ebf4-154">optional</span></span>  <br/> |<span data-ttu-id="0ebf4-155">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="0ebf4-156">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0ebf4-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0ebf4-157">skycode</span><span class="sxs-lookup"><span data-stu-id="0ebf4-157">skycode</span></span>  <br/> |<span data-ttu-id="0ebf4-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0ebf4-158">xs:integer</span></span>  <br/> |<span data-ttu-id="0ebf4-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-159">required</span></span>  <br/> |<span data-ttu-id="0ebf4-160">Gibt einen ganze Zahl Code für die aktuelle Wettervorhersage.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="0ebf4-161">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="0ebf4-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="0ebf4-162">skytext</span><span class="sxs-lookup"><span data-stu-id="0ebf4-162">skytext</span></span>  <br/> |<span data-ttu-id="0ebf4-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="0ebf4-163">xs:string</span></span>  <br/> |<span data-ttu-id="0ebf4-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-164">required</span></span>  <br/> |<span data-ttu-id="0ebf4-165">Gibt ein bis zwei Wörter, die aktuelle Wetterbericht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="0ebf4-166">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0ebf4-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0ebf4-167">Temperatur</span><span class="sxs-lookup"><span data-stu-id="0ebf4-167">temperature</span></span>  <br/> |<span data-ttu-id="0ebf4-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0ebf4-168">xs:integer</span></span>  <br/> |<span data-ttu-id="0ebf4-169">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-169">required</span></span>  <br/> |<span data-ttu-id="0ebf4-170">Gibt die aktuelle Temperatur des Speicherorts an.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="0ebf4-171">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="0ebf4-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="0ebf4-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="0ebf4-172">winddisplay</span></span>  <br/> |<span data-ttu-id="0ebf4-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="0ebf4-173">xs:string</span></span>  <br/> |<span data-ttu-id="0ebf4-174">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-174">required</span></span>  <br/> |<span data-ttu-id="0ebf4-175">Eine Zeichenfolge, die die aktuelle Wind Bedingungen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="0ebf4-176">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0ebf4-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0ebf4-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="0ebf4-177">windspeed</span></span>  <br/> |<span data-ttu-id="0ebf4-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0ebf4-178">xs:integer</span></span>  <br/> |<span data-ttu-id="0ebf4-179">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0ebf4-179">required</span></span>  <br/> |<span data-ttu-id="0ebf4-180">Gibt den aktuellen Wert der numerische Wind Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="0ebf4-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="0ebf4-181">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="0ebf4-181">A value of the type xs:integer</span></span>  <br/> |
   

