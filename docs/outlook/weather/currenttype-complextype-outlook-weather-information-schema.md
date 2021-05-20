---
title: currentType complexType (Outlook Wetterinformationsschema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Definiert die Parameter zu den aktuellen Wetterbedingungen eines Standorts.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540987"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="d9983-103">currentType complexType (Outlook Wetterinformationsschema)</span><span class="sxs-lookup"><span data-stu-id="d9983-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="d9983-104">Definiert die Parameter zu den aktuellen Wetterbedingungen eines Standorts.</span><span class="sxs-lookup"><span data-stu-id="d9983-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="d9983-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d9983-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d9983-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d9983-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="d9983-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d9983-107">**Schema file**</span></span> <br/> |<span data-ttu-id="d9983-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="d9983-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="d9983-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d9983-109">**Extension base**</span></span> <br/> |<span data-ttu-id="d9983-110">Keine</span><span class="sxs-lookup"><span data-stu-id="d9983-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d9983-111">Definition</span><span class="sxs-lookup"><span data-stu-id="d9983-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d9983-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d9983-112">Elements and attributes</span></span>

<span data-ttu-id="d9983-113">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d9983-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d9983-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d9983-114">Child elements</span></span>

<span data-ttu-id="d9983-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="d9983-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d9983-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="d9983-116">Attributes</span></span>

|<span data-ttu-id="d9983-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d9983-117">**Attribute**</span></span>|<span data-ttu-id="d9983-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d9983-118">**Type**</span></span>|<span data-ttu-id="d9983-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d9983-119">**Required**</span></span>|<span data-ttu-id="d9983-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d9983-120">**Description**</span></span>|<span data-ttu-id="d9983-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d9983-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d9983-122">date</span><span class="sxs-lookup"><span data-stu-id="d9983-122">date</span></span>  <br/> |<span data-ttu-id="d9983-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="d9983-123">xs:date</span></span>  <br/> |<span data-ttu-id="d9983-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-124">required</span></span>  <br/> |<span data-ttu-id="d9983-125">Gibt das heutige Datum an.</span><span class="sxs-lookup"><span data-stu-id="d9983-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="d9983-126">Ein Wert vom Typ xs:date</span><span class="sxs-lookup"><span data-stu-id="d9983-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="d9983-127">day</span><span class="sxs-lookup"><span data-stu-id="d9983-127">day</span></span>  <br/> |<span data-ttu-id="d9983-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-128">xs:string</span></span>  <br/> |<span data-ttu-id="d9983-129">Optional</span><span class="sxs-lookup"><span data-stu-id="d9983-129">optional</span></span>  <br/> |<span data-ttu-id="d9983-130">Gibt einen Tag für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="d9983-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="d9983-131">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d9983-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="d9983-132">feelslike</span></span>  <br/> |<span data-ttu-id="d9983-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-133">xs:integer</span></span>  <br/> |<span data-ttu-id="d9983-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-134">required</span></span>  <br/> |<span data-ttu-id="d9983-135">Gibt die Temperatur an, wie sich das aktuelle Wetter anfühlt.</span><span class="sxs-lookup"><span data-stu-id="d9983-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="d9983-136">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d9983-137">Feuchtigkeit</span><span class="sxs-lookup"><span data-stu-id="d9983-137">humidity</span></span>  <br/> |<span data-ttu-id="d9983-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-138">xs:integer</span></span>  <br/> |<span data-ttu-id="d9983-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-139">required</span></span>  <br/> |<span data-ttu-id="d9983-140">Gibt den aktuellen numerischen Feuchtigkeitswert an.</span><span class="sxs-lookup"><span data-stu-id="d9983-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="d9983-141">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d9983-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="d9983-142">observationpoint</span></span>  <br/> |<span data-ttu-id="d9983-143">xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-143">xs:string</span></span>  <br/> |<span data-ttu-id="d9983-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-144">required</span></span>  <br/> |<span data-ttu-id="d9983-145">Gibt an, wo die aktuellen Wetterinformationen beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="d9983-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="d9983-146">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d9983-147">observationtime</span><span class="sxs-lookup"><span data-stu-id="d9983-147">observationtime</span></span>  <br/> |<span data-ttu-id="d9983-148">xs:time</span><span class="sxs-lookup"><span data-stu-id="d9983-148">xs:time</span></span>  <br/> |<span data-ttu-id="d9983-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-149">required</span></span>  <br/> |<span data-ttu-id="d9983-150">Gibt an, wann die aktuellen Wetterinformationen beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="d9983-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="d9983-151">Ein Wert vom Typ xs:time</span><span class="sxs-lookup"><span data-stu-id="d9983-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="d9983-152">shortday</span><span class="sxs-lookup"><span data-stu-id="d9983-152">shortday</span></span>  <br/> |<span data-ttu-id="d9983-153">xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-153">xs:string</span></span>  <br/> |<span data-ttu-id="d9983-154">Optional</span><span class="sxs-lookup"><span data-stu-id="d9983-154">optional</span></span>  <br/> |<span data-ttu-id="d9983-155">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="d9983-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="d9983-156">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d9983-157">skycode</span><span class="sxs-lookup"><span data-stu-id="d9983-157">skycode</span></span>  <br/> |<span data-ttu-id="d9983-158">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-158">xs:integer</span></span>  <br/> |<span data-ttu-id="d9983-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-159">required</span></span>  <br/> |<span data-ttu-id="d9983-160">Gibt einen ganzzahligen Code für die aktuellen Wetterbedingungen an.</span><span class="sxs-lookup"><span data-stu-id="d9983-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="d9983-161">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d9983-162">skytext</span><span class="sxs-lookup"><span data-stu-id="d9983-162">skytext</span></span>  <br/> |<span data-ttu-id="d9983-163">xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-163">xs:string</span></span>  <br/> |<span data-ttu-id="d9983-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-164">required</span></span>  <br/> |<span data-ttu-id="d9983-165">Gibt ein bis zwei Wörter an, die aktuelle Wetterbedingungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d9983-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="d9983-166">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d9983-167">temperatur</span><span class="sxs-lookup"><span data-stu-id="d9983-167">temperature</span></span>  <br/> |<span data-ttu-id="d9983-168">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-168">xs:integer</span></span>  <br/> |<span data-ttu-id="d9983-169">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-169">required</span></span>  <br/> |<span data-ttu-id="d9983-170">Gibt die aktuelle Temperatur des Standorts an.</span><span class="sxs-lookup"><span data-stu-id="d9983-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="d9983-171">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d9983-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="d9983-172">winddisplay</span></span>  <br/> |<span data-ttu-id="d9983-173">xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-173">xs:string</span></span>  <br/> |<span data-ttu-id="d9983-174">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-174">required</span></span>  <br/> |<span data-ttu-id="d9983-175">Eine Zeichenfolge, die die aktuellen Windbedingungen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d9983-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="d9983-176">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="d9983-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d9983-177">windspeed</span><span class="sxs-lookup"><span data-stu-id="d9983-177">windspeed</span></span>  <br/> |<span data-ttu-id="d9983-178">xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-178">xs:integer</span></span>  <br/> |<span data-ttu-id="d9983-179">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d9983-179">required</span></span>  <br/> |<span data-ttu-id="d9983-180">Gibt den aktuellen numerischen Windgeschwindigkeitswert an.</span><span class="sxs-lookup"><span data-stu-id="d9983-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="d9983-181">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="d9983-181">A value of the type xs:integer</span></span>  <br/> |
   

