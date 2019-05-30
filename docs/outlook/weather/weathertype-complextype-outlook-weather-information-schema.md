---
title: weathertype complexType (Outlook-Wetter Informations Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b94d848e-868a-5d5e-ad82-39ed9bd5b357
description: Gibt die Wetterbedingungen eines Standorts an.
ms.openlocfilehash: ac7b8f37e71da203db0f6aefc8e20b29e810c3cf
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542947"
---
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="85553-103">weathertype complexType (Outlook-Wetter Informations Schema)</span><span class="sxs-lookup"><span data-stu-id="85553-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="85553-104">Gibt die Wetterbedingungen eines Standorts an.</span><span class="sxs-lookup"><span data-stu-id="85553-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="85553-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="85553-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85553-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="85553-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="85553-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="85553-107">**Schema file**</span></span> <br/> |<span data-ttu-id="85553-108">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="85553-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="85553-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="85553-109">**Extension base**</span></span> <br/> |<span data-ttu-id="85553-110">Keine</span><span class="sxs-lookup"><span data-stu-id="85553-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="85553-111">Definition</span><span class="sxs-lookup"><span data-stu-id="85553-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="85553-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="85553-112">Elements and attributes</span></span>

<span data-ttu-id="85553-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="85553-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="85553-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85553-114">Child elements</span></span>

|<span data-ttu-id="85553-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="85553-115">**Element**</span></span>|<span data-ttu-id="85553-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="85553-116">**Type**</span></span>|<span data-ttu-id="85553-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85553-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="85553-118">aktuellen</span><span class="sxs-lookup"><span data-stu-id="85553-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="85553-119">currentType</span><span class="sxs-lookup"><span data-stu-id="85553-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="85553-120">Gibt die aktuellen Wetterbedingungen an.</span><span class="sxs-lookup"><span data-stu-id="85553-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="85553-121">Prognose</span><span class="sxs-lookup"><span data-stu-id="85553-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="85553-122">forecasttype</span><span class="sxs-lookup"><span data-stu-id="85553-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="85553-123">Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: heute, morgen, Tag nach morgen.</span><span class="sxs-lookup"><span data-stu-id="85553-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="85553-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="85553-124">Attributes</span></span>

|<span data-ttu-id="85553-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="85553-125">**Attribute**</span></span>|<span data-ttu-id="85553-126">**Typ**</span><span class="sxs-lookup"><span data-stu-id="85553-126">**Type**</span></span>|<span data-ttu-id="85553-127">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="85553-127">**Required**</span></span>|<span data-ttu-id="85553-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85553-128">**Description**</span></span>|<span data-ttu-id="85553-129">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="85553-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="85553-130">Attribution</span><span class="sxs-lookup"><span data-stu-id="85553-130">attribution</span></span>  <br/> |<span data-ttu-id="85553-131">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85553-131">xs:string</span></span>  <br/> |<span data-ttu-id="85553-132">erforderlich</span><span class="sxs-lookup"><span data-stu-id="85553-132">required</span></span>  <br/> |<span data-ttu-id="85553-133">Gibt die Quelle der Wetterinformationen an.</span><span class="sxs-lookup"><span data-stu-id="85553-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="85553-134">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="85553-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="85553-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="85553-135">degreetype</span></span>  <br/> |<span data-ttu-id="85553-136">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85553-136">xs:string</span></span>  <br/> |<span data-ttu-id="85553-137">erforderlich</span><span class="sxs-lookup"><span data-stu-id="85553-137">required</span></span>  <br/> |<span data-ttu-id="85553-138">Gibt die Einheit für die Temperatur des Standorts an, beispielsweise Celsius.</span><span class="sxs-lookup"><span data-stu-id="85553-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="85553-139">C, F</span><span class="sxs-lookup"><span data-stu-id="85553-139">C, F</span></span>  <br/> |
|<span data-ttu-id="85553-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="85553-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="85553-141">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85553-141">xs:string</span></span>  <br/> |<span data-ttu-id="85553-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="85553-142">required</span></span>  <br/> |<span data-ttu-id="85553-143">Gibt die URL des Bilds für den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="85553-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="85553-144">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="85553-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="85553-145">TimeZone</span><span class="sxs-lookup"><span data-stu-id="85553-145">timezone</span></span>  <br/> |<span data-ttu-id="85553-146">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="85553-146">xs:integer</span></span>  <br/> |<span data-ttu-id="85553-147">erforderlich</span><span class="sxs-lookup"><span data-stu-id="85553-147">required</span></span>  <br/> |<span data-ttu-id="85553-148">Gibt den GMT-Offset an.</span><span class="sxs-lookup"><span data-stu-id="85553-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="85553-149">Ein Wert zwischen-11 und 12 inklusive</span><span class="sxs-lookup"><span data-stu-id="85553-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="85553-150">url</span><span class="sxs-lookup"><span data-stu-id="85553-150">url</span></span>  <br/> |<span data-ttu-id="85553-151">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85553-151">xs:string</span></span>  <br/> |<span data-ttu-id="85553-152">erforderlich</span><span class="sxs-lookup"><span data-stu-id="85553-152">required</span></span>  <br/> |<span data-ttu-id="85553-153">Gibt die URL für die Webseite des Wetter Diensts an, die Wetterinformationen für den angegebenen Speicherort enthält.</span><span class="sxs-lookup"><span data-stu-id="85553-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="85553-154">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="85553-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="85553-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="85553-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="85553-156">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85553-156">xs:string</span></span>  <br/> |<span data-ttu-id="85553-157">erforderlich</span><span class="sxs-lookup"><span data-stu-id="85553-157">required</span></span>  <br/> |<span data-ttu-id="85553-158">Gibt den Code an, der dem Speicherort zugeordnet ist, der verwendet wird, um mehrere Standorte mit demselben Namen zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="85553-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="85553-159">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="85553-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="85553-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="85553-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="85553-161">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="85553-161">xs:string</span></span>  <br/> |<span data-ttu-id="85553-162">erforderlich</span><span class="sxs-lookup"><span data-stu-id="85553-162">required</span></span>  <br/> |<span data-ttu-id="85553-163">Gibt den Namen des Speicherorts an, der im Dropdown-Steuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="85553-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="85553-164">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="85553-164">A value of the type xs:string</span></span>  <br/> |
   

