---
title: ForecastType ComplexType (Outlook Wetter Informationen-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Definiert die Parameter für die Vorhersage Wetter Formatierungen einen Speicherort an.
ms.openlocfilehash: 886c6cdbbeb9f07564854dc6a62cbcdad9703b62
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796091"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="64dea-103">ForecastType ComplexType (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="64dea-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="64dea-104">Definiert die Parameter für die Vorhersage Wetter Formatierungen einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="64dea-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="64dea-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="64dea-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="64dea-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="64dea-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="64dea-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="64dea-107">**Schema file**</span></span> <br/> |<span data-ttu-id="64dea-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="64dea-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="64dea-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="64dea-109">**Extension base**</span></span> <br/> |<span data-ttu-id="64dea-110">Keine</span><span class="sxs-lookup"><span data-stu-id="64dea-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="64dea-111">Definition</span><span class="sxs-lookup"><span data-stu-id="64dea-111">Definition</span></span>

```XML
       <xs:complexType name="forecastType">
     <xs:attribute name="shortday"   type="xs:string"      use="required"     />
     <xs:attribute name="day"   type="xs:string"      use="required"     />
     <xs:attribute name="date"   type="xs:date"      use="required"     />
     <xs:attribute name="precip"   type="xs:integer"      use="required"     />
     <xs:attribute name="skytextday"   type="xs:string"      use="required"     />
     <xs:attribute name="skycodeday"   type="xs:integer"      use="required"     />
     <xs:attribute name="high"   type="xs:integer"      use="required"     />
     <xs:attribute name="low"   type="xs:integer"      use="required"     />
       </xs:complexType>

```

## <a name="elements-and-attributes"></a><span data-ttu-id="64dea-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="64dea-112">Elements and attributes</span></span>

<span data-ttu-id="64dea-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="64dea-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="64dea-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="64dea-114">Child elements</span></span>

<span data-ttu-id="64dea-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="64dea-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="64dea-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="64dea-116">Attributes</span></span>

|<span data-ttu-id="64dea-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="64dea-117">**Attribute**</span></span>|<span data-ttu-id="64dea-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="64dea-118">**Type**</span></span>|<span data-ttu-id="64dea-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="64dea-119">**Required**</span></span>|<span data-ttu-id="64dea-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="64dea-120">**Description**</span></span>|<span data-ttu-id="64dea-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="64dea-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="64dea-122">date</span><span class="sxs-lookup"><span data-stu-id="64dea-122">date</span></span>  <br/> |<span data-ttu-id="64dea-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="64dea-123">xs:date</span></span>  <br/> |<span data-ttu-id="64dea-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64dea-124">required</span></span>  <br/> |<span data-ttu-id="64dea-125">Gibt das Datum für die Planung.</span><span class="sxs-lookup"><span data-stu-id="64dea-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="64dea-126">Ein Wert, der den Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="64dea-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="64dea-127">Tag</span><span class="sxs-lookup"><span data-stu-id="64dea-127">day</span></span>  <br/> |<span data-ttu-id="64dea-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="64dea-128">xs:string</span></span>  <br/> |<span data-ttu-id="64dea-129">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64dea-129">required</span></span>  <br/> |<span data-ttu-id="64dea-130">Gibt einen Tag für die Planung.</span><span class="sxs-lookup"><span data-stu-id="64dea-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="64dea-131">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="64dea-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="64dea-132">hohe</span><span class="sxs-lookup"><span data-stu-id="64dea-132">high</span></span>  <br/> |<span data-ttu-id="64dea-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="64dea-133">xs:integer</span></span>  <br/> |<span data-ttu-id="64dea-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64dea-134">required</span></span>  <br/> |<span data-ttu-id="64dea-135">Gibt die höchste prognostizierten Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="64dea-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="64dea-136">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="64dea-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="64dea-137">Niedrig</span><span class="sxs-lookup"><span data-stu-id="64dea-137">low</span></span>  <br/> |<span data-ttu-id="64dea-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="64dea-138">xs:integer</span></span>  <br/> |<span data-ttu-id="64dea-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64dea-139">required</span></span>  <br/> |<span data-ttu-id="64dea-140">Gibt die geplanten niedrigsten Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="64dea-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="64dea-141">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="64dea-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="64dea-142">precip</span><span class="sxs-lookup"><span data-stu-id="64dea-142">precip</span></span>  <br/> |<span data-ttu-id="64dea-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="64dea-143">xs:integer</span></span>  <br/> |<span data-ttu-id="64dea-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64dea-144">required</span></span>  <br/> |<span data-ttu-id="64dea-145">Gibt die Möglichkeit Prozentsatz Niederschlagsmenge an.</span><span class="sxs-lookup"><span data-stu-id="64dea-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="64dea-146">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="64dea-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="64dea-147">shortday</span><span class="sxs-lookup"><span data-stu-id="64dea-147">shortday</span></span>  <br/> |<span data-ttu-id="64dea-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="64dea-148">xs:string</span></span>  <br/> |<span data-ttu-id="64dea-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64dea-149">required</span></span>  <br/> |<span data-ttu-id="64dea-150">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="64dea-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="64dea-151">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="64dea-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="64dea-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="64dea-152">skycodeday</span></span>  <br/> |<span data-ttu-id="64dea-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="64dea-153">xs:integer</span></span>  <br/> |<span data-ttu-id="64dea-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64dea-154">required</span></span>  <br/> |<span data-ttu-id="64dea-155">Gibt einen Code für die geplanten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="64dea-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="64dea-156">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="64dea-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="64dea-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="64dea-157">skytextday</span></span>  <br/> |<span data-ttu-id="64dea-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="64dea-158">xs:string</span></span>  <br/> |<span data-ttu-id="64dea-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="64dea-159">required</span></span>  <br/> |<span data-ttu-id="64dea-160">Gibt ein bis zwei Wörter, die die geplanten Bedingungen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="64dea-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="64dea-161">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="64dea-161">A value of the type xs:string</span></span>  <br/> |
   

