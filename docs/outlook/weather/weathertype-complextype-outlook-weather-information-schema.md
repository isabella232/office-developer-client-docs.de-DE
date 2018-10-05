---
title: WeatherType ComplexType (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Gibt die Wetterbedingungen einen Speicherort an.
ms.openlocfilehash: ffa91c4982b5703041c79b47eb15a3a2b845b429
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25398766"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="0b3c1-103">WeatherType ComplexType (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="0b3c1-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="0b3c1-104">Gibt die Wetterbedingungen einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="0b3c1-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="0b3c1-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0b3c1-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="0b3c1-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-107">**Schema file**</span></span> <br/> |<span data-ttu-id="0b3c1-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="0b3c1-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="0b3c1-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-109">**Extension base**</span></span> <br/> |<span data-ttu-id="0b3c1-110">Keine</span><span class="sxs-lookup"><span data-stu-id="0b3c1-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="0b3c1-111">Definition</span><span class="sxs-lookup"><span data-stu-id="0b3c1-111">Definition</span></span>

```XML
           <xs:complexType name="weatherType">
           <xs:sequence>
     <xs:element name="current"      type="currentType">
  </xs:element>  
     <xs:element name="forecast"      type="forecastType" minOccurs="3"     maxOccurs="unbounded"    >
  </xs:element>  
       </xs:sequence>
     <xs:attribute name="weatherlocationcode"   type="xs:string"      use="required"     />
     <xs:attribute name="timezone"   type="xs:integer"      use="required"     />
     <xs:attribute name="attribution"   type="xs:string"      use="required"     />
     <xs:attribute name="degreetype"   type="xs:string"      use="required"     />
     <xs:attribute name="imagerelativeurl"   type="xs:string"      use="required"     />
     <xs:attribute name="url"   type="xs:string"      use="required"     />
     <xs:attribute name="weatherlocationname"   type="xs:string"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="0b3c1-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="0b3c1-112">Elements and attributes</span></span>

<span data-ttu-id="0b3c1-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="0b3c1-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0b3c1-114">Child elements</span></span>

|<span data-ttu-id="0b3c1-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-115">**Element**</span></span>|<span data-ttu-id="0b3c1-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-116">**Type**</span></span>|<span data-ttu-id="0b3c1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="0b3c1-118">aktuelle</span><span class="sxs-lookup"><span data-stu-id="0b3c1-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="0b3c1-119">currentType</span><span class="sxs-lookup"><span data-stu-id="0b3c1-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="0b3c1-120">Gibt die aktuelle Wettervorhersage an.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="0b3c1-121">Planung</span><span class="sxs-lookup"><span data-stu-id="0b3c1-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="0b3c1-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="0b3c1-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="0b3c1-123">Gibt an, die Wetterbedingungen zukünftigen mindestens drei Tage im Voraus einschließlich heute: heute, morgen, übermorgen.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="0b3c1-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="0b3c1-124">Attributes</span></span>

|<span data-ttu-id="0b3c1-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-125">**Attribute**</span></span>|<span data-ttu-id="0b3c1-126">**Typ**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-126">**Type**</span></span>|<span data-ttu-id="0b3c1-127">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-127">**Required**</span></span>|<span data-ttu-id="0b3c1-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-128">**Description**</span></span>|<span data-ttu-id="0b3c1-129">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="0b3c1-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="0b3c1-130">Zuweisung</span><span class="sxs-lookup"><span data-stu-id="0b3c1-130">attribution</span></span>  <br/> |<span data-ttu-id="0b3c1-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b3c1-131">xs:string</span></span>  <br/> |<span data-ttu-id="0b3c1-132">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b3c1-132">required</span></span>  <br/> |<span data-ttu-id="0b3c1-133">Gibt die Quelle der Wetterinformationen.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="0b3c1-134">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0b3c1-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0b3c1-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="0b3c1-135">degreetype</span></span>  <br/> |<span data-ttu-id="0b3c1-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b3c1-136">xs:string</span></span>  <br/> |<span data-ttu-id="0b3c1-137">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b3c1-137">required</span></span>  <br/> |<span data-ttu-id="0b3c1-138">Gibt die Maßeinheit für die Temperatur des Speicherorts beispielsweise Celsius.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="0b3c1-139">C, F</span><span class="sxs-lookup"><span data-stu-id="0b3c1-139">C, F</span></span>  <br/> |
|<span data-ttu-id="0b3c1-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="0b3c1-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="0b3c1-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b3c1-141">xs:string</span></span>  <br/> |<span data-ttu-id="0b3c1-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b3c1-142">required</span></span>  <br/> |<span data-ttu-id="0b3c1-143">Gibt die URL des Bilds für den Speicherort.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="0b3c1-144">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0b3c1-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0b3c1-145">Zeitzone</span><span class="sxs-lookup"><span data-stu-id="0b3c1-145">timezone</span></span>  <br/> |<span data-ttu-id="0b3c1-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="0b3c1-146">xs:integer</span></span>  <br/> |<span data-ttu-id="0b3c1-147">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b3c1-147">required</span></span>  <br/> |<span data-ttu-id="0b3c1-148">Gibt den Offset GMT.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="0b3c1-149">Ein Wert zwischen-11 und 12 inklusive</span><span class="sxs-lookup"><span data-stu-id="0b3c1-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="0b3c1-150">url</span><span class="sxs-lookup"><span data-stu-id="0b3c1-150">url</span></span>  <br/> |<span data-ttu-id="0b3c1-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b3c1-151">xs:string</span></span>  <br/> |<span data-ttu-id="0b3c1-152">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b3c1-152">required</span></span>  <br/> |<span data-ttu-id="0b3c1-153">Gibt die URL für die Webseite des Diensts Wetter, die für den angegebenen Speicherort Wetterinformationen enthält.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="0b3c1-154">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0b3c1-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0b3c1-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="0b3c1-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="0b3c1-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b3c1-156">xs:string</span></span>  <br/> |<span data-ttu-id="0b3c1-157">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b3c1-157">required</span></span>  <br/> |<span data-ttu-id="0b3c1-158">Gibt den Code, der mit dem Speicherort zum unterscheiden von mehreren Standorten mit dem gleichen Namen zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="0b3c1-159">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0b3c1-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="0b3c1-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="0b3c1-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="0b3c1-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="0b3c1-161">xs:string</span></span>  <br/> |<span data-ttu-id="0b3c1-162">erforderlich</span><span class="sxs-lookup"><span data-stu-id="0b3c1-162">required</span></span>  <br/> |<span data-ttu-id="0b3c1-163">Gibt den Namen des Speicherorts, der angezeigt wird im Dropdown-Steuerelement.</span><span class="sxs-lookup"><span data-stu-id="0b3c1-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="0b3c1-164">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="0b3c1-164">A value of the type xs:string</span></span>  <br/> |
   

