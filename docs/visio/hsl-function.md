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
description: Gibt einen Wert, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe durch seine Farbton, Sättigung und Helligkeit Komponenten.
ms.openlocfilehash: 50f343d990157d831ac4ac43057d0a2b7fca63f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797166"
---
# <a name="hsl-function"></a><span data-ttu-id="d051b-104">HSL-Funktion</span><span class="sxs-lookup"><span data-stu-id="d051b-104">HSL Function</span></span>

<span data-ttu-id="d051b-105">Gibt einen Wert, der einen Index in der Farbpalette des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="d051b-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="d051b-106">Es gibt eine Farbe durch seine Farbton, Sättigung und Helligkeit Komponenten.</span><span class="sxs-lookup"><span data-stu-id="d051b-106">It specifies a color by its hue, saturation, and luminosity components.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="d051b-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="d051b-107">Syntax</span></span>

<span data-ttu-id="d051b-108">HSL (** *Farbton* **, ** *Sättigung* **, ** *Helligkeit* **)</span><span class="sxs-lookup"><span data-stu-id="d051b-108">HSL(** *hue* **, ** *saturation* **, ** *luminosity* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="d051b-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="d051b-109">Parameters</span></span>

|<span data-ttu-id="d051b-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="d051b-110">**Name**</span></span>|<span data-ttu-id="d051b-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="d051b-111">**Required/Optional**</span></span>|<span data-ttu-id="d051b-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="d051b-112">**Data Type**</span></span>|<span data-ttu-id="d051b-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d051b-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="d051b-114">_Farbton_</span><span class="sxs-lookup"><span data-stu-id="d051b-114">_hue_</span></span> <br/> |<span data-ttu-id="d051b-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d051b-115">Required</span></span>  <br/> |<span data-ttu-id="d051b-116">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="d051b-116">**Number**</span></span> <br/> |<span data-ttu-id="d051b-117">Der Farbton einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 239 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d051b-117">The color's hue, expressed as a number in the range 0 to 239, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="d051b-118">_Sättigung_</span><span class="sxs-lookup"><span data-stu-id="d051b-118">_saturation_</span></span> <br/> |<span data-ttu-id="d051b-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d051b-119">Required</span></span>  <br/> |<span data-ttu-id="d051b-120">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="d051b-120">**Number**</span></span> <br/> |<span data-ttu-id="d051b-121">Die Sättigung einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 240 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d051b-121">The color's saturation, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
| <span data-ttu-id="d051b-122">_Helligkeit_</span><span class="sxs-lookup"><span data-stu-id="d051b-122">_luminosity_</span></span> <br/> |<span data-ttu-id="d051b-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="d051b-123">Required</span></span>  <br/> |<span data-ttu-id="d051b-124">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="d051b-124">**Number**</span></span> <br/> | <span data-ttu-id="d051b-125">Die Helligkeit einer Farbe wird als Zahl im Bereich von 0 bis einschließlich 240 ausgedrückt oder als Ausdruck, der als eine derartige Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="d051b-125">The color's luminosity, expressed as a number in the range 0 to 240, inclusive, or an expression that evaluates to such a number.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="d051b-126">R�ckgabewert</span><span class="sxs-lookup"><span data-stu-id="d051b-126">Return value</span></span>

<span data-ttu-id="d051b-127">Zahl</span><span class="sxs-lookup"><span data-stu-id="d051b-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d051b-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d051b-128">Remarks</span></span>

<span data-ttu-id="d051b-129">Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie der Liste der verfügbaren Farben im Dokument hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d051b-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the document's list of available colors.</span></span> 
  
<span data-ttu-id="d051b-130">In der folgenden Tabelle sind einige Standardfarben mit ihren Farbton-, Sättigungs- und Helligkeitswerten aufgelistet.</span><span class="sxs-lookup"><span data-stu-id="d051b-130">The following table lists some standard colors and their hue, saturation, and luminosity values.</span></span> 
  
|<span data-ttu-id="d051b-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="d051b-131">**Color**</span></span>|<span data-ttu-id="d051b-132">**Farbton**</span><span class="sxs-lookup"><span data-stu-id="d051b-132">**Hue value**</span></span>|<span data-ttu-id="d051b-133">**Sättigung**</span><span class="sxs-lookup"><span data-stu-id="d051b-133">**Saturation value**</span></span>|<span data-ttu-id="d051b-134">**Helligkeitswert**</span><span class="sxs-lookup"><span data-stu-id="d051b-134">**Luminosity value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="d051b-135">Schwarz</span><span class="sxs-lookup"><span data-stu-id="d051b-135">Black</span></span>  <br/> |<span data-ttu-id="d051b-136">0</span><span class="sxs-lookup"><span data-stu-id="d051b-136">0</span></span>  <br/> |<span data-ttu-id="d051b-137">0</span><span class="sxs-lookup"><span data-stu-id="d051b-137">0</span></span>  <br/> |<span data-ttu-id="d051b-138">24</span><span class="sxs-lookup"><span data-stu-id="d051b-138">24</span></span>  <br/> |
|<span data-ttu-id="d051b-139">Blau</span><span class="sxs-lookup"><span data-stu-id="d051b-139">Blue</span></span>  <br/> |<span data-ttu-id="d051b-140">160</span><span class="sxs-lookup"><span data-stu-id="d051b-140">160</span></span>  <br/> |<span data-ttu-id="d051b-141">240</span><span class="sxs-lookup"><span data-stu-id="d051b-141">240</span></span>  <br/> |<span data-ttu-id="d051b-142">120</span><span class="sxs-lookup"><span data-stu-id="d051b-142">120</span></span>  <br/> |
|<span data-ttu-id="d051b-143">Grün</span><span class="sxs-lookup"><span data-stu-id="d051b-143">Green</span></span>  <br/> |<span data-ttu-id="d051b-144">80</span><span class="sxs-lookup"><span data-stu-id="d051b-144">80</span></span>  <br/> |<span data-ttu-id="d051b-145">240</span><span class="sxs-lookup"><span data-stu-id="d051b-145">240</span></span>  <br/> |<span data-ttu-id="d051b-146">120</span><span class="sxs-lookup"><span data-stu-id="d051b-146">120</span></span>  <br/> |
|<span data-ttu-id="d051b-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="d051b-147">Cyan</span></span>  <br/> |<span data-ttu-id="d051b-148">120</span><span class="sxs-lookup"><span data-stu-id="d051b-148">120</span></span>  <br/> |<span data-ttu-id="d051b-149">240</span><span class="sxs-lookup"><span data-stu-id="d051b-149">240</span></span>  <br/> |<span data-ttu-id="d051b-150">120</span><span class="sxs-lookup"><span data-stu-id="d051b-150">120</span></span>  <br/> |
|<span data-ttu-id="d051b-151">Rot</span><span class="sxs-lookup"><span data-stu-id="d051b-151">Red</span></span>  <br/> |<span data-ttu-id="d051b-152">0</span><span class="sxs-lookup"><span data-stu-id="d051b-152">0</span></span>  <br/> |<span data-ttu-id="d051b-153">240</span><span class="sxs-lookup"><span data-stu-id="d051b-153">240</span></span>  <br/> |<span data-ttu-id="d051b-154">120</span><span class="sxs-lookup"><span data-stu-id="d051b-154">120</span></span>  <br/> |
|<span data-ttu-id="d051b-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="d051b-155">Magenta</span></span>  <br/> |<span data-ttu-id="d051b-156">200</span><span class="sxs-lookup"><span data-stu-id="d051b-156">200</span></span>  <br/> |<span data-ttu-id="d051b-157">240</span><span class="sxs-lookup"><span data-stu-id="d051b-157">240</span></span>  <br/> |<span data-ttu-id="d051b-158">120</span><span class="sxs-lookup"><span data-stu-id="d051b-158">120</span></span>  <br/> |
|<span data-ttu-id="d051b-159">Gelb</span><span class="sxs-lookup"><span data-stu-id="d051b-159">Yellow</span></span>  <br/> |<span data-ttu-id="d051b-160">40</span><span class="sxs-lookup"><span data-stu-id="d051b-160">40</span></span>  <br/> |<span data-ttu-id="d051b-161">240</span><span class="sxs-lookup"><span data-stu-id="d051b-161">240</span></span>  <br/> |<span data-ttu-id="d051b-162">120</span><span class="sxs-lookup"><span data-stu-id="d051b-162">120</span></span>  <br/> |
|<span data-ttu-id="d051b-163">Weiß</span><span class="sxs-lookup"><span data-stu-id="d051b-163">White</span></span>  <br/> |<span data-ttu-id="d051b-164">0</span><span class="sxs-lookup"><span data-stu-id="d051b-164">0</span></span>  <br/> |<span data-ttu-id="d051b-165">0</span><span class="sxs-lookup"><span data-stu-id="d051b-165">0</span></span>  <br/> |<span data-ttu-id="d051b-166">240</span><span class="sxs-lookup"><span data-stu-id="d051b-166">240</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="d051b-167">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="d051b-167">Example 1</span></span>

<span data-ttu-id="d051b-168">HSL(160,240,120)</span><span class="sxs-lookup"><span data-stu-id="d051b-168">HSL(160,240,120)</span></span>
  
<span data-ttu-id="d051b-169">Gibt den Index für die Farbe Blau zurück.</span><span class="sxs-lookup"><span data-stu-id="d051b-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="d051b-170">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="d051b-170">Example 2</span></span>

<span data-ttu-id="d051b-171">HSL(Hue(FillForegnd),SAT(FillForegnd),Min(LUM(FillForegnd)+100,240))</span><span class="sxs-lookup"><span data-stu-id="d051b-171">HSL(HUE(FillForegnd),SAT(FillForegnd),MIN(LUM(FillForegnd)+100,240))</span></span>
  
<span data-ttu-id="d051b-172">Gibt den Index für eine Farbe zurück, der die Vordergrundfüllfarbe mit erhöhter Helligkeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="d051b-172">Returns the index for a color that mirrors the fill foreground color with increased luminosity.</span></span>
  

