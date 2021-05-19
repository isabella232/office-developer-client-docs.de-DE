---
title: RGB-Funktion (VisioShapeSheet)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251489
localization_priority: Normal
ms.assetid: f6b9f65c-6752-16cb-7eb1-44e1ce56e80b
description: Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt. Es gibt eine Farbe durch seine roten, grünen und blauen Komponenten an, wobei jede eine Zahl im Bereich von 0 bis einschließlich 255 oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426303"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="128c8-104">RGB-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="128c8-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="128c8-105">Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="128c8-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="128c8-106">Es gibt eine Farbe durch seine roten, grünen und blauen Komponenten an, wobei jede eine Zahl im Bereich von 0 bis einschließlich 255 oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="128c8-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="128c8-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="128c8-107">Syntax</span></span>

<span data-ttu-id="128c8-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span><span class="sxs-lookup"><span data-stu-id="128c8-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="128c8-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="128c8-109">Parameters</span></span>

|<span data-ttu-id="128c8-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="128c8-110">**Name**</span></span>|<span data-ttu-id="128c8-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="128c8-111">**Required/Optional**</span></span>|<span data-ttu-id="128c8-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="128c8-112">**Data Type**</span></span>|<span data-ttu-id="128c8-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="128c8-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="128c8-114">_red_</span><span class="sxs-lookup"><span data-stu-id="128c8-114">_red_</span></span> <br/> |<span data-ttu-id="128c8-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="128c8-115">Required</span></span>  <br/> |<span data-ttu-id="128c8-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="128c8-116">**Number**</span></span> <br/> |<span data-ttu-id="128c8-117">Die Rotkomponente.</span><span class="sxs-lookup"><span data-stu-id="128c8-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="128c8-118">_grün_</span><span class="sxs-lookup"><span data-stu-id="128c8-118">_green_</span></span> <br/> |<span data-ttu-id="128c8-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="128c8-119">Required</span></span>  <br/> |<span data-ttu-id="128c8-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="128c8-120">**Number**</span></span> <br/> |<span data-ttu-id="128c8-121">Die Grünkomponente.</span><span class="sxs-lookup"><span data-stu-id="128c8-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="128c8-122">_blue_</span><span class="sxs-lookup"><span data-stu-id="128c8-122">_blue_</span></span> <br/> |<span data-ttu-id="128c8-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="128c8-123">Required</span></span>  <br/> |<span data-ttu-id="128c8-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="128c8-124">**Nmber**</span></span> <br/> |<span data-ttu-id="128c8-125">Die Blaukomponente.</span><span class="sxs-lookup"><span data-stu-id="128c8-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="128c8-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="128c8-126">Return value</span></span>

<span data-ttu-id="128c8-127">Nummer</span><span class="sxs-lookup"><span data-stu-id="128c8-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="128c8-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="128c8-128">Remarks</span></span>

