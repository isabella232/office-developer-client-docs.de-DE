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
# <a name="nurbs-function"></a><span data-ttu-id="a7c5d-104">NURBS-Funktion</span><span class="sxs-lookup"><span data-stu-id="a7c5d-104">NURBS Function</span></span>

<span data-ttu-id="a7c5d-105">Gibt ein nonuniform rationales B-Spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="a7c5d-105">Returns a nonuniform rational B-spline (NURBS).</span></span> <span data-ttu-id="a7c5d-106">Diese Funktion wird in der Zelle E NURBS verwendet.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-106">This function is used in the E cell in the NURBSTo geometry rows.</span></span>
  
## <a name="syntax"></a><span data-ttu-id="a7c5d-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="a7c5d-107">Syntax</span></span>

<span data-ttu-id="a7c5d-108">NURBS (** *KnotZuletst* **, ** *Grad* **, ** *xTyp gleich* **, ** *gleich* **, ** *X1* **, ** *y1* **, ** *knot1* **, ** *Gewicht1* **,...)</span><span class="sxs-lookup"><span data-stu-id="a7c5d-108">NURBS(** *knotLast* **, ** *degree* **, ** *xType* **, ** *yType* **, ** *x1* **, ** *y1* **, ** *knot1* **, ** *weight1* **, ...)</span></span> 
  
### <a name="parameters"></a><span data-ttu-id="a7c5d-109">Parameter</span><span class="sxs-lookup"><span data-stu-id="a7c5d-109">Parameters</span></span>

