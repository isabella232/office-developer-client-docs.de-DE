---
title: forecastType complexType (Outlook Wetterinformationsschema)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6301d6b6-34fa-af8d-e682-605d35cfdf47
description: Definiert die Parameter zu den Wettervorhersagebedingungen eines Standorts.
ms.openlocfilehash: e799ebbea72daa1788aedbdcadbc523b5e4dff0d
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540952"
---
# <a name="forecasttype-complextype-outlook-weather-information-schema"></a><span data-ttu-id="6f0c4-103">forecastType complexType (Outlook Wetterinformationsschema)</span><span class="sxs-lookup"><span data-stu-id="6f0c4-103">forecastType complexType (Outlook Weather Information Schema)</span></span>

<span data-ttu-id="6f0c4-104">Definiert die Parameter zu den Wettervorhersagebedingungen eines Standorts.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-104">Defines the parameters about the forecast weather conditions of a location.</span></span>
  
## <a name="type-information"></a><span data-ttu-id="6f0c4-105">Informationen zum Typ</span><span class="sxs-lookup"><span data-stu-id="6f0c4-105">Type information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="6f0c4-106">**Namespace**</span><span class="sxs-lookup"><span data-stu-id="6f0c4-106">**Namespace**</span></span> <br/> |http://schemas.microsoft.com/office/outlook/15/getweatherinfo.xsd  <br/> |
|<span data-ttu-id="6f0c4-107">**Schemadatei**</span><span class="sxs-lookup"><span data-stu-id="6f0c4-107">**Schema file**</span></span> <br/> |<span data-ttu-id="6f0c4-108">getweatherinfo.xsd</span><span class="sxs-lookup"><span data-stu-id="6f0c4-108">getweatherinfo.xsd</span></span>  <br/> |
|<span data-ttu-id="6f0c4-109">**Erweiterungsbasis**</span><span class="sxs-lookup"><span data-stu-id="6f0c4-109">**Extension base**</span></span> <br/> |<span data-ttu-id="6f0c4-110">Keine</span><span class="sxs-lookup"><span data-stu-id="6f0c4-110">None</span></span>  <br/> |
   
## <a name="definition"></a><span data-ttu-id="6f0c4-111">Definition</span><span class="sxs-lookup"><span data-stu-id="6f0c4-111">Definition</span></span>

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

## <a name="elements-and-attributes"></a><span data-ttu-id="6f0c4-112">Elemente und Attribute</span><span class="sxs-lookup"><span data-stu-id="6f0c4-112">Elements and attributes</span></span>

<span data-ttu-id="6f0c4-113">Wenn das Schema bestimmte Anforderungen definiert, z. B. **Sequenz**, **minOccurs,** **maxOccurs** und **Auswahl,** finden Sie im Abschnitt Definition.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-113">If the schema defines specific requirements, such as **sequence**, **minOccurs**, **maxOccurs**, and **choice**, see the definition section.</span></span> 
  
### <a name="child-elements"></a><span data-ttu-id="6f0c4-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="6f0c4-114">Child elements</span></span>

<span data-ttu-id="6f0c4-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-115">None.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="6f0c4-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="6f0c4-116">Attributes</span></span>

