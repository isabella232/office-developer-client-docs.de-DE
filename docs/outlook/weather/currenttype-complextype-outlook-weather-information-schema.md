---
title: CurrentType complexType (Outlook-Wetter Informations Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9f4663ac-13d3-6c46-f839-ba6bca4047a3
description: Definiert die Parameter für die aktuellen Wetterbedingungen eines Standorts.
ms.openlocfilehash: 6dec923ce45ddc6470d80e1c973528246e01672f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540987"
---
# <a name="currenttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="00561-103">CurrentType complexType (Outlook-Wetter Informations Schema)</span><span class="sxs-lookup"><span data-stu-id="00561-103">currentType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="00561-104">Definiert die Parameter für die aktuellen Wetterbedingungen eines Standorts.</span><span class="sxs-lookup"><span data-stu-id="00561-104">Defines the parameters about the current weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="00561-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="00561-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00561-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="00561-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="00561-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="00561-107">**Schema file**</span></span> <br/> |<span data-ttu-id="00561-108">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="00561-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="00561-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="00561-109">**Extension base**</span></span> <br/> |<span data-ttu-id="00561-110">Keine</span><span class="sxs-lookup"><span data-stu-id="00561-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="00561-111">Definition</span><span class="sxs-lookup"><span data-stu-id="00561-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="00561-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="00561-112">Elements and attributes</span></span>

<span data-ttu-id="00561-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="00561-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="00561-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00561-114">Child elements</span></span>

<span data-ttu-id="00561-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="00561-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00561-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="00561-116">Attributes</span></span>

|<span data-ttu-id="00561-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="00561-117">**Attribute**</span></span>|<span data-ttu-id="00561-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="00561-118">**Type**</span></span>|<span data-ttu-id="00561-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="00561-119">**Required**</span></span>|<span data-ttu-id="00561-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00561-120">**Description**</span></span>|<span data-ttu-id="00561-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="00561-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="00561-122">date</span><span class="sxs-lookup"><span data-stu-id="00561-122">date</span></span>  <br/> |<span data-ttu-id="00561-123">xs: Datum</span><span class="sxs-lookup"><span data-stu-id="00561-123">xs:date</span></span>  <br/> |<span data-ttu-id="00561-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-124">required</span></span>  <br/> |<span data-ttu-id="00561-125">Gibt das heutige Datum an.</span><span class="sxs-lookup"><span data-stu-id="00561-125">Specifies today's date.</span></span>  <br/> |<span data-ttu-id="00561-126">Ein Wert vom Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="00561-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="00561-127">Tag</span><span class="sxs-lookup"><span data-stu-id="00561-127">day</span></span>  <br/> |<span data-ttu-id="00561-128">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00561-128">xs:string</span></span>  <br/> |<span data-ttu-id="00561-129">Optional</span><span class="sxs-lookup"><span data-stu-id="00561-129">optional</span></span>  <br/> |<span data-ttu-id="00561-130">Gibt einen Tag für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="00561-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="00561-131">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="00561-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="00561-132">feelslike</span><span class="sxs-lookup"><span data-stu-id="00561-132">feelslike</span></span>  <br/> |<span data-ttu-id="00561-133">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-133">xs:integer</span></span>  <br/> |<span data-ttu-id="00561-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-134">required</span></span>  <br/> |<span data-ttu-id="00561-135">Gibt die Temperatur an, wie sich das aktuelle Wetter anfühlt.</span><span class="sxs-lookup"><span data-stu-id="00561-135">Specifies the temperature of how the current weather feels like.</span></span>  <br/> |<span data-ttu-id="00561-136">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="00561-137">Luftfeuchtigkeits</span><span class="sxs-lookup"><span data-stu-id="00561-137">humidity</span></span>  <br/> |<span data-ttu-id="00561-138">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-138">xs:integer</span></span>  <br/> |<span data-ttu-id="00561-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-139">required</span></span>  <br/> |<span data-ttu-id="00561-140">Gibt den aktuellen numerischen Feuchtewert an.</span><span class="sxs-lookup"><span data-stu-id="00561-140">Specifies the current numerical humidity value.</span></span>  <br/> |<span data-ttu-id="00561-141">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="00561-142">observationpoint</span><span class="sxs-lookup"><span data-stu-id="00561-142">observationpoint</span></span>  <br/> |<span data-ttu-id="00561-143">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00561-143">xs:string</span></span>  <br/> |<span data-ttu-id="00561-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-144">required</span></span>  <br/> |<span data-ttu-id="00561-145">Gibt an, von wo die aktuellen Wetterinformationen beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="00561-145">Specifies where the current weather information is observed from.</span></span>  <br/> |<span data-ttu-id="00561-146">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="00561-146">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="00561-147">Beobachtungszeit</span><span class="sxs-lookup"><span data-stu-id="00561-147">observationtime</span></span>  <br/> |<span data-ttu-id="00561-148">xs: Zeit</span><span class="sxs-lookup"><span data-stu-id="00561-148">xs:time</span></span>  <br/> |<span data-ttu-id="00561-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-149">required</span></span>  <br/> |<span data-ttu-id="00561-150">Gibt an, wann die aktuellen Wetterinformationen bei beobachtet werden.</span><span class="sxs-lookup"><span data-stu-id="00561-150">Specifies when the current weather information is observed at.</span></span>  <br/> |<span data-ttu-id="00561-151">Ein Wert vom Typ xs: Time</span><span class="sxs-lookup"><span data-stu-id="00561-151">A value of the type xs:time</span></span>  <br/> |
|<span data-ttu-id="00561-152">shortday</span><span class="sxs-lookup"><span data-stu-id="00561-152">shortday</span></span>  <br/> |<span data-ttu-id="00561-153">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00561-153">xs:string</span></span>  <br/> |<span data-ttu-id="00561-154">Optional</span><span class="sxs-lookup"><span data-stu-id="00561-154">optional</span></span>  <br/> |<span data-ttu-id="00561-155">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="00561-155">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="00561-156">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="00561-156">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="00561-157">skycode</span><span class="sxs-lookup"><span data-stu-id="00561-157">skycode</span></span>  <br/> |<span data-ttu-id="00561-158">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-158">xs:integer</span></span>  <br/> |<span data-ttu-id="00561-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-159">required</span></span>  <br/> |<span data-ttu-id="00561-160">Gibt einen ganzzahligen Code für die aktuellen Wetterbedingungen an.</span><span class="sxs-lookup"><span data-stu-id="00561-160">Specifies an integer code for the current weather conditions.</span></span>  <br/> |<span data-ttu-id="00561-161">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-161">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="00561-162">skytext</span><span class="sxs-lookup"><span data-stu-id="00561-162">skytext</span></span>  <br/> |<span data-ttu-id="00561-163">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00561-163">xs:string</span></span>  <br/> |<span data-ttu-id="00561-164">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-164">required</span></span>  <br/> |<span data-ttu-id="00561-165">Gibt ein bis zwei Wörter an, die die aktuellen Wetterbedingungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="00561-165">Specifies one to two words describing current weather conditions.</span></span>  <br/> |<span data-ttu-id="00561-166">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="00561-166">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="00561-167">Temperatur</span><span class="sxs-lookup"><span data-stu-id="00561-167">temperature</span></span>  <br/> |<span data-ttu-id="00561-168">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-168">xs:integer</span></span>  <br/> |<span data-ttu-id="00561-169">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-169">required</span></span>  <br/> |<span data-ttu-id="00561-170">Gibt die aktuelle Temperatur des Standorts an.</span><span class="sxs-lookup"><span data-stu-id="00561-170">Specifies the current temperature of the location.</span></span>  <br/> |<span data-ttu-id="00561-171">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-171">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="00561-172">winddisplay</span><span class="sxs-lookup"><span data-stu-id="00561-172">winddisplay</span></span>  <br/> |<span data-ttu-id="00561-173">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="00561-173">xs:string</span></span>  <br/> |<span data-ttu-id="00561-174">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-174">required</span></span>  <br/> |<span data-ttu-id="00561-175">Eine Zeichenfolge, die die aktuellen Windbedingungen beschreibt.</span><span class="sxs-lookup"><span data-stu-id="00561-175">A string that describes the current wind conditions.</span></span>  <br/> |<span data-ttu-id="00561-176">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="00561-176">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="00561-177">WindSpeed</span><span class="sxs-lookup"><span data-stu-id="00561-177">windspeed</span></span>  <br/> |<span data-ttu-id="00561-178">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-178">xs:integer</span></span>  <br/> |<span data-ttu-id="00561-179">erforderlich</span><span class="sxs-lookup"><span data-stu-id="00561-179">required</span></span>  <br/> |<span data-ttu-id="00561-180">Gibt den aktuellen numerischen Wind Geschwindigkeitswert an.</span><span class="sxs-lookup"><span data-stu-id="00561-180">Specifies the current numerical wind speed value.</span></span>  <br/> |<span data-ttu-id="00561-181">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="00561-181">A value of the type xs:integer</span></span>  <br/> |
   

