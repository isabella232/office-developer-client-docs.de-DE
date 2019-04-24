---
title: forecasttype complexType (Outlook Wetter Information-Schema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Definiert die Parameter für die Wettervorhersage für einen Standort.
ms.openlocfilehash: 75f20d7857fac85e1e95d23cf5ac826336648132
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361145"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="deac7-103">forecasttype complexType (Outlook Wetter Information-Schema)</span><span class="sxs-lookup"><span data-stu-id="deac7-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="deac7-104">Definiert die Parameter für die Wettervorhersage für einen Standort.</span><span class="sxs-lookup"><span data-stu-id="deac7-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="deac7-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="deac7-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="deac7-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="deac7-106">**Namespace**</span></span> <br/> |https://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="deac7-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="deac7-107">**Schema file**</span></span> <br/> |<span data-ttu-id="deac7-108">GetWeatherInfo. xsd</span><span class="sxs-lookup"><span data-stu-id="deac7-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="deac7-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="deac7-109">**Extension base**</span></span> <br/> |<span data-ttu-id="deac7-110">Keine</span><span class="sxs-lookup"><span data-stu-id="deac7-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="deac7-111">Definition</span><span class="sxs-lookup"><span data-stu-id="deac7-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="deac7-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="deac7-112">Elements and attributes</span></span>

<span data-ttu-id="deac7-113">Wenn das Schema bestimmte Anforderungen wie **Sequence**, **minOccurs**, **maxOccurs**und **Choice**definiert, lesen Sie den Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="deac7-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="deac7-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="deac7-114">Child elements</span></span>

<span data-ttu-id="deac7-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="deac7-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="deac7-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="deac7-116">Attributes</span></span>

|<span data-ttu-id="deac7-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="deac7-117">**Attribute**</span></span>|<span data-ttu-id="deac7-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="deac7-118">**Type**</span></span>|<span data-ttu-id="deac7-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="deac7-119">**Required**</span></span>|<span data-ttu-id="deac7-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="deac7-120">**Description**</span></span>|<span data-ttu-id="deac7-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="deac7-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="deac7-122">Datum</span><span class="sxs-lookup"><span data-stu-id="deac7-122">date</span></span>  <br/> |<span data-ttu-id="deac7-123">xs: Datum</span><span class="sxs-lookup"><span data-stu-id="deac7-123">xs:date</span></span>  <br/> |<span data-ttu-id="deac7-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="deac7-124">required</span></span>  <br/> |<span data-ttu-id="deac7-125">Gibt das Datum für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="deac7-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="deac7-126">Ein Wert vom Typ xs: Date</span><span class="sxs-lookup"><span data-stu-id="deac7-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="deac7-127">Tag</span><span class="sxs-lookup"><span data-stu-id="deac7-127">day</span></span>  <br/> |<span data-ttu-id="deac7-128">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="deac7-128">xs:string</span></span>  <br/> |<span data-ttu-id="deac7-129">erforderlich</span><span class="sxs-lookup"><span data-stu-id="deac7-129">required</span></span>  <br/> |<span data-ttu-id="deac7-130">Gibt einen Tag für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="deac7-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="deac7-131">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="deac7-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="deac7-132">hohe</span><span class="sxs-lookup"><span data-stu-id="deac7-132">high</span></span>  <br/> |<span data-ttu-id="deac7-133">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="deac7-133">xs:integer</span></span>  <br/> |<span data-ttu-id="deac7-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="deac7-134">required</span></span>  <br/> |<span data-ttu-id="deac7-135">Gibt die prognostizierte höchste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="deac7-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="deac7-136">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="deac7-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="deac7-137">mit niedriger</span><span class="sxs-lookup"><span data-stu-id="deac7-137">low</span></span>  <br/> |<span data-ttu-id="deac7-138">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="deac7-138">xs:integer</span></span>  <br/> |<span data-ttu-id="deac7-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="deac7-139">required</span></span>  <br/> |<span data-ttu-id="deac7-140">Gibt die prognostizierte niedrigste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="deac7-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="deac7-141">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="deac7-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="deac7-142">Precip</span><span class="sxs-lookup"><span data-stu-id="deac7-142">precip</span></span>  <br/> |<span data-ttu-id="deac7-143">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="deac7-143">xs:integer</span></span>  <br/> |<span data-ttu-id="deac7-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="deac7-144">required</span></span>  <br/> |<span data-ttu-id="deac7-145">Gibt die prozentuale Niederschlagswahrscheinlichkeit an.</span><span class="sxs-lookup"><span data-stu-id="deac7-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="deac7-146">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="deac7-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="deac7-147">shortday</span><span class="sxs-lookup"><span data-stu-id="deac7-147">shortday</span></span>  <br/> |<span data-ttu-id="deac7-148">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="deac7-148">xs:string</span></span>  <br/> |<span data-ttu-id="deac7-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="deac7-149">required</span></span>  <br/> |<span data-ttu-id="deac7-150">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="deac7-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="deac7-151">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="deac7-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="deac7-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="deac7-152">skycodeday</span></span>  <br/> |<span data-ttu-id="deac7-153">xs: Integer</span><span class="sxs-lookup"><span data-stu-id="deac7-153">xs:integer</span></span>  <br/> |<span data-ttu-id="deac7-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="deac7-154">required</span></span>  <br/> |<span data-ttu-id="deac7-155">Gibt einen Code für die prognostizierten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="deac7-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="deac7-156">Ein Wert vom Typ xs: Integer</span><span class="sxs-lookup"><span data-stu-id="deac7-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="deac7-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="deac7-157">skytextday</span></span>  <br/> |<span data-ttu-id="deac7-158">xs: Zeichenfolge</span><span class="sxs-lookup"><span data-stu-id="deac7-158">xs:string</span></span>  <br/> |<span data-ttu-id="deac7-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="deac7-159">required</span></span>  <br/> |<span data-ttu-id="deac7-160">Gibt ein bis zwei Wörter an, in denen die prognostizierten Bedingungen beschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="deac7-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="deac7-161">Ein Wert vom Typ xs: String</span><span class="sxs-lookup"><span data-stu-id="deac7-161">A value of the type xs:string</span></span>  <br/> |
   

