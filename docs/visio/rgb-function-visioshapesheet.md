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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326740"
---
# <a name="rgb-function-visioshapesheet"></a><span data-ttu-id="a9332-104">RGB-Funktion (VisioShapeSheet)</span><span class="sxs-lookup"><span data-stu-id="a9332-104">RGB Function (VisioShapeSheet)</span></span>

<span data-ttu-id="a9332-105">Gibt einen Wert zurück, der einen Index in der Farbpalette des Dokuments darstellt.</span><span class="sxs-lookup"><span data-stu-id="a9332-105">Returns a value representing an index in the document's color palette.</span></span> <span data-ttu-id="a9332-106">Sie gibt eine Farbe anhand ihrer rot-, grün-und Blau-Komponenten an, wobei jedes eine Zahl im Bereich von 0 bis 255, einschließlich oder ein Ausdruck ist, der zu einer solchen Zahl ausgewertet wird.</span><span class="sxs-lookup"><span data-stu-id="a9332-106">It specifies a color by its red, green, and blue components, where each is a number in the range 0 to 255, inclusive, or an expression that evaluates to such a number.</span></span> 
  
## <a name="syntax"></a><span data-ttu-id="a9332-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a9332-107">Syntax</span></span>

<span data-ttu-id="a9332-108">RGB (\* \* *rot* \* \*, \* \* *grün* \* \*, \* \* *blau* \* \*)</span><span class="sxs-lookup"><span data-stu-id="a9332-108">RGB(\*\* *red* \*\*, \*\* *green* \*\*, \*\* *blue* \*\* )</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a9332-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a9332-109">Parameters</span></span>

|<span data-ttu-id="a9332-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a9332-110">**Name**</span></span>|<span data-ttu-id="a9332-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a9332-111">**Required/Optional**</span></span>|<span data-ttu-id="a9332-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a9332-112">**Data Type**</span></span>|<span data-ttu-id="a9332-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9332-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a9332-114">_rot_</span><span class="sxs-lookup"><span data-stu-id="a9332-114">_red_</span></span> <br/> |<span data-ttu-id="a9332-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9332-115">Required</span></span>  <br/> |<span data-ttu-id="a9332-116">**Number**</span><span class="sxs-lookup"><span data-stu-id="a9332-116">**Number**</span></span> <br/> |<span data-ttu-id="a9332-117">Die Rotkomponente.</span><span class="sxs-lookup"><span data-stu-id="a9332-117">The red component.</span></span>  <br/> |
| <span data-ttu-id="a9332-118">_grün_</span><span class="sxs-lookup"><span data-stu-id="a9332-118">_green_</span></span> <br/> |<span data-ttu-id="a9332-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9332-119">Required</span></span>  <br/> |<span data-ttu-id="a9332-120">**Number**</span><span class="sxs-lookup"><span data-stu-id="a9332-120">**Number**</span></span> <br/> |<span data-ttu-id="a9332-121">Die Grünkomponente.</span><span class="sxs-lookup"><span data-stu-id="a9332-121">The green component.</span></span>  <br/> |
| <span data-ttu-id="a9332-122">_blau_</span><span class="sxs-lookup"><span data-stu-id="a9332-122">_blue_</span></span> <br/> |<span data-ttu-id="a9332-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a9332-123">Required</span></span>  <br/> |<span data-ttu-id="a9332-124">**Nmber**</span><span class="sxs-lookup"><span data-stu-id="a9332-124">**Nmber**</span></span> <br/> |<span data-ttu-id="a9332-125">Die Blaukomponente.</span><span class="sxs-lookup"><span data-stu-id="a9332-125">The blue component.</span></span>  <br/> |
   
### <a name="return-value"></a><span data-ttu-id="a9332-126">Rückgabewert</span><span class="sxs-lookup"><span data-stu-id="a9332-126">Return value</span></span>

<span data-ttu-id="a9332-127">Zahl</span><span class="sxs-lookup"><span data-stu-id="a9332-127">Number</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a9332-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a9332-128">Remarks</span></span>

<span data-ttu-id="a9332-129">Wenn die durch die Funktion zurückgegebene Farbe nicht bereits in der Farbpalette des aktuellen Dokuments vorhanden ist, wird sie in diese eingefügt.</span><span class="sxs-lookup"><span data-stu-id="a9332-129">If the color returned by the function does not already exist in the current document's color palette, it is added to the palette.</span></span>
  
<span data-ttu-id="a9332-130">Die folgende Tabelle listet einige Standardfarben mit ihren Rot-, Grün- und Blauwerten auf.</span><span class="sxs-lookup"><span data-stu-id="a9332-130">The following table lists some standard colors and their red, green, and blue values.</span></span>
  
