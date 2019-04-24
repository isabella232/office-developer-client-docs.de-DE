---
title: Zelle "A" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm51215
localization_priority: Normal
ms.assetid: 6853df0f-d22e-89ca-7d34-342b9c0bea23
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: 42f346b06cad827cfe56fc113a8387d1a31a6867
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341587"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="0c028-104">Zelle "A" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="0c028-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="0c028-105">Stellt die Informationen in den verschiedenen Zeilen dar.</span><span class="sxs-lookup"><span data-stu-id="0c028-105">Represents different information in different rows.</span></span> <span data-ttu-id="0c028-106">In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="0c028-106">This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="0c028-107">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="0c028-107">**Row**</span></span>|<span data-ttu-id="0c028-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0c028-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0c028-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="0c028-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="0c028-110">Der Abstand vom Mittelpunkt des Bogens bis zum Mittelpunkt seiner Sehne.</span><span class="sxs-lookup"><span data-stu-id="0c028-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="0c028-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="0c028-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="0c028-112">Die *x* -Koordinate des Kontrollpunkts des Bogens, ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten in der Mitte zwischen dem Anfangs-und Endscheitel des Bogens. Andernfalls kann der Bogen zu einer extremen Größe anwachsen, um den Kontrollpunkt mit unvorhersehbaren Ergebnissen zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="0c028-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="0c028-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="0c028-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="0c028-114">Die Polylinienformel.</span><span class="sxs-lookup"><span data-stu-id="0c028-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="0c028-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="0c028-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="0c028-116">Der vorletzte Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="0c028-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="0c028-117">Zeile SplineStart</span><span class="sxs-lookup"><span data-stu-id="0c028-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="0c028-118">Der zweite Knoten des Splines.</span><span class="sxs-lookup"><span data-stu-id="0c028-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="0c028-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="0c028-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="0c028-120">Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).</span><span class="sxs-lookup"><span data-stu-id="0c028-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="0c028-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="0c028-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="0c028-122">Eine *x* -Koordinate eines Punkts auf der unendlichen Reihe; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="0c028-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="0c028-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="0c028-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="0c028-124">Eine *x* -Koordinate eines Punkts auf der Ellipse; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="0c028-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0c028-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="0c028-125">Remarks</span></span>

<span data-ttu-id="0c028-126">Wenn Sie einen Verweis auf die Zelle A aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0c028-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c028-127">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0c028-127">Cell name:</span></span>  <br/> | <span data-ttu-id="0c028-128">Geometrie *i* . A *j* wobei *i* und *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0c028-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="0c028-129">Geometrie *i* . A1 (Endpunkte und Ellipse) wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0c028-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0c028-130">Wenn Sie einen Verweis auf die Zelle A aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0c028-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0c028-131">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0c028-131">Section index:</span></span>  <br/> |<span data-ttu-id="0c028-132">**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0c028-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0c028-133">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0c028-133">Row index:</span></span>  <br/> |<span data-ttu-id="0c028-134">**visRowVertex** +  *j* = \*\* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0c028-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="0c028-135">**visRowVertex** (Zeilen für unendliche und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="0c028-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="0c028-136">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0c028-136">Cell index:</span></span>  <br/> |<span data-ttu-id="0c028-137">**visBow** (ArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="0c028-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="0c028-138">**visControlX** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="0c028-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="0c028-139">**visControlY** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="0c028-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="0c028-140">**visPolylineData** (Polylinie)</span><span class="sxs-lookup"><span data-stu-id="0c028-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="0c028-141">**visNURBSKnot** (NURBSTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="0c028-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="0c028-142">**visSplineKnot** (Zeile SplineStart-und SplineKnot-Zeilen)</span><span class="sxs-lookup"><span data-stu-id="0c028-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="0c028-143">**visInfiniteLineX2** (Unendliche Zeile)</span><span class="sxs-lookup"><span data-stu-id="0c028-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="0c028-144">**visEllipseMajorX** (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="0c028-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

