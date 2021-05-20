---
title: Zelle "Y" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251750
localization_priority: Normal
ms.assetid: a53b5787-f419-7a36-3c04-c63b3c173ac7
description: Stellt eine y-Koordinate in einer Form in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 7dea96b544c84f09abe1d72304da0bacaa09432f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540490"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="2760c-104">Zelle "Y" (Abschnitt "Geometrie")</span><span class="sxs-lookup"><span data-stu-id="2760c-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="2760c-105">Stellt  eine y-Koordinate in einer Form in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="2760c-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="2760c-106">Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="2760c-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="2760c-107">Zeile</span><span class="sxs-lookup"><span data-stu-id="2760c-107">Row</span></span>|<span data-ttu-id="2760c-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2760c-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="2760c-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="2760c-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-110">Wenn die MoveTo-Zeile die erste Zeile im Abschnitt  ist, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts eines Pfads dar.</span><span class="sxs-lookup"><span data-stu-id="2760c-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="2760c-111">Wenn die MoveTo-Zeile zwischen zwei Zeilen angezeigt  wird, stellt die Zelle Y die y-Koordinate des ersten Scheitelpunkts nach dem Umbruch im Pfad dar.</span><span class="sxs-lookup"><span data-stu-id="2760c-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="2760c-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="2760c-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-113">Die  y-Koordinate des endenden Scheitelpunkts eines geraden Abschnitts.</span><span class="sxs-lookup"><span data-stu-id="2760c-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="2760c-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="2760c-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-115">Die  y-Koordinate des endenden Scheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="2760c-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="2760c-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="2760c-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-117">Die  y-Koordinate des endenden Scheitelpunkts eines elliptischen Bogens.</span><span class="sxs-lookup"><span data-stu-id="2760c-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="2760c-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="2760c-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-119">Die  y-Koordinate des endenden Scheitelpunkts einer Polylinie.</span><span class="sxs-lookup"><span data-stu-id="2760c-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="2760c-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="2760c-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-121">Die  y-Koordinate des letzten Kontrollpunkts eines nicht einheitlich rationalen B-Splines (NURBS).</span><span class="sxs-lookup"><span data-stu-id="2760c-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="2760c-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="2760c-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-123">Die  y-Koordinate des zweiten Kontrollpunkts eines Splines.</span><span class="sxs-lookup"><span data-stu-id="2760c-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="2760c-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="2760c-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-125">Die  y-Koordinate eines Kontrollpunkts.</span><span class="sxs-lookup"><span data-stu-id="2760c-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="2760c-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="2760c-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-127">Eine  *y-Koordinate*  eines Punkts auf der unendlichen Linie.</span><span class="sxs-lookup"><span data-stu-id="2760c-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="2760c-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="2760c-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="2760c-129">Die  y-Koordinate der Mitte der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="2760c-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2760c-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2760c-130">Remarks</span></span>

<span data-ttu-id="2760c-131">Um einen Verweis auf die Zelle Y anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2760c-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2760c-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2760c-132">Cell name:</span></span>  <br/> | <span data-ttu-id="2760c-133">Geometry  *i*  . Y  *j,*            *wobei i*  und  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2760c-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="2760c-134">Geometry  *i*  . Y1 (InfiniteLine- und Ellipsenzeilen), wobei  *i*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="2760c-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="2760c-135">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Y nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2760c-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2760c-136">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2760c-136">Section index:</span></span>  <br/> |<span data-ttu-id="2760c-137">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2760c-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2760c-138">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2760c-138">Row index:</span></span>  <br/> |<span data-ttu-id="2760c-139">**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2760c-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="2760c-140">**visRowVertex** (InfiniteLine- und Ellipsenzeilen)</span><span class="sxs-lookup"><span data-stu-id="2760c-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="2760c-141">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2760c-141">Cell index:</span></span>  <br/> |<span data-ttu-id="2760c-142">**visY** (Zeilen MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart und SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="2760c-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="2760c-143">**visInfiniteLineY1** (InfiniteLine-Zeile)</span><span class="sxs-lookup"><span data-stu-id="2760c-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="2760c-144">**visEllipseCenterY** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="2760c-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