|<span data-ttu-id="6f0c4-117">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="6f0c4-117">**Attribute**</span></span>|<span data-ttu-id="6f0c4-118">**Typ**</span><span class="sxs-lookup"><span data-stu-id="6f0c4-118">**Type**</span></span>|<span data-ttu-id="6f0c4-119">**Erforderlich**</span><span class="sxs-lookup"><span data-stu-id="6f0c4-119">**Required**</span></span>|<span data-ttu-id="6f0c4-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f0c4-120">**Description**</span></span>|<span data-ttu-id="6f0c4-121">**Mögliche Werte**</span><span class="sxs-lookup"><span data-stu-id="6f0c4-121">**Possible values**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="6f0c4-122">date</span><span class="sxs-lookup"><span data-stu-id="6f0c4-122">date</span></span>  <br/> |<span data-ttu-id="6f0c4-123">xs:date</span><span class="sxs-lookup"><span data-stu-id="6f0c4-123">xs:date</span></span>  <br/> |<span data-ttu-id="6f0c4-124">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f0c4-124">required</span></span>  <br/> |<span data-ttu-id="6f0c4-125">Gibt das Datum für die Planung an.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-125">Specifies the date for the forecast.</span></span>  <br/> |<span data-ttu-id="6f0c4-126">Ein Wert vom Typ xs:date</span><span class="sxs-lookup"><span data-stu-id="6f0c4-126">A value of the type xs:date</span></span>  <br/> |
|<span data-ttu-id="6f0c4-127">day</span><span class="sxs-lookup"><span data-stu-id="6f0c4-127">day</span></span>  <br/> |<span data-ttu-id="6f0c4-128">xs:string</span><span class="sxs-lookup"><span data-stu-id="6f0c4-128">xs:string</span></span>  <br/> |<span data-ttu-id="6f0c4-129">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f0c4-129">required</span></span>  <br/> |<span data-ttu-id="6f0c4-130">Gibt einen Tag für die Prognose an.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-130">Specifies a day for the forecast.</span></span>  <br/> |<span data-ttu-id="6f0c4-131">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="6f0c4-131">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6f0c4-132">high</span><span class="sxs-lookup"><span data-stu-id="6f0c4-132">high</span></span>  <br/> |<span data-ttu-id="6f0c4-133">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6f0c4-133">xs:integer</span></span>  <br/> |<span data-ttu-id="6f0c4-134">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f0c4-134">required</span></span>  <br/> |<span data-ttu-id="6f0c4-135">Gibt die vorhergesagte höchste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-135">Specifies the forecasted highest temperature.</span></span>  <br/> |<span data-ttu-id="6f0c4-136">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="6f0c4-136">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="6f0c4-137">low</span><span class="sxs-lookup"><span data-stu-id="6f0c4-137">low</span></span>  <br/> |<span data-ttu-id="6f0c4-138">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6f0c4-138">xs:integer</span></span>  <br/> |<span data-ttu-id="6f0c4-139">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f0c4-139">required</span></span>  <br/> |<span data-ttu-id="6f0c4-140">Gibt die vorhergesagte niedrigste Temperatur an.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-140">Specifies the forecasted lowest temperature.</span></span>  <br/> |<span data-ttu-id="6f0c4-141">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="6f0c4-141">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="6f0c4-142">precip</span><span class="sxs-lookup"><span data-stu-id="6f0c4-142">precip</span></span>  <br/> |<span data-ttu-id="6f0c4-143">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6f0c4-143">xs:integer</span></span>  <br/> |<span data-ttu-id="6f0c4-144">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f0c4-144">required</span></span>  <br/> |<span data-ttu-id="6f0c4-145">Gibt die prozentuale Wahrscheinlichkeit der Verfällung an.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-145">Specifies the percentage possibility of precipitation.</span></span>  <br/> |<span data-ttu-id="6f0c4-146">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="6f0c4-146">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="6f0c4-147">shortday</span><span class="sxs-lookup"><span data-stu-id="6f0c4-147">shortday</span></span>  <br/> |<span data-ttu-id="6f0c4-148">xs:string</span><span class="sxs-lookup"><span data-stu-id="6f0c4-148">xs:string</span></span>  <br/> |<span data-ttu-id="6f0c4-149">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f0c4-149">required</span></span>  <br/> |<span data-ttu-id="6f0c4-150">Gibt einen Tag in abgekürzter Form an.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-150">Specifies a day in abbreviated form.</span></span>  <br/> |<span data-ttu-id="6f0c4-151">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="6f0c4-151">A value of the type xs:string</span></span>  <br/> |
|<span data-ttu-id="6f0c4-152">skycodeday</span><span class="sxs-lookup"><span data-stu-id="6f0c4-152">skycodeday</span></span>  <br/> |<span data-ttu-id="6f0c4-153">xs:integer</span><span class="sxs-lookup"><span data-stu-id="6f0c4-153">xs:integer</span></span>  <br/> |<span data-ttu-id="6f0c4-154">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f0c4-154">required</span></span>  <br/> |<span data-ttu-id="6f0c4-155">Gibt einen Code für die vorhergesagten Bedingungen an.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-155">Specifies a code for the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="6f0c4-156">Ein Wert vom Typ xs:integer</span><span class="sxs-lookup"><span data-stu-id="6f0c4-156">A value of the type xs:integer</span></span>  <br/> |
|<span data-ttu-id="6f0c4-157">skytextday</span><span class="sxs-lookup"><span data-stu-id="6f0c4-157">skytextday</span></span>  <br/> |<span data-ttu-id="6f0c4-158">xs:string</span><span class="sxs-lookup"><span data-stu-id="6f0c4-158">xs:string</span></span>  <br/> |<span data-ttu-id="6f0c4-159">erforderlich</span><span class="sxs-lookup"><span data-stu-id="6f0c4-159">required</span></span>  <br/> |<span data-ttu-id="6f0c4-160">Gibt ein bis zwei Wörter an, die die prognostizierten Bedingungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="6f0c4-160">Specifies one to two words that describe the forecasted conditions.</span></span>  <br/> |<span data-ttu-id="6f0c4-161">Ein Wert vom Typ xs:string</span><span class="sxs-lookup"><span data-stu-id="6f0c4-161">A value of the type xs:string</span></span>  <br/> |
   