|<span data-ttu-id="a9332-131">**Color**</span><span class="sxs-lookup"><span data-stu-id="a9332-131">**Color**</span></span>|<span data-ttu-id="a9332-132">**Rotwert**</span><span class="sxs-lookup"><span data-stu-id="a9332-132">**Red value**</span></span>|<span data-ttu-id="a9332-133">**Grünwert**</span><span class="sxs-lookup"><span data-stu-id="a9332-133">**Green value**</span></span>|<span data-ttu-id="a9332-134">**Blauwert**</span><span class="sxs-lookup"><span data-stu-id="a9332-134">**Blue value**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a9332-135">Schwarz</span><span class="sxs-lookup"><span data-stu-id="a9332-135">Black</span></span>  <br/> |<span data-ttu-id="a9332-136">0</span><span class="sxs-lookup"><span data-stu-id="a9332-136">0</span></span>  <br/> |<span data-ttu-id="a9332-137">0</span><span class="sxs-lookup"><span data-stu-id="a9332-137">0</span></span>  <br/> |<span data-ttu-id="a9332-138">0</span><span class="sxs-lookup"><span data-stu-id="a9332-138">0</span></span>  <br/> |
|<span data-ttu-id="a9332-139">Blau</span><span class="sxs-lookup"><span data-stu-id="a9332-139">Blue</span></span>  <br/> |<span data-ttu-id="a9332-140">0</span><span class="sxs-lookup"><span data-stu-id="a9332-140">0</span></span>  <br/> |<span data-ttu-id="a9332-141">0</span><span class="sxs-lookup"><span data-stu-id="a9332-141">0</span></span>  <br/> |<span data-ttu-id="a9332-142">255</span><span class="sxs-lookup"><span data-stu-id="a9332-142">255</span></span>  <br/> |
|<span data-ttu-id="a9332-143">Grün</span><span class="sxs-lookup"><span data-stu-id="a9332-143">Green</span></span>  <br/> |<span data-ttu-id="a9332-144">0</span><span class="sxs-lookup"><span data-stu-id="a9332-144">0</span></span>  <br/> |<span data-ttu-id="a9332-145">255</span><span class="sxs-lookup"><span data-stu-id="a9332-145">255</span></span>  <br/> |<span data-ttu-id="a9332-146">0</span><span class="sxs-lookup"><span data-stu-id="a9332-146">0</span></span>  <br/> |
|<span data-ttu-id="a9332-147">Cyan</span><span class="sxs-lookup"><span data-stu-id="a9332-147">Cyan</span></span>  <br/> |<span data-ttu-id="a9332-148">0</span><span class="sxs-lookup"><span data-stu-id="a9332-148">0</span></span>  <br/> |<span data-ttu-id="a9332-149">255</span><span class="sxs-lookup"><span data-stu-id="a9332-149">255</span></span>  <br/> |<span data-ttu-id="a9332-150">255</span><span class="sxs-lookup"><span data-stu-id="a9332-150">255</span></span>  <br/> |
|<span data-ttu-id="a9332-151">Rot</span><span class="sxs-lookup"><span data-stu-id="a9332-151">Red</span></span>  <br/> |<span data-ttu-id="a9332-152">255</span><span class="sxs-lookup"><span data-stu-id="a9332-152">255</span></span>  <br/> |<span data-ttu-id="a9332-153">0</span><span class="sxs-lookup"><span data-stu-id="a9332-153">0</span></span>  <br/> |<span data-ttu-id="a9332-154">0</span><span class="sxs-lookup"><span data-stu-id="a9332-154">0</span></span>  <br/> |
|<span data-ttu-id="a9332-155">Magenta</span><span class="sxs-lookup"><span data-stu-id="a9332-155">Magenta</span></span>  <br/> |<span data-ttu-id="a9332-156">255</span><span class="sxs-lookup"><span data-stu-id="a9332-156">255</span></span>  <br/> |<span data-ttu-id="a9332-157">0</span><span class="sxs-lookup"><span data-stu-id="a9332-157">0</span></span>  <br/> |<span data-ttu-id="a9332-158">255</span><span class="sxs-lookup"><span data-stu-id="a9332-158">255</span></span>  <br/> |
|<span data-ttu-id="a9332-159">Gelb</span><span class="sxs-lookup"><span data-stu-id="a9332-159">Yellow</span></span>  <br/> |<span data-ttu-id="a9332-160">255</span><span class="sxs-lookup"><span data-stu-id="a9332-160">255</span></span>  <br/> |<span data-ttu-id="a9332-161">255</span><span class="sxs-lookup"><span data-stu-id="a9332-161">255</span></span>  <br/> |<span data-ttu-id="a9332-162">0</span><span class="sxs-lookup"><span data-stu-id="a9332-162">0</span></span>  <br/> |
|<span data-ttu-id="a9332-163">Weiß</span><span class="sxs-lookup"><span data-stu-id="a9332-163">White</span></span>  <br/> |<span data-ttu-id="a9332-164">255</span><span class="sxs-lookup"><span data-stu-id="a9332-164">255</span></span>  <br/> |<span data-ttu-id="a9332-165">255</span><span class="sxs-lookup"><span data-stu-id="a9332-165">255</span></span>  <br/> |<span data-ttu-id="a9332-166">255</span><span class="sxs-lookup"><span data-stu-id="a9332-166">255</span></span>  <br/> |
   
## <a name="example-1"></a><span data-ttu-id="a9332-167">Beispiel 1</span><span class="sxs-lookup"><span data-stu-id="a9332-167">Example 1</span></span>

<span data-ttu-id="a9332-168">RGB (0, 0255)</span><span class="sxs-lookup"><span data-stu-id="a9332-168">RGB(0,0,255)</span></span>
  
<span data-ttu-id="a9332-169">Gibt den Index für die Farbe Blau zurück.</span><span class="sxs-lookup"><span data-stu-id="a9332-169">Returns the index for the color blue.</span></span>
  
## <a name="example-2"></a><span data-ttu-id="a9332-170">Beispiel 2</span><span class="sxs-lookup"><span data-stu-id="a9332-170">Example 2</span></span>

<span data-ttu-id="a9332-171">RGB (rot (Blatt. 1! Zelle FillForegnd), 120, 0)</span><span class="sxs-lookup"><span data-stu-id="a9332-171">RGB(RED(Sheet.1!FillForegnd),120,0)</span></span>
  
<span data-ttu-id="a9332-172">Gibt den Index für eine Farbe zurück, deren Rotkomponente der Vordergrundfüllfarbe von Sheet.1 entspricht.</span><span class="sxs-lookup"><span data-stu-id="a9332-172">Returns the index for a color whose red component mirrors Sheet.1's fill foreground.</span></span>
  

