---
title: weatherType complexType (Outlook Wetterinformationsschema)
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
# <a name="weathertype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="88524-103">weatherType complexType (Outlook Wetterinformationsschema)</span><span class="sxs-lookup"><span data-stu-id="88524-103">weatherType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="88524-104">Gibt die Wetterbedingungen eines Standorts an.</span><span class="sxs-lookup"><span data-stu-id="88524-104">Specifies the weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="88524-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="88524-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="88524-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="88524-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="88524-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="88524-107">**Schema file**</span></span> <br/> |<span data-ttu-id="88524-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="88524-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="88524-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="88524-109">**Extension base**</span></span> <br/> |<span data-ttu-id="88524-110">Keine</span><span class="sxs-lookup"><span data-stu-id="88524-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="88524-111">Definition</span><span class="sxs-lookup"><span data-stu-id="88524-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="88524-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="88524-112">Elements and attributes</span></span>

<span data-ttu-id="88524-113">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="88524-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="88524-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="88524-114">Child elements</span></span>

|<span data-ttu-id="88524-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="88524-115">**Element**</span></span>|<span data-ttu-id="88524-116">**Typ**</span><span class="sxs-lookup"><span data-stu-id="88524-116">**Type**</span></span>|<span data-ttu-id="88524-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88524-117">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="88524-118">current</span><span class="sxs-lookup"><span data-stu-id="88524-118">current</span></span>](current-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="88524-119">currentType</span><span class="sxs-lookup"><span data-stu-id="88524-119">currentType</span></span>](currenttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="88524-120">Gibt die aktuellen Wetterbedingungen an.</span><span class="sxs-lookup"><span data-stu-id="88524-120">Specifies the current weather conditions.</span></span>  <br/> |
|[<span data-ttu-id="88524-121">forecast</span><span class="sxs-lookup"><span data-stu-id="88524-121">forecast</span></span>](forecast-element-weathertype-complextypeoutlook-weather-information-schema.md) <br/> |[<span data-ttu-id="88524-122">forecastType</span><span class="sxs-lookup"><span data-stu-id="88524-122">forecastType</span></span>](forecasttype-complextype-outlook-weather-information-schema.md) <br/> |<span data-ttu-id="88524-123">Gibt die zukünftigen Wetterbedingungen von mindestens drei Tagen voraus, einschließlich heute: Heute, Morgen, Tag nach Morgen.</span><span class="sxs-lookup"><span data-stu-id="88524-123">Specifies the future weather conditions of at least three days ahead including today: Today, Tomorrow, Day after Tomorrow.</span></span>  <br/> |
   
### <a name="attributes"></a><span data-ttu-id="88524-124">Attribute</span><span class="sxs-lookup"><span data-stu-id="88524-124">Attributes</span></span>