|<span data-ttu-id="a7c5d-110">**Name**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-110">**Name**</span></span>|<span data-ttu-id="a7c5d-111">**Erforderlich/Optional**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-111">**Required/Optional**</span></span>|<span data-ttu-id="a7c5d-112">**Datentyp**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-112">**Data Type**</span></span>|<span data-ttu-id="a7c5d-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-113">**Description**</span></span>|
|:-----|:-----|:-----|:-----|
| <span data-ttu-id="a7c5d-114">_KnotZuletst_</span><span class="sxs-lookup"><span data-stu-id="a7c5d-114">_knotLast_</span></span> <br/> |<span data-ttu-id="a7c5d-115">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a7c5d-115">Required</span></span>  <br/> |<span data-ttu-id="a7c5d-116">**string**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-116">**string**</span></span> <br/> | <span data-ttu-id="a7c5d-117">Der letzte Knoten.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-117">The last knot.</span></span>  <br/> |
| <span data-ttu-id="a7c5d-118">_Grad_</span><span class="sxs-lookup"><span data-stu-id="a7c5d-118">_degree_</span></span> <br/> |<span data-ttu-id="a7c5d-119">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a7c5d-119">Required</span></span>  <br/> |<span data-ttu-id="a7c5d-120">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-120">**Numeric**</span></span> <br/> |<span data-ttu-id="a7c5d-121">Der Gradwert des Splines.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-121">The spline's degree.</span></span>  <br/> |
| <span data-ttu-id="a7c5d-122">_xTyp gleich_</span><span class="sxs-lookup"><span data-stu-id="a7c5d-122">_xType_</span></span> <br/> |<span data-ttu-id="a7c5d-123">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a7c5d-123">Required</span></span>  <br/> |<span data-ttu-id="a7c5d-124">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-124">**Numeric**</span></span> <br/> |<span data-ttu-id="a7c5d-125">Gibt an, wie die _X_ -Eingabedaten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-125">Specifies how to interpret the  _x_ input data.</span></span> <span data-ttu-id="a7c5d-126">Wenn _xTyp gleich_ 0 ist, werden alle _x_ eingegebenen Daten als Prozentsatz der Breite interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-126">If  _xType_ is 0, all  _x_ input data is interpreted as a percentage of Width.</span></span> <span data-ttu-id="a7c5d-127">Wenn _xTyp gleich_ 1 ist, werden alle _X_ Eingabedaten als lokale Koordinaten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-127">If  _xType_ is 1, all  _x_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="a7c5d-128">_Gleich_</span><span class="sxs-lookup"><span data-stu-id="a7c5d-128">_yType_</span></span> <br/> |<span data-ttu-id="a7c5d-129">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a7c5d-129">Required</span></span>  <br/> |<span data-ttu-id="a7c5d-130">**Numerische**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-130">**Numeric**</span></span> <br/> |<span data-ttu-id="a7c5d-131">Gibt an, wie die _y_ -Eingabedaten interpretiert werden.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-131">Specifies how to interpret the  _y_ input data.</span></span> <span data-ttu-id="a7c5d-132">Wenn _gleich_ 0 ist, werden alle eingegebenen _y_ -Daten als Prozentsatz der Höhe interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-132">If  _yType_ is 0, all  _y_ input data is interpreted as a percentage of Height.</span></span> <span data-ttu-id="a7c5d-133">Wenn _gleich_ 1 ist, werden alle _y_ eingegebenen Daten als lokale Koordinaten interpretiert.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-133">If  _yType_ is 1, all  _y_ input data is interpreted as local coordinates.</span></span>  <br/> |
| <span data-ttu-id="a7c5d-134">_x1_</span><span class="sxs-lookup"><span data-stu-id="a7c5d-134">_x1_</span></span> <br/> |<span data-ttu-id="a7c5d-135">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a7c5d-135">Required</span></span>  <br/> |<span data-ttu-id="a7c5d-136">**String**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-136">**String**</span></span> <br/> |<span data-ttu-id="a7c5d-137">Eine x-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-137">An x-coordinate.</span></span>  <br/> |
| <span data-ttu-id="a7c5d-138">_Y1_</span><span class="sxs-lookup"><span data-stu-id="a7c5d-138">_y1_</span></span> <br/> |<span data-ttu-id="a7c5d-139">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a7c5d-139">Required</span></span>  <br/> |<span data-ttu-id="a7c5d-140">**String**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-140">**String**</span></span> <br/> |<span data-ttu-id="a7c5d-141">Eine y-Koordinate.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-141">A y-coordinate.</span></span>  <br/> |
| <span data-ttu-id="a7c5d-142">_Knot1_</span><span class="sxs-lookup"><span data-stu-id="a7c5d-142">_knot1_</span></span> <br/> |<span data-ttu-id="a7c5d-143">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a7c5d-143">Required</span></span>  <br/> |<span data-ttu-id="a7c5d-144">**String**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-144">**String**</span></span> <br/> |<span data-ttu-id="a7c5d-145">Ein Knoten auf dem B-Spline.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-145">A knot on the B-spline.</span></span>  <br/> |
| <span data-ttu-id="a7c5d-146">_Gewicht1_</span><span class="sxs-lookup"><span data-stu-id="a7c5d-146">_weight1_</span></span> <br/> |<span data-ttu-id="a7c5d-147">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="a7c5d-147">Required</span></span>  <br/> |<span data-ttu-id="a7c5d-148">**String**</span><span class="sxs-lookup"><span data-stu-id="a7c5d-148">**String**</span></span> <br/> |<span data-ttu-id="a7c5d-149">Eine Breite für das B-Spline.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-149">A weight on the B-spline.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a7c5d-150">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a7c5d-150">Remarks</span></span>

<span data-ttu-id="a7c5d-151">Für jedes *X* -Argument muss ein *y* -Argument; Andernfalls wird ein Fehler zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-151">For every  *x*  argument, there must be a  *y*  argument; otherwise, an error is returned.</span></span> 
  
<span data-ttu-id="a7c5d-152">Sie müssen mindestens eine *X*, *y*, *Knoten* und *Weight* -Argument angeben. andernfalls, gibt Visio einen Fehler zurück.</span><span class="sxs-lookup"><span data-stu-id="a7c5d-152">You must specify at least one  *x*, *y*, *knot*  , and  *weight*  argument; otherwise, Visio returns an error.</span></span> 
  

