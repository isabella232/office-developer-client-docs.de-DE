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
ms.openlocfilehash: 55ea2cfa6904d88c695268675bc7a893fa643010
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796096"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="195e3-103">CurrentType ComplexType (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="195e3-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="195e3-104">Definiert die Parameter über die aktuelle Wettervorhersage von einem Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="195e3-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="195e3-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="195e3-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="195e3-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="195e3-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="195e3-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="195e3-107">**Schema file**</span></span> <br/> |<span data-ttu-id="195e3-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="195e3-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="195e3-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="195e3-109">**Extension base**</span></span> <br/> |<span data-ttu-id="195e3-110">Keine</span><span class="sxs-lookup"><span data-stu-id="195e3-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="195e3-111">Definition</span><span class="sxs-lookup"><span data-stu-id="195e3-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="195e3-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="195e3-112">Elements and attributes</span></span>

<span data-ttu-id="195e3-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="195e3-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="195e3-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="195e3-114">Child elements</span></span>

<span data-ttu-id="195e3-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="195e3-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="195e3-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="195e3-116">Attributes</span></span>

|<span data-ttu-id="195e3-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="195e3-117">**Attribute**</span></span>|<span data-ttu-id="195e3-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="195e3-118">**Type**</span></span>|<span data-ttu-id="195e3-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="195e3-119">**Required**</span></span>|<span data-ttu-id="195e3-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="195e3-120">**Description**</span></span>|<span data-ttu-id="195e3-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="195e3-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="195e3-122">date</span><span class="sxs-lookup"><span data-stu-id="195e3-122">date</span></span>  <br/> |<span data-ttu-id="195e3-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="195e3-123">xs:date</span></span>  <br/> |<span data-ttu-id="195e3-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-124">required</span></span>  <br/> |<span data-ttu-id="195e3-125">Heutiges Datum angibt.</span><span class="sxs-lookup"><span data-stu-id="195e3-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="195e3-126">Ein Wert, der den Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="195e3-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="195e3-127">Tag</span><span class="sxs-lookup"><span data-stu-id="195e3-127">day</span></span>  <br/> |<span data-ttu-id="195e3-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="195e3-128">xs:string</span></span>  <br/> |<span data-ttu-id="195e3-129">Optional</span><span class="sxs-lookup"><span data-stu-id="195e3-129">optional</span></span>  <br/> |<span data-ttu-id="195e3-130">Gibt einen Tag für die Planung.</span><span class="sxs-lookup"><span data-stu-id="195e3-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="195e3-131">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="195e3-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="195e3-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="195e3-132">feelslike</span></span>  <br/> |<span data-ttu-id="195e3-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="195e3-133">xs:integer</span></span>  <br/> |<span data-ttu-id="195e3-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-134">required</span></span>  <br/> |<span data-ttu-id="195e3-135">Gibt die Temperatur des wie ist mit das aktuelle Wetter wie an.</span><span class="sxs-lookup"><span data-stu-id="195e3-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="195e3-136">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="195e3-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="195e3-137">Luftfeuchtigkeit</span><span class="sxs-lookup"><span data-stu-id="195e3-137">humidity</span></span>  <br/> |<span data-ttu-id="195e3-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="195e3-138">xs:integer</span></span>  <br/> |<span data-ttu-id="195e3-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-139">required</span></span>  <br/> |<span data-ttu-id="195e3-140">Gibt den aktuellen Luftfeuchtigkeit numerischen Wert.</span><span class="sxs-lookup"><span data-stu-id="195e3-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="195e3-141">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="195e3-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="195e3-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="195e3-142">observationpoint</span></span>  <br/> |<span data-ttu-id="195e3-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="195e3-143">xs:string</span></span>  <br/> |<span data-ttu-id="195e3-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-144">required</span></span>  <br/> |<span data-ttu-id="195e3-145">Gibt an, in dem die aktuelle Wetterinformationen aus beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="195e3-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="195e3-146">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="195e3-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="195e3-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="195e3-147">observationtime</span></span>  <br/> |<span data-ttu-id="195e3-148">xs: Time</span><span class="sxs-lookup"><span data-stu-id="195e3-148">xs:time</span></span>  <br/> |<span data-ttu-id="195e3-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-149">required</span></span>  <br/> |<span data-ttu-id="195e3-150">Gibt an, wenn die aktuelle Wetterinformationen unter beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="195e3-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="195e3-151">Ein Wert, der den Typ xs: Time</span><span class="sxs-lookup"><span data-stu-id="195e3-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="195e3-152">shortday</span><span class="sxs-lookup"><span data-stu-id="195e3-152">shortday</span></span>  <br/> |<span data-ttu-id="195e3-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="195e3-153">xs:string</span></span>  <br/> |<span data-ttu-id="195e3-154">Optional</span><span class="sxs-lookup"><span data-stu-id="195e3-154">optional</span></span>  <br/> |<span data-ttu-id="195e3-155">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="195e3-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="195e3-156">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="195e3-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="195e3-157">skycode</span><span class="sxs-lookup"><span data-stu-id="195e3-157">skycode</span></span>  <br/> |<span data-ttu-id="195e3-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="195e3-158">xs:integer</span></span>  <br/> |<span data-ttu-id="195e3-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-159">required</span></span>  <br/> |<span data-ttu-id="195e3-160">Gibt einen ganze Zahl Code für die aktuelle Wettervorhersage.</span><span class="sxs-lookup"><span data-stu-id="195e3-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="195e3-161">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="195e3-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="195e3-162">skytext</span><span class="sxs-lookup"><span data-stu-id="195e3-162">skytext</span></span>  <br/> |<span data-ttu-id="195e3-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="195e3-163">xs:string</span></span>  <br/> |<span data-ttu-id="195e3-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-164">required</span></span>  <br/> |<span data-ttu-id="195e3-165">Gibt ein bis zwei Wörter, die aktuelle Wetterbericht beschreibt.</span><span class="sxs-lookup"><span data-stu-id="195e3-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="195e3-166">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="195e3-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="195e3-167">Temperatur</span><span class="sxs-lookup"><span data-stu-id="195e3-167">temperature</span></span>  <br/> |<span data-ttu-id="195e3-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="195e3-168">xs:integer</span></span>  <br/> |<span data-ttu-id="195e3-169">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-169">required</span></span>  <br/> |<span data-ttu-id="195e3-170">Gibt die aktuelle Temperatur des Speicherorts an.</span><span class="sxs-lookup"><span data-stu-id="195e3-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="195e3-171">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="195e3-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="195e3-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="195e3-172">winddisplay</span></span>  <br/> |<span data-ttu-id="195e3-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="195e3-173">xs:string</span></span>  <br/> |<span data-ttu-id="195e3-174">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-174">required</span></span>  <br/> |<span data-ttu-id="195e3-175">Eine Zeichenfolge, die die aktuelle Wind Bedingungen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="195e3-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="195e3-176">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="195e3-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="195e3-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="195e3-177">windspeed</span></span>  <br/> |<span data-ttu-id="195e3-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="195e3-178">xs:integer</span></span>  <br/> |<span data-ttu-id="195e3-179">erforderlich</span><span class="sxs-lookup"><span data-stu-id="195e3-179">required</span></span>  <br/> |<span data-ttu-id="195e3-180">Gibt den aktuellen Wert der numerische Wind Geschwindigkeit.</span><span class="sxs-lookup"><span data-stu-id="195e3-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="195e3-181">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="195e3-181">A value of the type xs:integer</span></span>  <br/> |
   