|<span data-ttu-id="88524-125">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="88524-125">**Attribute**</span></span>|<span data-ttu-id="88524-126">**Typ**</span><span class="sxs-lookup"><span data-stu-id="88524-126">**Type**</span></span>|<span data-ttu-id="88524-127">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="88524-127">**Required**</span></span>|<span data-ttu-id="88524-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="88524-128">**Description**</span></span>|<span data-ttu-id="88524-129">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="88524-129">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="88524-130">attribution</span><span class="sxs-lookup"><span data-stu-id="88524-130">attribution</span></span>  <br/> |<span data-ttu-id="88524-131">xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-131">xs:string</span></span>  <br/> |<span data-ttu-id="88524-132">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88524-132">required</span></span>  <br/> |<span data-ttu-id="88524-133">Gibt die Quelle der Wetterinformationen an.</span><span class="sxs-lookup"><span data-stu-id="88524-133">Specifies the source of the weather information.</span></span>  <br/> |<span data-ttu-id="88524-134">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-134">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="88524-135">degreetype</span><span class="sxs-lookup"><span data-stu-id="88524-135">degreetype</span></span>  <br/> |<span data-ttu-id="88524-136">xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-136">xs:string</span></span>  <br/> |<span data-ttu-id="88524-137">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88524-137">required</span></span>  <br/> |<span data-ttu-id="88524-138">Gibt die Einheit für die Temperatur des Standorts an, z. B. "Celsius".</span><span class="sxs-lookup"><span data-stu-id="88524-138">Specifies the unit for the temperature of the location for example, Celsius.</span></span>  <br/> |<span data-ttu-id="88524-139">C, F</span><span class="sxs-lookup"><span data-stu-id="88524-139">C, F</span></span>  <br/> |
|<span data-ttu-id="88524-140">imagerelativeurl</span><span class="sxs-lookup"><span data-stu-id="88524-140">imagerelativeurl</span></span>  <br/> |<span data-ttu-id="88524-141">xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-141">xs:string</span></span>  <br/> |<span data-ttu-id="88524-142">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88524-142">required</span></span>  <br/> |<span data-ttu-id="88524-143">Gibt die URL des Bilds für den Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="88524-143">Specifies the URL of the image for the location.</span></span>  <br/> |<span data-ttu-id="88524-144">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-144">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="88524-145">Zeitzone</span><span class="sxs-lookup"><span data-stu-id="88524-145">timezone</span></span>  <br/> |<span data-ttu-id="88524-146">xs:integer</span><span class="sxs-lookup"><span data-stu-id="88524-146">xs:integer</span></span>  <br/> |<span data-ttu-id="88524-147">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88524-147">required</span></span>  <br/> |<span data-ttu-id="88524-148">Gibt den GMT-Offset an.</span><span class="sxs-lookup"><span data-stu-id="88524-148">Specifies the GMT offset.</span></span>  <br/> |<span data-ttu-id="88524-149">Ein Wert zwischen -11 und einschließlich 12</span><span class="sxs-lookup"><span data-stu-id="88524-149">A value between -11 and 12 inclusive</span></span>  <br/> |
|<span data-ttu-id="88524-150">url</span><span class="sxs-lookup"><span data-stu-id="88524-150">url</span></span>  <br/> |<span data-ttu-id="88524-151">xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-151">xs:string</span></span>  <br/> |<span data-ttu-id="88524-152">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88524-152">required</span></span>  <br/> |<span data-ttu-id="88524-153">Gibt die URL für die Webseite des Wetterdiensts an, die Wetterinformationen für den angegebenen Standort enthält.</span><span class="sxs-lookup"><span data-stu-id="88524-153">Specifies the URL for the web page of the weather service that contains weather information for the specified location.</span></span>  <br/> |<span data-ttu-id="88524-154">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-154">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="88524-155">weatherlocationcode</span><span class="sxs-lookup"><span data-stu-id="88524-155">weatherlocationcode</span></span>  <br/> |<span data-ttu-id="88524-156">xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-156">xs:string</span></span>  <br/> |<span data-ttu-id="88524-157">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88524-157">required</span></span>  <br/> |<span data-ttu-id="88524-158">Gibt den Code an, der dem Speicherort zugeordnet ist, der zum Unterscheiden mehrerer Speicherorte mit demselben Namen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="88524-158">Specifies the code that is associated with the location used to distinguish multiple location that have the same name.</span></span>  <br/> |<span data-ttu-id="88524-159">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-159">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="88524-160">weatherlocationname</span><span class="sxs-lookup"><span data-stu-id="88524-160">weatherlocationname</span></span>  <br/> |<span data-ttu-id="88524-161">xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-161">xs:string</span></span>  <br/> |<span data-ttu-id="88524-162">erforderlich</span><span class="sxs-lookup"><span data-stu-id="88524-162">required</span></span>  <br/> |<span data-ttu-id="88524-163">Gibt den Namen des Speicherorts an, der im Dropdownsteuerelement angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="88524-163">Specifies the name of the location that appears in the drop-down control.</span></span>  <br/> |<span data-ttu-id="88524-164">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="88524-164">A value of the type xs:string</span></span>  <br/> |
   

