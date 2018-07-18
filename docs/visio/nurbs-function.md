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
description: Gibt ein nonuniform rationales B-Spline (NURBS). Diese Funktion wird in der Zelle E NURBS verwendet.
ms.openlocfilehash: 005a66b9da2425beaf416ec2273c10446c183add
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19797588"
---
# <a name="nurbs-function"></a><span data-ttu-id="629cf-104">NURBS Function</span><span class="sxs-lookup"><span data-stu-id="629cf-104">NURBS Function</span></span>

<span data-ttu-id="629cf-105">Gibt ein nonuniform rationales B-Spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="629cf-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="629cf-106">Diese Funktion wird in der Zelle E NURBS verwendet.</span><span class="sxs-lookup"><span data-stu-id="629cf-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="629cf-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="629cf-107">Syntax</span></span>

<span data-ttu-id="629cf-108">NURBS (** *KnotZuletst* **, ** *Grad* **, ** *xTyp gleich* **, ** *gleich* **, ** *X1* **, ** *y1* **, ** *knot1* **, ** *Gewicht1* **,...)</span><span class="sxs-lookup"><span data-stu-id="629cf-108">NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="629cf-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="629cf-109">Parameters</span></span>

|<span data-ttu-id="629cf-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="629cf-110">**Name**</span></span>|<span data-ttu-id="629cf-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="629cf-111">**Required/Optional**</span></span>|<span data-ttu-id="629cf-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="629cf-112">**Data Type**</span></span>|<span data-ttu-id="629cf-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="629cf-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="629cf-114">_KnotZuletst_</span><span class="sxs-lookup"><span data-stu-id="629cf-114">_knotLast_</span></span> <br/> |<span data-ttu-id="629cf-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="629cf-115">Required</span></span>  <br/> |<span data-ttu-id="629cf-116">**string**</span><span class="sxs-lookup"><span data-stu-id="629cf-116">**string**</span></span> <br/> | <span data-ttu-id="629cf-117">Der letzte Knoten.</span><span class="sxs-lookup"><span data-stu-id="629cf-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="629cf-118">_Grad_</span><span class="sxs-lookup"><span data-stu-id="629cf-118">_degree_</span></span> <br/> |<span data-ttu-id="629cf-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="629cf-119">Required</span></span>  <br/> |<span data-ttu-id="629cf-120">**Numeric**</span><span class="sxs-lookup"><span data-stu-id="629cf-120">**Numeric**</span></span> <br/> |<span data-ttu-id="629cf-121">Der Gradwert des Splines.</span><span class="sxs-lookup"><span data-stu-id="629cf-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="629cf-122">_xTyp gleich_</span><span class="sxs-lookup"><span data-stu-id="629cf-122">_xType_</span></span> <br/> |<span data-ttu-id="629cf-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="629cf-123">Required</span></span>  <br/> |<span data-ttu-id="629cf-124">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="629cf-124">**Numeric**</span></span> <br/> |<span data-ttu-id="629cf-125">Gibt an, wie die _X_ -Eingabedaten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="629cf-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="629cf-126">Wenn _xTyp gleich_ 0 ist, werden alle _x_ eingegebenen Daten als Prozentsatz der Breite interpretiert.</span><span class="sxs-lookup"><span data-stu-id="629cf-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="629cf-127">Wenn _xTyp gleich_ 1 ist, werden alle _X_ Eingabedaten als lokale Koordinaten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="629cf-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="629cf-128">_Gleich_</span><span class="sxs-lookup"><span data-stu-id="629cf-128">_yType_</span></span> <br/> |<span data-ttu-id="629cf-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="629cf-129">Required</span></span>  <br/> |<span data-ttu-id="629cf-130">**Numerisch**</span><span class="sxs-lookup"><span data-stu-id="629cf-130">**Numeric**</span></span> <br/> |<span data-ttu-id="629cf-131">Gibt an, wie die _y_ -Eingabedaten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="629cf-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="629cf-132">Wenn _gleich_ 0 ist, werden alle eingegebenen _y_ -Daten als Prozentsatz der Höhe interpretiert.</span><span class="sxs-lookup"><span data-stu-id="629cf-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="629cf-133">Wenn _gleich_ 1 ist, werden alle _y_ eingegebenen Daten als lokale Koordinaten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="629cf-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="629cf-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="629cf-134">_x1_</span></span> <br/> |<span data-ttu-id="629cf-135">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="629cf-135">Required</span></span>  <br/> |<span data-ttu-id="629cf-136">**String**</span><span class="sxs-lookup"><span data-stu-id="629cf-136">**String**</span></span> <br/> |<span data-ttu-id="629cf-137">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="629cf-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="629cf-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="629cf-138">_y1_</span></span> <br/> |<span data-ttu-id="629cf-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="629cf-139">Required</span></span>  <br/> |<span data-ttu-id="629cf-140">**String**</span><span class="sxs-lookup"><span data-stu-id="629cf-140">**String**</span></span> <br/> |<span data-ttu-id="629cf-141">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="629cf-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="629cf-142">_Knot1_</span><span class="sxs-lookup"><span data-stu-id="629cf-142">_knot1_</span></span> <br/> |<span data-ttu-id="629cf-143">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="629cf-143">Required</span></span>  <br/> |<span data-ttu-id="629cf-144">**String**</span><span class="sxs-lookup"><span data-stu-id="629cf-144">**String**</span></span> <br/> |<span data-ttu-id="629cf-145">Ein Knoten auf dem B-Spline.</span><span class="sxs-lookup"><span data-stu-id="629cf-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="629cf-146">_Gewicht1_</span><span class="sxs-lookup"><span data-stu-id="629cf-146">_weight1_</span></span> <br/> |<span data-ttu-id="629cf-147">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="629cf-147">Required</span></span>  <br/> |<span data-ttu-id="629cf-148">**String**</span><span class="sxs-lookup"><span data-stu-id="629cf-148">**String**</span></span> <br/> |<span data-ttu-id="629cf-149">Eine Breite für das B-Spline.</span><span class="sxs-lookup"><span data-stu-id="629cf-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="629cf-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="629cf-150">Remarks</span></span>

<span data-ttu-id="629cf-151">Für jedes *X* -Argument muss ein *y* -Argument; Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="629cf-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="629cf-152">Sie müssen mindestens eine *X*, *y*, *Knoten* und *Weight* -Argument angeben. andernfalls, gibt Visio einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="629cf-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

