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
ms.openlocfilehash: 7009658c7a6844a5c6071f502c05114a4accd7b7
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541302"
---
# <a name="a-cell-geometry-section"></a><span data-ttu-id="1c032-104">Zelle "A" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="1c032-104">A Cell (Geometry Section)</span></span>

<span data-ttu-id="1c032-p102">Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle A auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1c032-p102">Represents different information in different rows. This table describes the A cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="1c032-107">Zeile</span><span class="sxs-lookup"><span data-stu-id="1c032-107">Row</span></span>|<span data-ttu-id="1c032-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1c032-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c032-109">ArcTo</span><span class="sxs-lookup"><span data-stu-id="1c032-109">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="1c032-110">Der Abstand vom Mittelpunkt des Bogens bis zum Mittelpunkt seiner Sehne.</span><span class="sxs-lookup"><span data-stu-id="1c032-110">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
|[<span data-ttu-id="1c032-111">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="1c032-111">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="1c032-112">Die  x-Koordinate des Kontrollpunkts des Bogens, ein Punkt im Bogen. Der Kontrollpunkt befindet sich am besten ungefähr auf halbem Weg zwischen den Scheitelpunkte am Anfang und Ende des Bogens. Andernfalls kann der Bogen zu einer extremen Größe anwachsen, um den Kontrollpunkt mit unvorhersehbaren Ergebnissen zu passieren.</span><span class="sxs-lookup"><span data-stu-id="1c032-112">The  *x*  -coordinate of the arc's control point, a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="1c032-113">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="1c032-113">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="1c032-114">Die Polylinienformel.</span><span class="sxs-lookup"><span data-stu-id="1c032-114">The polyline formula.</span></span>  <br/> |
|[<span data-ttu-id="1c032-115">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="1c032-115">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="1c032-116">Der vorletzte Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="1c032-116">The second to the last knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="1c032-117">SplineStart</span><span class="sxs-lookup"><span data-stu-id="1c032-117">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="1c032-118">Der zweite Knoten des Splines.</span><span class="sxs-lookup"><span data-stu-id="1c032-118">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="1c032-119">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="1c032-119">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="1c032-120">Einer der Splineknoten (außer dem letzten bzw. den ersten beiden).</span><span class="sxs-lookup"><span data-stu-id="1c032-120">One of the spline's knots (other than the last one or the first two).</span></span>  <br/> |
|[<span data-ttu-id="1c032-121">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="1c032-121">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="1c032-122">Eine  x-Koordinate eines Punkts auf der unendlichen Linie; gekoppelt mit *y* -koordinate, die durch die [Zelle B dargestellt](b-cell-geometry-section.md) wird.</span><span class="sxs-lookup"><span data-stu-id="1c032-122">An  *x*  -coordinate of a point on the infinite line; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="1c032-123">Ellipse</span><span class="sxs-lookup"><span data-stu-id="1c032-123">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="1c032-124">Eine  x-Koordinate eines Punkts auf der Ellipse; gekoppelt mit *y* -koordinate, die durch die [Zelle B dargestellt](b-cell-geometry-section.md) wird.</span><span class="sxs-lookup"><span data-stu-id="1c032-124">An  *x*  -coordinate of a point on the ellipse; paired with  *y*  -coordinate represented by the [B](b-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c032-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c032-125">Remarks</span></span>

<span data-ttu-id="1c032-126">Verwenden Sie zum Erhalten eines Verweises auf die Zelle A anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="1c032-126">To get a reference to the A cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c032-127">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1c032-127">Cell name:</span></span>  <br/> | <span data-ttu-id="1c032-128">Geometry  *i*  . A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1c032-128">Geometry  *i*  .A  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="1c032-129">Geometry  *i*  . A1 (InfiniteLine- und Ellipsenzeilen),  *wobei i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1c032-129">Geometry  *i*  .A1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="1c032-130">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle A nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="1c032-130">To get a reference to the A cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1c032-131">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1c032-131">Section index:</span></span>  <br/> |<span data-ttu-id="1c032-132">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1c032-132">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1c032-133">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1c032-133">Row index:</span></span>  <br/> |<span data-ttu-id="1c032-134">**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1c032-134">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="1c032-135">**visRowVertex** (InfiniteLine- und Ellipsenzeilen)</span><span class="sxs-lookup"><span data-stu-id="1c032-135">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="1c032-136">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1c032-136">Cell index:</span></span>  <br/> |<span data-ttu-id="1c032-137">**visBow** (ArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1c032-137">**visBow** (ArcTo row)</span></span>  <br/> |
||<span data-ttu-id="1c032-138">**visControlX** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1c032-138">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="1c032-139">**visControlY** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1c032-139">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="1c032-140">**visPolylineData** (Polyline-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1c032-140">**visPolylineData** (Polyline row)</span></span>  <br/> |
||<span data-ttu-id="1c032-141">**visNURBSKnot** (NURBSTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1c032-141">**visNURBSKnot** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="1c032-142">**visSplineKnot** (SplineStart- und SplineKnot-Zeilen)</span><span class="sxs-lookup"><span data-stu-id="1c032-142">**visSplineKnot** (SplineStart and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="1c032-143">**visInfiniteLineX2** (InfiniteLine-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1c032-143">**visInfiniteLineX2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="1c032-144">**visEllipseMajorX** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="1c032-144">**visEllipseMajorX** (Ellipse row)</span></span>  <br/> |
   

