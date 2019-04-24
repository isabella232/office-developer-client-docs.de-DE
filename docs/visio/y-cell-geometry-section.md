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
description: Stellt eine y-Koordinate für ein Shape in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 9e823b8d21682b419a70ce498016abf575f36f6b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342812"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="ffe49-104">Zelle "Y" (Abschnitt "Geometrie")</span><span class="sxs-lookup"><span data-stu-id="ffe49-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="ffe49-105">Stellt eine *y* -Koordinate für ein Shape in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="ffe49-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="ffe49-106">Diese Tabelle beschreibt die Zelle Y anhand der Zeile, in der sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="ffe49-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="ffe49-107">**Zeile**</span><span class="sxs-lookup"><span data-stu-id="ffe49-107">**Row**</span></span>|<span data-ttu-id="ffe49-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ffe49-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ffe49-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="ffe49-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-110">Wenn die MoveTo-Zeile die erste Zeile im Abschnitt ist, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts eines Pfads dar.</span><span class="sxs-lookup"><span data-stu-id="ffe49-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="ffe49-111">Wenn die MoveTo-Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.</span><span class="sxs-lookup"><span data-stu-id="ffe49-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="ffe49-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="ffe49-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-113">Die *y* -Koordinate des Endpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="ffe49-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="ffe49-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="ffe49-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-115">Die *y* -Koordinate des Endpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="ffe49-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="ffe49-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="ffe49-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-117">Die *y* -Koordinate des Endpunkts eines elliptischen Bogens.</span><span class="sxs-lookup"><span data-stu-id="ffe49-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="ffe49-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="ffe49-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-119">Die *y* -Koordinate des Endpunkts einer Polylinie.</span><span class="sxs-lookup"><span data-stu-id="ffe49-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="ffe49-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="ffe49-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-121">Die *y* -Koordinate des letzten Kontrollpunkts eines nicht einheitlichen rationalen B-Splines (NURBS).</span><span class="sxs-lookup"><span data-stu-id="ffe49-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="ffe49-122">Zeile SplineStart</span><span class="sxs-lookup"><span data-stu-id="ffe49-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-123">Die *y* -Koordinate des zweiten Kontrollpunkts eines Splines.</span><span class="sxs-lookup"><span data-stu-id="ffe49-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="ffe49-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="ffe49-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-125">Die *y* -Koordinate eines Kontrollpunkts.</span><span class="sxs-lookup"><span data-stu-id="ffe49-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="ffe49-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="ffe49-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-127">Eine *y-* Koordinate eines Punkts auf der unendlichen Achse.</span><span class="sxs-lookup"><span data-stu-id="ffe49-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="ffe49-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="ffe49-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="ffe49-129">Die *y* -Koordinate des Mittelpunkts der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="ffe49-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ffe49-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ffe49-130">Remarks</span></span>

<span data-ttu-id="ffe49-131">Wenn Sie einen Verweis auf die Zelle Y aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ffe49-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ffe49-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ffe49-132">Cell name:</span></span>  <br/> | <span data-ttu-id="ffe49-133">Geometrie *i* . Y *j* wobei *i* und *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ffe49-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="ffe49-134">Geometrie *i* . Y1 (Zeilen für unendliche und Ellipse) wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ffe49-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="ffe49-135">Wenn Sie einen Verweis auf die Zelle Y nach Index aus einem Programm erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ffe49-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ffe49-136">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ffe49-136">Section index:</span></span>  <br/> |<span data-ttu-id="ffe49-137">**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ffe49-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ffe49-138">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ffe49-138">Row index:</span></span>  <br/> |<span data-ttu-id="ffe49-139">**visRowVertex** +  *j* = \*\* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ffe49-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="ffe49-140">**visRowVertex** (Zeilen für unendliche und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="ffe49-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="ffe49-141">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ffe49-141">Cell index:</span></span>  <br/> |<span data-ttu-id="ffe49-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polylinie, Zeile SplineStart und SplineKnot Zeilen)</span><span class="sxs-lookup"><span data-stu-id="ffe49-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="ffe49-143">**visInfiniteLineY1** (Unendliche Zeile)</span><span class="sxs-lookup"><span data-stu-id="ffe49-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="ffe49-144">**visEllipseCenterY** (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="ffe49-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

