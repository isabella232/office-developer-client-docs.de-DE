---
title: RGB Function (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Gibt einen Wert, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe nach seiner Rot-, Grün- und blauen-Komponenten, wobei es sich um eine Zahl im Bereich von 0 bis einschließlich 255 oder ein Ausdruck, der als eine derartige Zahl ausgewertet wird.
ms.openlocfilehash: 7fa129d3ed28441f619660ed0db035cde85979bf
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797856"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="828f0-104">RGB Function (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="828f0-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="828f0-105">Gibt einen Wert, der einen Index in der Farbpalette des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="828f0-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="828f0-106">Es gibt eine Farbe nach seiner Rot-, Grün- und blauen-Komponenten, wobei es sich um eine Zahl im Bereich von 0 bis einschließlich 255 oder ein Ausdruck, der als eine derartige Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="828f0-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="828f0-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="828f0-107">Syntax</span></span>

<span data-ttu-id="828f0-108">RGB (** *Rot* **, ** *grüne* **, ** *Blau* **)</span><span class="sxs-lookup"><span data-stu-id="828f0-108">RGB(** *red* **, ** *green* **, ** *blue* ** )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="828f0-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="828f0-109">Parameters</span></span>

|<span data-ttu-id="828f0-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="828f0-110">**Name**</span></span>|<span data-ttu-id="828f0-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="828f0-111">**Required/Optional**</span></span>|<span data-ttu-id="828f0-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="828f0-112">**Data Type**</span></span>|<span data-ttu-id="828f0-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="828f0-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="828f0-114">_Rot_</span><span class="sxs-lookup"><span data-stu-id="828f0-114">_red_</span></span> <br/> |<span data-ttu-id="828f0-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="828f0-115">Required</span></span>  <br/> |<span data-ttu-id="828f0-116">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="828f0-116">**Number**</span></span> <br/> |<span data-ttu-id="828f0-117">Die Rotkomponente.</span><span class="sxs-lookup"><span data-stu-id="828f0-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="828f0-118">_Grün_</span><span class="sxs-lookup"><span data-stu-id="828f0-118">_green_</span></span> <br/> |<span data-ttu-id="828f0-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="828f0-119">Required</span></span>  <br/> |<span data-ttu-id="828f0-120">**Nummer**</span><span class="sxs-lookup"><span data-stu-id="828f0-120">**Number**</span></span> <br/> |<span data-ttu-id="828f0-121">Die Grünkomponente.</span><span class="sxs-lookup"><span data-stu-id="828f0-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="828f0-122">_Blau_</span><span class="sxs-lookup"><span data-stu-id="828f0-122">_blue_</span></span> <br/> |<span data-ttu-id="828f0-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="828f0-123">Required</span></span>  <br/> |<span data-ttu-id="828f0-124">**Number**</span><span class="sxs-lookup"><span data-stu-id="828f0-124">**Nmber**</span></span> <br/> |<span data-ttu-id="828f0-125">Die Blaukomponente.</span><span class="sxs-lookup"><span data-stu-id="828f0-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="828f0-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="828f0-126">Return value</span></span>

<span data-ttu-id="828f0-127">Zahl</span><span class="sxs-lookup"><span data-stu-id="828f0-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="828f0-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="828f0-128">Remarks</span></span>

<span data-ttu-id="828f0-129">Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie in diese eingefügt.</span><span class="sxs-lookup"><span data-stu-id="828f0-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="828f0-130">Die folgende Tabelle listet einige Standardfarben mit ihren Rot-, Grün- und Blauwerten auf.</span><span class="sxs-lookup"><span data-stu-id="828f0-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="828f0-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="828f0-131">**Color**</span></span>|<span data-ttu-id="828f0-132">**Rotwert**</span><span class="sxs-lookup"><span data-stu-id="828f0-132">**Red value**</span></span>|<span data-ttu-id="828f0-133">**Grünwert**</span><span class="sxs-lookup"><span data-stu-id="828f0-133">**Green value**</span></span>|<span data-ttu-id="828f0-134">**Blauwert**</span><span class="sxs-lookup"><span data-stu-id="828f0-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="828f0-135">Schwarz</span><span class="sxs-lookup"><span data-stu-id="828f0-135">Black</span></span>  <br/> |<span data-ttu-id="828f0-136">0</span><span class="sxs-lookup"><span data-stu-id="828f0-136">0</span></span>  <br/> |<span data-ttu-id="828f0-137">0</span><span class="sxs-lookup"><span data-stu-id="828f0-137">0</span></span>  <br/> |<span data-ttu-id="828f0-138">0</span><span class="sxs-lookup"><span data-stu-id="828f0-138">0</span></span>  <br/> |
|<span data-ttu-id="828f0-139">Blau</span><span class="sxs-lookup"><span data-stu-id="828f0-139">Blue</span></span>  <br/> |<span data-ttu-id="828f0-140">0</span><span class="sxs-lookup"><span data-stu-id="828f0-140">0</span></span>  <br/> |<span data-ttu-id="828f0-141">0</span><span class="sxs-lookup"><span data-stu-id="828f0-141">0</span></span>  <br/> |<span data-ttu-id="828f0-142">255</span><span class="sxs-lookup"><span data-stu-id="828f0-142">255</span></span>  <br/> |
|<span data-ttu-id="828f0-143">Grün</span><span class="sxs-lookup"><span data-stu-id="828f0-143">Green</span></span>  <br/> |<span data-ttu-id="828f0-144">0</span><span class="sxs-lookup"><span data-stu-id="828f0-144">0</span></span>  <br/> |<span data-ttu-id="828f0-145">255</span><span class="sxs-lookup"><span data-stu-id="828f0-145">255</span></span>  <br/> |<span data-ttu-id="828f0-146">0</span><span class="sxs-lookup"><span data-stu-id="828f0-146">0</span></span>  <br/> |
|<span data-ttu-id="828f0-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="828f0-147">Cyan</span></span>  <br/> |<span data-ttu-id="828f0-148">0</span><span class="sxs-lookup"><span data-stu-id="828f0-148">0</span></span>  <br/> |<span data-ttu-id="828f0-149">255</span><span class="sxs-lookup"><span data-stu-id="828f0-149">255</span></span>  <br/> |<span data-ttu-id="828f0-150">255</span><span class="sxs-lookup"><span data-stu-id="828f0-150">255</span></span>  <br/> |
|<span data-ttu-id="828f0-151">Rot</span><span class="sxs-lookup"><span data-stu-id="828f0-151">Red</span></span>  <br/> |<span data-ttu-id="828f0-152">255</span><span class="sxs-lookup"><span data-stu-id="828f0-152">255</span></span>  <br/> |<span data-ttu-id="828f0-153">0</span><span class="sxs-lookup"><span data-stu-id="828f0-153">0</span></span>  <br/> |<span data-ttu-id="828f0-154">0</span><span class="sxs-lookup"><span data-stu-id="828f0-154">0</span></span>  <br/> |
|<span data-ttu-id="828f0-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="828f0-155">Magenta</span></span>  <br/> |<span data-ttu-id="828f0-156">255</span><span class="sxs-lookup"><span data-stu-id="828f0-156">255</span></span>  <br/> |<span data-ttu-id="828f0-157">0</span><span class="sxs-lookup"><span data-stu-id="828f0-157">0</span></span>  <br/> |<span data-ttu-id="828f0-158">255</span><span class="sxs-lookup"><span data-stu-id="828f0-158">255</span></span>  <br/> |
|<span data-ttu-id="828f0-159">Gelb</span><span class="sxs-lookup"><span data-stu-id="828f0-159">Yellow</span></span>  <br/> |<span data-ttu-id="828f0-160">255</span><span class="sxs-lookup"><span data-stu-id="828f0-160">255</span></span>  <br/> |<span data-ttu-id="828f0-161">255</span><span class="sxs-lookup"><span data-stu-id="828f0-161">255</span></span>  <br/> |<span data-ttu-id="828f0-162">0</span><span class="sxs-lookup"><span data-stu-id="828f0-162">0</span></span>  <br/> |
|<span data-ttu-id="828f0-163">Weiß</span><span class="sxs-lookup"><span data-stu-id="828f0-163">White</span></span>  <br/> |<span data-ttu-id="828f0-164">255</span><span class="sxs-lookup"><span data-stu-id="828f0-164">255</span></span>  <br/> |<span data-ttu-id="828f0-165">255</span><span class="sxs-lookup"><span data-stu-id="828f0-165">255</span></span>  <br/> |<span data-ttu-id="828f0-166">255</span><span class="sxs-lookup"><span data-stu-id="828f0-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="828f0-167">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="828f0-167">Example 1</span></span>

<span data-ttu-id="828f0-168">RGB(0,0,255)</span><span class="sxs-lookup"><span data-stu-id="828f0-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="828f0-169">Gibt den Index für die Farbe Blau zurück.</span><span class="sxs-lookup"><span data-stu-id="828f0-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="828f0-170">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="828f0-170">Example 2</span></span>

<span data-ttu-id="828f0-171">RGB (Rot (Sheet.1! FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="828f0-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="828f0-172">Gibt den Index für eine Farbe zurück, deren Rotkomponente der Vordergrundfüllfarbe von Sheet.1 entspricht.</span><span class="sxs-lookup"><span data-stu-id="828f0-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

