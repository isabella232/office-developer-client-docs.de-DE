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
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390625"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="86e69-103">ForecastType ComplexType (Outlook Wetter Informationen-Schema)</span><span class="sxs-lookup"><span data-stu-id="86e69-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="86e69-104">Definiert die Parameter für die Vorhersage Wetter Formatierungen einen Speicherort an.</span><span class="sxs-lookup"><span data-stu-id="86e69-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="86e69-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="86e69-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="86e69-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="86e69-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="86e69-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="86e69-107">**Schema file**</span></span> <br/> |<span data-ttu-id="86e69-108">GetWeatherInfo.xsd</span><span class="sxs-lookup"><span data-stu-id="86e69-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="86e69-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="86e69-109">**Extension base**</span></span> <br/> |<span data-ttu-id="86e69-110">Keine</span><span class="sxs-lookup"><span data-stu-id="86e69-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="86e69-111">Definition</span><span class="sxs-lookup"><span data-stu-id="86e69-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="86e69-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="86e69-112">Elements and attributes</span></span>

<span data-ttu-id="86e69-113">Wenn das Schema spezifische Anforderungen, beispielsweise **Abfolge**, **MinOccurs**, **MaxOccurs**und **Wahl**, definiert finden Sie im Definitionsabschnitt.</span><span class="sxs-lookup"><span data-stu-id="86e69-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="86e69-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="86e69-114">Child elements</span></span>

<span data-ttu-id="86e69-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="86e69-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="86e69-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="86e69-116">Attributes</span></span>

|<span data-ttu-id="86e69-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="86e69-117">**Attribute**</span></span>|<span data-ttu-id="86e69-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="86e69-118">**Type**</span></span>|<span data-ttu-id="86e69-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="86e69-119">**Required**</span></span>|<span data-ttu-id="86e69-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="86e69-120">**Description**</span></span>|<span data-ttu-id="86e69-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="86e69-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="86e69-122">date</span><span class="sxs-lookup"><span data-stu-id="86e69-122">date</span></span>  <br/> |<span data-ttu-id="86e69-123">xs: Date</span><span class="sxs-lookup"><span data-stu-id="86e69-123">xs:date</span></span>  <br/> |<span data-ttu-id="86e69-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="86e69-124">required</span></span>  <br/> |<span data-ttu-id="86e69-125">Gibt das Datum für die Planung.</span><span class="sxs-lookup"><span data-stu-id="86e69-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="86e69-126">Ein Wert, der den Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="86e69-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="86e69-127">Tag</span><span class="sxs-lookup"><span data-stu-id="86e69-127">day</span></span>  <br/> |<span data-ttu-id="86e69-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="86e69-128">xs:string</span></span>  <br/> |<span data-ttu-id="86e69-129">erforderlich</span><span class="sxs-lookup"><span data-stu-id="86e69-129">required</span></span>  <br/> |<span data-ttu-id="86e69-130">Gibt einen Tag für die Planung.</span><span class="sxs-lookup"><span data-stu-id="86e69-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="86e69-131">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="86e69-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="86e69-132">hohe</span><span class="sxs-lookup"><span data-stu-id="86e69-132">high</span></span>  <br/> |<span data-ttu-id="86e69-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="86e69-133">xs:integer</span></span>  <br/> |<span data-ttu-id="86e69-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="86e69-134">required</span></span>  <br/> |<span data-ttu-id="86e69-135">Gibt die höchste prognostizierten Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="86e69-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="86e69-136">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="86e69-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="86e69-137">Niedrig</span><span class="sxs-lookup"><span data-stu-id="86e69-137">low</span></span>  <br/> |<span data-ttu-id="86e69-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="86e69-138">xs:integer</span></span>  <br/> |<span data-ttu-id="86e69-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="86e69-139">required</span></span>  <br/> |<span data-ttu-id="86e69-140">Gibt die geplanten niedrigsten Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="86e69-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="86e69-141">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="86e69-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="86e69-142">precip</span><span class="sxs-lookup"><span data-stu-id="86e69-142">precip</span></span>  <br/> |<span data-ttu-id="86e69-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="86e69-143">xs:integer</span></span>  <br/> |<span data-ttu-id="86e69-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="86e69-144">required</span></span>  <br/> |<span data-ttu-id="86e69-145">Gibt die Möglichkeit Prozentsatz Niederschlagsmenge an.</span><span class="sxs-lookup"><span data-stu-id="86e69-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="86e69-146">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="86e69-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="86e69-147">shortday</span><span class="sxs-lookup"><span data-stu-id="86e69-147">shortday</span></span>  <br/> |<span data-ttu-id="86e69-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="86e69-148">xs:string</span></span>  <br/> |<span data-ttu-id="86e69-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="86e69-149">required</span></span>  <br/> |<span data-ttu-id="86e69-150">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="86e69-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="86e69-151">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="86e69-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="86e69-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="86e69-152">skycodeday</span></span>  <br/> |<span data-ttu-id="86e69-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="86e69-153">xs:integer</span></span>  <br/> |<span data-ttu-id="86e69-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="86e69-154">required</span></span>  <br/> |<span data-ttu-id="86e69-155">Gibt einen Code für die geplanten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="86e69-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="86e69-156">Der Wert der Type-xs</span><span class="sxs-lookup"><span data-stu-id="86e69-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="86e69-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="86e69-157">skytextday</span></span>  <br/> |<span data-ttu-id="86e69-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="86e69-158">xs:string</span></span>  <br/> |<span data-ttu-id="86e69-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="86e69-159">required</span></span>  <br/> |<span data-ttu-id="86e69-160">Gibt ein bis zwei Wörter, die die geplanten Bedingungen zu beschreiben.</span><span class="sxs-lookup"><span data-stu-id="86e69-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="86e69-161">Ein Wert, der den Typ xs:</span><span class="sxs-lookup"><span data-stu-id="86e69-161">A value of the type xs:string</span></span>  <br/> |
   