<span data-ttu-id="128c8-129">Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie in diese eingefügt.</span><span class="sxs-lookup"><span data-stu-id="128c8-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="128c8-130">Die folgende Tabelle listet einige Standardfarben mit ihren Rot-, Grün- und Blauwerten auf.</span><span class="sxs-lookup"><span data-stu-id="128c8-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="128c8-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="128c8-131">**Color**</span></span>|<span data-ttu-id="128c8-132">**Rotwert**</span><span class="sxs-lookup"><span data-stu-id="128c8-132">**Red value**</span></span>|<span data-ttu-id="128c8-133">**Grünwert**</span><span class="sxs-lookup"><span data-stu-id="128c8-133">**Green value**</span></span>|<span data-ttu-id="128c8-134">**Blauwert**</span><span class="sxs-lookup"><span data-stu-id="128c8-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="128c8-135">Schwarz</span><span class="sxs-lookup"><span data-stu-id="128c8-135">Black</span></span>  <br/> |<span data-ttu-id="128c8-136">0</span><span class="sxs-lookup"><span data-stu-id="128c8-136">0</span></span>  <br/> |<span data-ttu-id="128c8-137">0</span><span class="sxs-lookup"><span data-stu-id="128c8-137">0</span></span>  <br/> |<span data-ttu-id="128c8-138">0</span><span class="sxs-lookup"><span data-stu-id="128c8-138">0</span></span>  <br/> |
|<span data-ttu-id="128c8-139">Blau</span><span class="sxs-lookup"><span data-stu-id="128c8-139">Blue</span></span>  <br/> |<span data-ttu-id="128c8-140">0</span><span class="sxs-lookup"><span data-stu-id="128c8-140">0</span></span>  <br/> |<span data-ttu-id="128c8-141">0</span><span class="sxs-lookup"><span data-stu-id="128c8-141">0</span></span>  <br/> |<span data-ttu-id="128c8-142">255</span><span class="sxs-lookup"><span data-stu-id="128c8-142">255</span></span>  <br/> |
|<span data-ttu-id="128c8-143">Grün</span><span class="sxs-lookup"><span data-stu-id="128c8-143">Green</span></span>  <br/> |<span data-ttu-id="128c8-144">0</span><span class="sxs-lookup"><span data-stu-id="128c8-144">0</span></span>  <br/> |<span data-ttu-id="128c8-145">255</span><span class="sxs-lookup"><span data-stu-id="128c8-145">255</span></span>  <br/> |<span data-ttu-id="128c8-146">0</span><span class="sxs-lookup"><span data-stu-id="128c8-146">0</span></span>  <br/> |
|<span data-ttu-id="128c8-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="128c8-147">Cyan</span></span>  <br/> |<span data-ttu-id="128c8-148">0</span><span class="sxs-lookup"><span data-stu-id="128c8-148">0</span></span>  <br/> |<span data-ttu-id="128c8-149">255</span><span class="sxs-lookup"><span data-stu-id="128c8-149">255</span></span>  <br/> |<span data-ttu-id="128c8-150">255</span><span class="sxs-lookup"><span data-stu-id="128c8-150">255</span></span>  <br/> |
|<span data-ttu-id="128c8-151">Rot</span><span class="sxs-lookup"><span data-stu-id="128c8-151">Red</span></span>  <br/> |<span data-ttu-id="128c8-152">255</span><span class="sxs-lookup"><span data-stu-id="128c8-152">255</span></span>  <br/> |<span data-ttu-id="128c8-153">0</span><span class="sxs-lookup"><span data-stu-id="128c8-153">0</span></span>  <br/> |<span data-ttu-id="128c8-154">0</span><span class="sxs-lookup"><span data-stu-id="128c8-154">0</span></span>  <br/> |
|<span data-ttu-id="128c8-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="128c8-155">Magenta</span></span>  <br/> |<span data-ttu-id="128c8-156">255</span><span class="sxs-lookup"><span data-stu-id="128c8-156">255</span></span>  <br/> |<span data-ttu-id="128c8-157">0</span><span class="sxs-lookup"><span data-stu-id="128c8-157">0</span></span>  <br/> |<span data-ttu-id="128c8-158">255</span><span class="sxs-lookup"><span data-stu-id="128c8-158">255</span></span>  <br/> |
|<span data-ttu-id="128c8-159">Gelb</span><span class="sxs-lookup"><span data-stu-id="128c8-159">Yellow</span></span>  <br/> |<span data-ttu-id="128c8-160">255</span><span class="sxs-lookup"><span data-stu-id="128c8-160">255</span></span>  <br/> |<span data-ttu-id="128c8-161">255</span><span class="sxs-lookup"><span data-stu-id="128c8-161">255</span></span>  <br/> |<span data-ttu-id="128c8-162">0</span><span class="sxs-lookup"><span data-stu-id="128c8-162">0</span></span>  <br/> |
|<span data-ttu-id="128c8-163">Weiß</span><span class="sxs-lookup"><span data-stu-id="128c8-163">White</span></span>  <br/> |<span data-ttu-id="128c8-164">255</span><span class="sxs-lookup"><span data-stu-id="128c8-164">255</span></span>  <br/> |<span data-ttu-id="128c8-165">255</span><span class="sxs-lookup"><span data-stu-id="128c8-165">255</span></span>  <br/> |<span data-ttu-id="128c8-166">255</span><span class="sxs-lookup"><span data-stu-id="128c8-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="128c8-167">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="128c8-167">Example 1</span></span>

<span data-ttu-id="128c8-168">RGB(0,0,255)</span><span class="sxs-lookup"><span data-stu-id="128c8-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="128c8-169">Gibt den Index für die Farbe Blau zurück.</span><span class="sxs-lookup"><span data-stu-id="128c8-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="128c8-170">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="128c8-170">Example 2</span></span>

<span data-ttu-id="128c8-171">RGB(RED(Sheet.1! FillForegnd),120,0)</span><span class="sxs-lookup"><span data-stu-id="128c8-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="128c8-172">Gibt den Index für eine Farbe zurück, deren Rotkomponente der Vordergrundfüllfarbe von Sheet.1 entspricht.</span><span class="sxs-lookup"><span data-stu-id="128c8-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

