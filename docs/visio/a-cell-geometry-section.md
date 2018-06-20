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
ms.openlocfilehash: b907552c2346292a6b14baf16481b6b40cc80fc4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796363"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="d3281-104">A Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="d3281-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="d3281-p102">Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="d3281-p102">Represents different information in different rows. This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="d3281-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="d3281-107">**Row**</span></span>|<span data-ttu-id="d3281-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d3281-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d3281-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="d3281-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="d3281-110">Der Abstand vom Mittelpunkt des Bogens bis zum Mittelpunkt seiner Sehne.</span><span class="sxs-lookup"><span data-stu-id="d3281-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="d3281-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="d3281-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="d3281-112">Die *X* -Koordinate des Kontrollpunkts des Bogens, einen Punkt auf dem Bogen. Kontrollpunkts ist die beste in der Mitte zwischen dem ersten und letzten Scheitelpunkt des Bogens. Andernfalls kann Bogens extrem große anwachsen, um passieren Kontrollpunkts weitergibt.</span><span class="sxs-lookup"><span data-stu-id="d3281-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="d3281-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="d3281-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="d3281-114">Die Polylinienformel.</span><span class="sxs-lookup"><span data-stu-id="d3281-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="d3281-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="d3281-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="d3281-116">Der vorletzte Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="d3281-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="d3281-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="d3281-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="d3281-118">Der zweite Knoten des Splines.</span><span class="sxs-lookup"><span data-stu-id="d3281-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="d3281-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="d3281-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="d3281-120">Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).</span><span class="sxs-lookup"><span data-stu-id="d3281-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="d3281-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="d3281-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="d3281-122">Eine *X* -Koordinate eines Punkts auf der unendlichen Linie gepaart mit einer *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="d3281-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="d3281-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="d3281-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="d3281-124">Eine *X* -Koordinate eines Punkts auf der Ellipse; gepaart mit einer *y* -Koordinate, dargestellt durch die Zelle [B](b-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="d3281-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d3281-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d3281-125">Remarks</span></span>

<span data-ttu-id="d3281-126">Zum Abrufen eines Verweises auf die Zelle A nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft verwenden Sie zu können:</span><span class="sxs-lookup"><span data-stu-id="d3281-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3281-127">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d3281-127">Cell name:</span></span>  <br/> | <span data-ttu-id="d3281-128">Geometrie *i* . Ein *j* wobei *i* und *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d3281-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="d3281-129">Geometrie *i* . A1 (Zeilen UnendlicheLinie und Ellipse) wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="d3281-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="d3281-130">Wenn Sie einen Verweis auf die Zelle A aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d3281-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d3281-131">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d3281-131">Section index:</span></span>  <br/> |<span data-ttu-id="d3281-132">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d3281-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="d3281-133">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d3281-133">Row index:</span></span>  <br/> |<span data-ttu-id="d3281-134">**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="d3281-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="d3281-135">**visRowVertex** (Zeilen UnendlicheLinie und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="d3281-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="d3281-136">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d3281-136">Cell index:</span></span>  <br/> |<span data-ttu-id="d3281-137">**visBow** (Zeile ArcTo)</span><span class="sxs-lookup"><span data-stu-id="d3281-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="d3281-138">**visControlX** (Zeile EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="d3281-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="d3281-139">**visControlY** (Zeile EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="d3281-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="d3281-140">**visPolylineData** (Zeile Polyline)</span><span class="sxs-lookup"><span data-stu-id="d3281-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="d3281-141">**visNURBSKnot** (Zeile NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="d3281-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="d3281-142">**visSplineKnot** (Zeilen SplineStart und SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="d3281-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="d3281-143">**visInfiniteLineX2** (Zeile InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="d3281-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="d3281-144">**visEllipseMinorX** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="d3281-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

