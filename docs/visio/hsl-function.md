---
title: HSL-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251438
localization_priority: Normal
ms.assetid: c9314c39-1d2e-a18f-c01b-8817286099dc
description: Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt. Sie gibt eine Farbe anhand ihrer Farbton-, Sättigungs-und Helligkeits Komponenten an.
ms.openlocfilehash: 55703239395c54beedf4b7383435253f9c37006f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329925"
---
# <a name="hsl-function"></a><span data-ttu-id="41590-104">HSL-Funktion</span><span class="sxs-lookup"><span data-stu-id="41590-104">HSL Function</span></span>

<span data-ttu-id="41590-105">Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="41590-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="41590-106">Sie gibt eine Farbe anhand ihrer Farbton-, Sättigungs-und Helligkeits Komponenten an.</span><span class="sxs-lookup"><span data-stu-id="41590-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="41590-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="41590-107">Syntax</span></span>

<span data-ttu-id="41590-108">GSL (\* \* *Hue* \* \*, \* \* *Sättigung* \* \*, \* \* *Helligkeit* \* \*)</span><span class="sxs-lookup"><span data-stu-id="41590-108">HSL(\*\* *hue* \*\*, \*\* *saturation* \*\*, \*\* *luminosity* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="41590-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="41590-109">Parameters</span></span>

|<span data-ttu-id="41590-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="41590-110">**Name**</span></span>|<span data-ttu-id="41590-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="41590-111">**Required/Optional**</span></span>|<span data-ttu-id="41590-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="41590-112">**Data Type**</span></span>|<span data-ttu-id="41590-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41590-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="41590-114">_Farbton_</span><span class="sxs-lookup"><span data-stu-id="41590-114">_hue_</span></span> <br/> |<span data-ttu-id="41590-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="41590-115">Required</span></span>  <br/> |<span data-ttu-id="41590-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="41590-116">**Number**</span></span> <br/> |<span data-ttu-id="41590-117">Der Farbton einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 239 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="41590-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="41590-118">_Sättigung_</span><span class="sxs-lookup"><span data-stu-id="41590-118">_saturation_</span></span> <br/> |<span data-ttu-id="41590-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="41590-119">Required</span></span>  <br/> |<span data-ttu-id="41590-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="41590-120">**Number**</span></span> <br/> |<span data-ttu-id="41590-121">Die Sättigung einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 240 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="41590-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="41590-122">_Helligkeit_</span><span class="sxs-lookup"><span data-stu-id="41590-122">_luminosity_</span></span> <br/> |<span data-ttu-id="41590-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="41590-123">Required</span></span>  <br/> |<span data-ttu-id="41590-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="41590-124">**Number**</span></span> <br/> | <span data-ttu-id="41590-125">Die Helligkeit einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 240 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="41590-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="41590-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="41590-126">Return value</span></span>

<span data-ttu-id="41590-127">Zahl</span><span class="sxs-lookup"><span data-stu-id="41590-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="41590-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="41590-128">Remarks</span></span>

<span data-ttu-id="41590-129">Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie der Liste der verfügbaren Farben im Dokument hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="41590-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="41590-130">In der folgenden Tabelle sind einige Standardfarben mit ihren Farbton-, Sättigungs- und Helligkeitswerten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="41590-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="41590-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="41590-131">**Color**</span></span>|<span data-ttu-id="41590-132">**Farbton**</span><span class="sxs-lookup"><span data-stu-id="41590-132">**Hue value**</span></span>|<span data-ttu-id="41590-133">**Sättigung**</span><span class="sxs-lookup"><span data-stu-id="41590-133">**Saturation value**</span></span>|<span data-ttu-id="41590-134">**Helligkeitswert**</span><span class="sxs-lookup"><span data-stu-id="41590-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="41590-135">Schwarz</span><span class="sxs-lookup"><span data-stu-id="41590-135">Black</span></span>  <br/> |<span data-ttu-id="41590-136">0</span><span class="sxs-lookup"><span data-stu-id="41590-136">0</span></span>  <br/> |<span data-ttu-id="41590-137">0</span><span class="sxs-lookup"><span data-stu-id="41590-137">0</span></span>  <br/> |<span data-ttu-id="41590-138">24</span><span class="sxs-lookup"><span data-stu-id="41590-138">24</span></span>  <br/> |
|<span data-ttu-id="41590-139">Blau</span><span class="sxs-lookup"><span data-stu-id="41590-139">Blue</span></span>  <br/> |<span data-ttu-id="41590-140">160</span><span class="sxs-lookup"><span data-stu-id="41590-140">160</span></span>  <br/> |<span data-ttu-id="41590-141">240</span><span class="sxs-lookup"><span data-stu-id="41590-141">240</span></span>  <br/> |<span data-ttu-id="41590-142">120</span><span class="sxs-lookup"><span data-stu-id="41590-142">120</span></span>  <br/> |
|<span data-ttu-id="41590-143">Grün</span><span class="sxs-lookup"><span data-stu-id="41590-143">Green</span></span>  <br/> |<span data-ttu-id="41590-144">80</span><span class="sxs-lookup"><span data-stu-id="41590-144">80</span></span>  <br/> |<span data-ttu-id="41590-145">240</span><span class="sxs-lookup"><span data-stu-id="41590-145">240</span></span>  <br/> |<span data-ttu-id="41590-146">120</span><span class="sxs-lookup"><span data-stu-id="41590-146">120</span></span>  <br/> |
|<span data-ttu-id="41590-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="41590-147">Cyan</span></span>  <br/> |<span data-ttu-id="41590-148">120</span><span class="sxs-lookup"><span data-stu-id="41590-148">120</span></span>  <br/> |<span data-ttu-id="41590-149">240</span><span class="sxs-lookup"><span data-stu-id="41590-149">240</span></span>  <br/> |<span data-ttu-id="41590-150">120</span><span class="sxs-lookup"><span data-stu-id="41590-150">120</span></span>  <br/> |
|<span data-ttu-id="41590-151">Rot</span><span class="sxs-lookup"><span data-stu-id="41590-151">Red</span></span>  <br/> |<span data-ttu-id="41590-152">0</span><span class="sxs-lookup"><span data-stu-id="41590-152">0</span></span>  <br/> |<span data-ttu-id="41590-153">240</span><span class="sxs-lookup"><span data-stu-id="41590-153">240</span></span>  <br/> |<span data-ttu-id="41590-154">120</span><span class="sxs-lookup"><span data-stu-id="41590-154">120</span></span>  <br/> |
|<span data-ttu-id="41590-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="41590-155">Magenta</span></span>  <br/> |<span data-ttu-id="41590-156">200</span><span class="sxs-lookup"><span data-stu-id="41590-156">200</span></span>  <br/> |<span data-ttu-id="41590-157">240</span><span class="sxs-lookup"><span data-stu-id="41590-157">240</span></span>  <br/> |<span data-ttu-id="41590-158">120</span><span class="sxs-lookup"><span data-stu-id="41590-158">120</span></span>  <br/> |
|<span data-ttu-id="41590-159">Gelb</span><span class="sxs-lookup"><span data-stu-id="41590-159">Yellow</span></span>  <br/> |<span data-ttu-id="41590-160">40</span><span class="sxs-lookup"><span data-stu-id="41590-160">40</span></span>  <br/> |<span data-ttu-id="41590-161">240</span><span class="sxs-lookup"><span data-stu-id="41590-161">240</span></span>  <br/> |<span data-ttu-id="41590-162">120</span><span class="sxs-lookup"><span data-stu-id="41590-162">120</span></span>  <br/> |
|<span data-ttu-id="41590-163">Weiß</span><span class="sxs-lookup"><span data-stu-id="41590-163">White</span></span>  <br/> |<span data-ttu-id="41590-164">0</span><span class="sxs-lookup"><span data-stu-id="41590-164">0</span></span>  <br/> |<span data-ttu-id="41590-165">0</span><span class="sxs-lookup"><span data-stu-id="41590-165">0</span></span>  <br/> |<span data-ttu-id="41590-166">240</span><span class="sxs-lookup"><span data-stu-id="41590-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="41590-167">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="41590-167">Example 1</span></span>

<span data-ttu-id="41590-168">GSL (160240120)</span><span class="sxs-lookup"><span data-stu-id="41590-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="41590-169">Gibt den Index für die Farbe Blau zurück.</span><span class="sxs-lookup"><span data-stu-id="41590-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="41590-170">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="41590-170">Example 2</span></span>

<span data-ttu-id="41590-171">GSL (HUE (Zelle FillForegnd), SAT (Zelle FillForegnd), MIN (LUM (Zelle FillForegnd) + 100240))</span><span class="sxs-lookup"><span data-stu-id="41590-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="41590-172">Gibt den Index für eine Farbe zurück, der die Vordergrundfüllfarbe mit erhöhter Helligkeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="41590-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

