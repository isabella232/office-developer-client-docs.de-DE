---
title: NURBS-Funktion
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251579
localization_priority: Normal
ms.assetid: f34db20d-6501-2026-a5e8-29c4d4cb2405
description: Gibt einen nicht einheitlichen rationalen B-Spline (NURBS) zurück. Diese Funktion wird in der Zelle "E" in den NURBSTo-Geometrie Zeilen verwendet.
ms.openlocfilehash: af92374a829c0df8e71ac81e630abc4fa64988dc
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438456"
---
# <a name="nurbs-function"></a><span data-ttu-id="c6303-104">NURBS Function</span><span class="sxs-lookup"><span data-stu-id="c6303-104">NURBS Function</span></span>

<span data-ttu-id="c6303-105">Gibt einen nicht einheitlichen rationalen B-Spline (NURBS) zurück.</span><span class="sxs-lookup"><span data-stu-id="c6303-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="c6303-106">Diese Funktion wird in der Zelle "E" in den NURBSTo-Geometrie Zeilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="c6303-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="c6303-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="c6303-107">Syntax</span></span>

<span data-ttu-id="c6303-108">NURBS (\* \* *knotLast* \* \*, \* \* *Grad* \* \*, \* \* *xType* \* \*, \* \* *yType* \* \*, \* \* *x1* \* \*, \* \* *Y1* \* \*, \* \* *Knot1* \* \*, \* \* *Gewicht1* \* \*,...)</span><span class="sxs-lookup"><span data-stu-id="c6303-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="c6303-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="c6303-109">Parameters</span></span>

|<span data-ttu-id="c6303-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="c6303-110">**Name**</span></span>|<span data-ttu-id="c6303-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="c6303-111">**Required/Optional**</span></span>|<span data-ttu-id="c6303-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="c6303-112">**Data Type**</span></span>|<span data-ttu-id="c6303-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c6303-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="c6303-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="c6303-114">_knotLast_</span></span> <br/> |<span data-ttu-id="c6303-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6303-115">Required</span></span>  <br/> |<span data-ttu-id="c6303-116">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="c6303-116">**string**</span></span> <br/> | <span data-ttu-id="c6303-117">Der letzte Knoten.</span><span class="sxs-lookup"><span data-stu-id="c6303-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="c6303-118">_Grad_</span><span class="sxs-lookup"><span data-stu-id="c6303-118">_degree_</span></span> <br/> |<span data-ttu-id="c6303-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6303-119">Required</span></span>  <br/> |<span data-ttu-id="c6303-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="c6303-120">**Numeric**</span></span> <br/> |<span data-ttu-id="c6303-121">Der Gradwert des Splines.</span><span class="sxs-lookup"><span data-stu-id="c6303-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="c6303-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="c6303-122">_xType_</span></span> <br/> |<span data-ttu-id="c6303-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6303-123">Required</span></span>  <br/> |<span data-ttu-id="c6303-124">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="c6303-124">**Numeric**</span></span> <br/> |<span data-ttu-id="c6303-125">Gibt an, wie die _x_ -Eingabedaten interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6303-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="c6303-126">Wenn _xType_ 0 ist, werden alle _x_ -Eingabedaten als Prozentsatz der Breite interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c6303-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="c6303-127">Wenn _xType_ ist, werden alle _x_ -Eingabedaten als lokale Koordinaten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c6303-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="c6303-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="c6303-128">_yType_</span></span> <br/> |<span data-ttu-id="c6303-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6303-129">Required</span></span>  <br/> |<span data-ttu-id="c6303-130">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="c6303-130">**Numeric**</span></span> <br/> |<span data-ttu-id="c6303-131">Gibt an, wie die _y_ -Eingabedaten interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="c6303-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="c6303-132">Wenn _yType_ 0 ist, werden alle _y_ -Eingabedaten als Prozentsatz der Höhe interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c6303-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="c6303-133">Wenn _yType_ ist, werden alle _y_ -Eingabedaten als lokale Koordinaten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="c6303-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="c6303-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="c6303-134">_x1_</span></span> <br/> |<span data-ttu-id="c6303-135">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6303-135">Required</span></span>  <br/> |<span data-ttu-id="c6303-136">**String**</span><span class="sxs-lookup"><span data-stu-id="c6303-136">**String**</span></span> <br/> |<span data-ttu-id="c6303-137">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="c6303-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="c6303-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="c6303-138">_y1_</span></span> <br/> |<span data-ttu-id="c6303-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6303-139">Required</span></span>  <br/> |<span data-ttu-id="c6303-140">**String**</span><span class="sxs-lookup"><span data-stu-id="c6303-140">**String**</span></span> <br/> |<span data-ttu-id="c6303-141">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="c6303-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="c6303-142">_Knot1_</span><span class="sxs-lookup"><span data-stu-id="c6303-142">_knot1_</span></span> <br/> |<span data-ttu-id="c6303-143">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6303-143">Required</span></span>  <br/> |<span data-ttu-id="c6303-144">**String**</span><span class="sxs-lookup"><span data-stu-id="c6303-144">**String**</span></span> <br/> |<span data-ttu-id="c6303-145">Ein Knoten auf dem B-Spline.</span><span class="sxs-lookup"><span data-stu-id="c6303-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="c6303-146">_Gewicht1_</span><span class="sxs-lookup"><span data-stu-id="c6303-146">_weight1_</span></span> <br/> |<span data-ttu-id="c6303-147">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="c6303-147">Required</span></span>  <br/> |<span data-ttu-id="c6303-148">**String**</span><span class="sxs-lookup"><span data-stu-id="c6303-148">**String**</span></span> <br/> |<span data-ttu-id="c6303-149">Eine Breite für das B-Spline.</span><span class="sxs-lookup"><span data-stu-id="c6303-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c6303-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c6303-150">Remarks</span></span>

<span data-ttu-id="c6303-151">Für jedes *x* -Argument muss ein *y* -Argument angegeben werden; Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="c6303-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="c6303-152">Sie müssen mindestens ein Argument für *x*, *y*, *Knot* und *Weight* angeben; Andernfalls gibt Visio einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="c6303-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

