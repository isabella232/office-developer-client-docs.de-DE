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
description: Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt. Sie gibt eine Farbe anhand ihrer rot-, grün-und Blau-Komponenten an, wobei jedes eine Zahl im Bereich von 0 bis 255, einschließlich oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird.
ms.openlocfilehash: 34f9c2f2043afe6144feba561e545dc7be35a5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426303"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="00f06-104">RGB-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="00f06-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="00f06-105">Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="00f06-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="00f06-106">Sie gibt eine Farbe anhand ihrer rot-, grün-und Blau-Komponenten an, wobei jedes eine Zahl im Bereich von 0 bis 255, einschließlich oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="00f06-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="00f06-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="00f06-107">Syntax</span></span>

<span data-ttu-id="00f06-108">RGB (\* \* *rot* \* \*, \* \* *grün* \* \*, \* \* *blau* \* \*)</span><span class="sxs-lookup"><span data-stu-id="00f06-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="00f06-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="00f06-109">Parameters</span></span>

|<span data-ttu-id="00f06-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="00f06-110">**Name**</span></span>|<span data-ttu-id="00f06-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="00f06-111">**Required/Optional**</span></span>|<span data-ttu-id="00f06-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="00f06-112">**Data Type**</span></span>|<span data-ttu-id="00f06-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00f06-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="00f06-114">_rot_</span><span class="sxs-lookup"><span data-stu-id="00f06-114">_red_</span></span> <br/> |<span data-ttu-id="00f06-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="00f06-115">Required</span></span>  <br/> |<span data-ttu-id="00f06-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="00f06-116">**Number**</span></span> <br/> |<span data-ttu-id="00f06-117">Die Rotkomponente.</span><span class="sxs-lookup"><span data-stu-id="00f06-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="00f06-118">_grün_</span><span class="sxs-lookup"><span data-stu-id="00f06-118">_green_</span></span> <br/> |<span data-ttu-id="00f06-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="00f06-119">Required</span></span>  <br/> |<span data-ttu-id="00f06-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="00f06-120">**Number**</span></span> <br/> |<span data-ttu-id="00f06-121">Die Grünkomponente.</span><span class="sxs-lookup"><span data-stu-id="00f06-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="00f06-122">_blau_</span><span class="sxs-lookup"><span data-stu-id="00f06-122">_blue_</span></span> <br/> |<span data-ttu-id="00f06-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="00f06-123">Required</span></span>  <br/> |<span data-ttu-id="00f06-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="00f06-124">**Nmber**</span></span> <br/> |<span data-ttu-id="00f06-125">Die Blaukomponente.</span><span class="sxs-lookup"><span data-stu-id="00f06-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="00f06-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="00f06-126">Return value</span></span>

<span data-ttu-id="00f06-127">Zahl</span><span class="sxs-lookup"><span data-stu-id="00f06-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00f06-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="00f06-128">Remarks</span></span>

