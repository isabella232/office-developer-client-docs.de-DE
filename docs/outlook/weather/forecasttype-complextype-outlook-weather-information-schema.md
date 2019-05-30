---
title: forecasttype complexType (Outlook-Wetter Informations Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Definiert die Parameter zu den Wetterbedingungen eines Standorts.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540952"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="d499b-103">forecasttype complexType (Outlook-Wetter Informations Schema)</span><span class="sxs-lookup"><span data-stu-id="d499b-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="d499b-104">Definiert die Parameter zu den Wetterbedingungen eines Standorts.</span><span class="sxs-lookup"><span data-stu-id="d499b-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="d499b-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="d499b-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d499b-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="d499b-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="d499b-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="d499b-107">**Schema file**</span></span> <br/> |<span data-ttu-id="d499b-108">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="d499b-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="d499b-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="d499b-109">**Extension base**</span></span> <br/> |<span data-ttu-id="d499b-110">Keine</span><span class="sxs-lookup"><span data-stu-id="d499b-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="d499b-111">Definition</span><span class="sxs-lookup"><span data-stu-id="d499b-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="d499b-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="d499b-112">Elements and attributes</span></span>

<span data-ttu-id="d499b-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="d499b-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="d499b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d499b-114">Child elements</span></span>

<span data-ttu-id="d499b-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="d499b-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d499b-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="d499b-116">Attributes</span></span>

|<span data-ttu-id="d499b-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="d499b-117">**Attribute**</span></span>|<span data-ttu-id="d499b-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="d499b-118">**Type**</span></span>|<span data-ttu-id="d499b-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="d499b-119">**Required**</span></span>|<span data-ttu-id="d499b-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d499b-120">**Description**</span></span>|<span data-ttu-id="d499b-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="d499b-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d499b-122">date</span><span class="sxs-lookup"><span data-stu-id="d499b-122">date</span></span>  <br/> |<span data-ttu-id="d499b-123">xs: Datum</span><span class="sxs-lookup"><span data-stu-id="d499b-123">xs:date</span></span>  <br/> |<span data-ttu-id="d499b-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d499b-124">required</span></span>  <br/> |<span data-ttu-id="d499b-125">Gibt das Datum für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="d499b-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="d499b-126">Ein Wert vom Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="d499b-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="d499b-127">Tag</span><span class="sxs-lookup"><span data-stu-id="d499b-127">day</span></span>  <br/> |<span data-ttu-id="d499b-128">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d499b-128">xs:string</span></span>  <br/> |<span data-ttu-id="d499b-129">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d499b-129">required</span></span>  <br/> |<span data-ttu-id="d499b-130">Gibt einen Tag für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="d499b-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="d499b-131">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="d499b-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d499b-132">hohe</span><span class="sxs-lookup"><span data-stu-id="d499b-132">high</span></span>  <br/> |<span data-ttu-id="d499b-133">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="d499b-133">xs:integer</span></span>  <br/> |<span data-ttu-id="d499b-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d499b-134">required</span></span>  <br/> |<span data-ttu-id="d499b-135">Gibt die prognostizierte höchste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="d499b-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="d499b-136">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="d499b-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d499b-137">niedrigen</span><span class="sxs-lookup"><span data-stu-id="d499b-137">low</span></span>  <br/> |<span data-ttu-id="d499b-138">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="d499b-138">xs:integer</span></span>  <br/> |<span data-ttu-id="d499b-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d499b-139">required</span></span>  <br/> |<span data-ttu-id="d499b-140">Gibt die prognostizierte niedrigste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="d499b-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="d499b-141">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="d499b-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d499b-142">Precip</span><span class="sxs-lookup"><span data-stu-id="d499b-142">precip</span></span>  <br/> |<span data-ttu-id="d499b-143">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="d499b-143">xs:integer</span></span>  <br/> |<span data-ttu-id="d499b-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d499b-144">required</span></span>  <br/> |<span data-ttu-id="d499b-145">Gibt den Prozentsatz der Niederschlagswahrscheinlichkeit an.</span><span class="sxs-lookup"><span data-stu-id="d499b-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="d499b-146">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="d499b-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d499b-147">shortday</span><span class="sxs-lookup"><span data-stu-id="d499b-147">shortday</span></span>  <br/> |<span data-ttu-id="d499b-148">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d499b-148">xs:string</span></span>  <br/> |<span data-ttu-id="d499b-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d499b-149">required</span></span>  <br/> |<span data-ttu-id="d499b-150">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="d499b-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="d499b-151">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="d499b-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="d499b-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="d499b-152">skycodeday</span></span>  <br/> |<span data-ttu-id="d499b-153">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="d499b-153">xs:integer</span></span>  <br/> |<span data-ttu-id="d499b-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d499b-154">required</span></span>  <br/> |<span data-ttu-id="d499b-155">Gibt einen Code für die prognostizierten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="d499b-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="d499b-156">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="d499b-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="d499b-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="d499b-157">skytextday</span></span>  <br/> |<span data-ttu-id="d499b-158">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="d499b-158">xs:string</span></span>  <br/> |<span data-ttu-id="d499b-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="d499b-159">required</span></span>  <br/> |<span data-ttu-id="d499b-160">Gibt ein bis zwei Wörter an, die die prognostizierten Bedingungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="d499b-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="d499b-161">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="d499b-161">A value of the type xs:string</span></span>  <br/> |
   

