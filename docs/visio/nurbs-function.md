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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32340124"
---
# <a name="nurbs-function"></a><span data-ttu-id="2fe2e-104">NURBS Function</span><span class="sxs-lookup"><span data-stu-id="2fe2e-104">NURBS Function</span></span>

<span data-ttu-id="2fe2e-105">Gibt einen nicht einheitlichen rationalen B-Spline (NURBS) zurück.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="2fe2e-106">Diese Funktion wird in der Zelle "E" in den NURBSTo-Geometrie Zeilen verwendet.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="2fe2e-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="2fe2e-107">Syntax</span></span>

<span data-ttu-id="2fe2e-108">NURBS (\* \* *knotLast* \* \*, \* \* *Grad* \* \*, \* \* *xType* \* \*, \* \* *yType* \* \*, \* \* *x1* \* \*, \* \* *Y1* \* \*, \* \* *Knot1* \* \*, \* \* *Gewicht1* \* \*,...)</span><span class="sxs-lookup"><span data-stu-id="2fe2e-108">NURBS(\*\* *knotLast* \*\*, \*\* *degree* \*\*, \*\* *xType* \*\*, \*\* *yType* \*\*, \*\* *x1* \*\*, \*\* *y1* \*\*, \*\* *knot1* \*\*, \*\* *weight1* \*\*, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="2fe2e-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="2fe2e-109">Parameters</span></span>

|<span data-ttu-id="2fe2e-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-110">**Name**</span></span>|<span data-ttu-id="2fe2e-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-111">**Required/Optional**</span></span>|<span data-ttu-id="2fe2e-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-112">**Data Type**</span></span>|<span data-ttu-id="2fe2e-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="2fe2e-114">_knotLast_</span><span class="sxs-lookup"><span data-stu-id="2fe2e-114">_knotLast_</span></span> <br/> |<span data-ttu-id="2fe2e-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2fe2e-115">Required</span></span>  <br/> |<span data-ttu-id="2fe2e-116">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-116">**string**</span></span> <br/> | <span data-ttu-id="2fe2e-117">Der letzte Knoten.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="2fe2e-118">_Grad_</span><span class="sxs-lookup"><span data-stu-id="2fe2e-118">_degree_</span></span> <br/> |<span data-ttu-id="2fe2e-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2fe2e-119">Required</span></span>  <br/> |<span data-ttu-id="2fe2e-120">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-120">**Numeric**</span></span> <br/> |<span data-ttu-id="2fe2e-121">Der Gradwert des Splines.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="2fe2e-122">_xType_</span><span class="sxs-lookup"><span data-stu-id="2fe2e-122">_xType_</span></span> <br/> |<span data-ttu-id="2fe2e-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2fe2e-123">Required</span></span>  <br/> |<span data-ttu-id="2fe2e-124">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-124">**Numeric**</span></span> <br/> |<span data-ttu-id="2fe2e-125">Gibt an, wie die _x_ -Eingabedaten interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="2fe2e-126">Wenn _xType_ 0 ist, werden alle _x_ -Eingabedaten als Prozentsatz der Breite interpretiert.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="2fe2e-127">Wenn _xType_ ist, werden alle _x_ -Eingabedaten als lokale Koordinaten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="2fe2e-128">_yType_</span><span class="sxs-lookup"><span data-stu-id="2fe2e-128">_yType_</span></span> <br/> |<span data-ttu-id="2fe2e-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2fe2e-129">Required</span></span>  <br/> |<span data-ttu-id="2fe2e-130">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-130">**Numeric**</span></span> <br/> |<span data-ttu-id="2fe2e-131">Gibt an, wie die _y_ -Eingabedaten interpretiert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="2fe2e-132">Wenn _yType_ 0 ist, werden alle _y_ -Eingabedaten als Prozentsatz der Höhe interpretiert.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="2fe2e-133">Wenn _yType_ ist, werden alle _y_ -Eingabedaten als lokale Koordinaten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="2fe2e-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="2fe2e-134">_x1_</span></span> <br/> |<span data-ttu-id="2fe2e-135">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2fe2e-135">Required</span></span>  <br/> |<span data-ttu-id="2fe2e-136">**String**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-136">**String**</span></span> <br/> |<span data-ttu-id="2fe2e-137">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="2fe2e-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="2fe2e-138">_y1_</span></span> <br/> |<span data-ttu-id="2fe2e-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2fe2e-139">Required</span></span>  <br/> |<span data-ttu-id="2fe2e-140">**String**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-140">**String**</span></span> <br/> |<span data-ttu-id="2fe2e-141">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="2fe2e-142">_Knot1_</span><span class="sxs-lookup"><span data-stu-id="2fe2e-142">_knot1_</span></span> <br/> |<span data-ttu-id="2fe2e-143">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2fe2e-143">Required</span></span>  <br/> |<span data-ttu-id="2fe2e-144">**String**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-144">**String**</span></span> <br/> |<span data-ttu-id="2fe2e-145">Ein Knoten auf dem B-Spline.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="2fe2e-146">_Gewicht1_</span><span class="sxs-lookup"><span data-stu-id="2fe2e-146">_weight1_</span></span> <br/> |<span data-ttu-id="2fe2e-147">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="2fe2e-147">Required</span></span>  <br/> |<span data-ttu-id="2fe2e-148">**String**</span><span class="sxs-lookup"><span data-stu-id="2fe2e-148">**String**</span></span> <br/> |<span data-ttu-id="2fe2e-149">Eine Breite für das B-Spline.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2fe2e-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2fe2e-150">Remarks</span></span>

<span data-ttu-id="2fe2e-151">Für jedes *x* -Argument muss ein *y* -Argument angegeben werden; Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="2fe2e-152">Sie müssen mindestens ein Argument für *x*, *y*, *Knot* und *Weight* angeben; Andernfalls gibt Visio einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="2fe2e-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