<span data-ttu-id="00f06-129">Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie in diese eingefügt.</span><span class="sxs-lookup"><span data-stu-id="00f06-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="00f06-130">Die folgende Tabelle listet einige Standardfarben mit ihren Rot-, Grün- und Blauwerten auf.</span><span class="sxs-lookup"><span data-stu-id="00f06-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="00f06-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="00f06-131">**Color**</span></span>|<span data-ttu-id="00f06-132">**Rotwert**</span><span class="sxs-lookup"><span data-stu-id="00f06-132">**Red value**</span></span>|<span data-ttu-id="00f06-133">**Grünwert**</span><span class="sxs-lookup"><span data-stu-id="00f06-133">**Green value**</span></span>|<span data-ttu-id="00f06-134">**Blauwert**</span><span class="sxs-lookup"><span data-stu-id="00f06-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="00f06-135">Schwarz</span><span class="sxs-lookup"><span data-stu-id="00f06-135">Black</span></span>  <br/> |<span data-ttu-id="00f06-136">0</span><span class="sxs-lookup"><span data-stu-id="00f06-136">0</span></span>  <br/> |<span data-ttu-id="00f06-137">0</span><span class="sxs-lookup"><span data-stu-id="00f06-137">0</span></span>  <br/> |<span data-ttu-id="00f06-138">0</span><span class="sxs-lookup"><span data-stu-id="00f06-138">0</span></span>  <br/> |
|<span data-ttu-id="00f06-139">Blau</span><span class="sxs-lookup"><span data-stu-id="00f06-139">Blue</span></span>  <br/> |<span data-ttu-id="00f06-140">0</span><span class="sxs-lookup"><span data-stu-id="00f06-140">0</span></span>  <br/> |<span data-ttu-id="00f06-141">0</span><span class="sxs-lookup"><span data-stu-id="00f06-141">0</span></span>  <br/> |<span data-ttu-id="00f06-142">255</span><span class="sxs-lookup"><span data-stu-id="00f06-142">255</span></span>  <br/> |
|<span data-ttu-id="00f06-143">Grün</span><span class="sxs-lookup"><span data-stu-id="00f06-143">Green</span></span>  <br/> |<span data-ttu-id="00f06-144">0</span><span class="sxs-lookup"><span data-stu-id="00f06-144">0</span></span>  <br/> |<span data-ttu-id="00f06-145">255</span><span class="sxs-lookup"><span data-stu-id="00f06-145">255</span></span>  <br/> |<span data-ttu-id="00f06-146">0</span><span class="sxs-lookup"><span data-stu-id="00f06-146">0</span></span>  <br/> |
|<span data-ttu-id="00f06-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="00f06-147">Cyan</span></span>  <br/> |<span data-ttu-id="00f06-148">0</span><span class="sxs-lookup"><span data-stu-id="00f06-148">0</span></span>  <br/> |<span data-ttu-id="00f06-149">255</span><span class="sxs-lookup"><span data-stu-id="00f06-149">255</span></span>  <br/> |<span data-ttu-id="00f06-150">255</span><span class="sxs-lookup"><span data-stu-id="00f06-150">255</span></span>  <br/> |
|<span data-ttu-id="00f06-151">Rot</span><span class="sxs-lookup"><span data-stu-id="00f06-151">Red</span></span>  <br/> |<span data-ttu-id="00f06-152">255</span><span class="sxs-lookup"><span data-stu-id="00f06-152">255</span></span>  <br/> |<span data-ttu-id="00f06-153">0</span><span class="sxs-lookup"><span data-stu-id="00f06-153">0</span></span>  <br/> |<span data-ttu-id="00f06-154">0</span><span class="sxs-lookup"><span data-stu-id="00f06-154">0</span></span>  <br/> |
|<span data-ttu-id="00f06-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="00f06-155">Magenta</span></span>  <br/> |<span data-ttu-id="00f06-156">255</span><span class="sxs-lookup"><span data-stu-id="00f06-156">255</span></span>  <br/> |<span data-ttu-id="00f06-157">0</span><span class="sxs-lookup"><span data-stu-id="00f06-157">0</span></span>  <br/> |<span data-ttu-id="00f06-158">255</span><span class="sxs-lookup"><span data-stu-id="00f06-158">255</span></span>  <br/> |
|<span data-ttu-id="00f06-159">Gelb</span><span class="sxs-lookup"><span data-stu-id="00f06-159">Yellow</span></span>  <br/> |<span data-ttu-id="00f06-160">255</span><span class="sxs-lookup"><span data-stu-id="00f06-160">255</span></span>  <br/> |<span data-ttu-id="00f06-161">255</span><span class="sxs-lookup"><span data-stu-id="00f06-161">255</span></span>  <br/> |<span data-ttu-id="00f06-162">0</span><span class="sxs-lookup"><span data-stu-id="00f06-162">0</span></span>  <br/> |
|<span data-ttu-id="00f06-163">Weiß</span><span class="sxs-lookup"><span data-stu-id="00f06-163">White</span></span>  <br/> |<span data-ttu-id="00f06-164">255</span><span class="sxs-lookup"><span data-stu-id="00f06-164">255</span></span>  <br/> |<span data-ttu-id="00f06-165">255</span><span class="sxs-lookup"><span data-stu-id="00f06-165">255</span></span>  <br/> |<span data-ttu-id="00f06-166">255</span><span class="sxs-lookup"><span data-stu-id="00f06-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="00f06-167">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="00f06-167">Example 1</span></span>

<span data-ttu-id="00f06-168">RGB (0, 0255)</span><span class="sxs-lookup"><span data-stu-id="00f06-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="00f06-169">Gibt den Index für die Farbe Blau zurück.</span><span class="sxs-lookup"><span data-stu-id="00f06-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="00f06-170">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="00f06-170">Example 2</span></span>

<span data-ttu-id="00f06-171">RGB (rot (Blatt. 1! Zelle FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="00f06-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="00f06-172">Gibt den Index für eine Farbe zurück, deren Rotkomponente der Vordergrundfüllfarbe von Sheet.1 entspricht.</span><span class="sxs-lookup"><span data-stu-id="00f06-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

