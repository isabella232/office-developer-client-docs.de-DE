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
description: Stellt einen y-Koordinaten eines Shapes in lokalen Koordinaten dar. Die folgende Tabelle beschreibt die Zelle Y anhand der Zeile in der sie enthalten.
ms.openlocfilehash: 461fd0ec41d34132f469c811292550d2f7e094f0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798464"
---
# <a name="y-cell-geometry-section"></a><span data-ttu-id="6f42b-104">Y Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="6f42b-104">Y Cell (Geometry Section)</span></span>

<span data-ttu-id="6f42b-105">Stellt eine *y* -Koordinaten eines Shapes in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="6f42b-105">Represents a  *y*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="6f42b-106">Die folgende Tabelle beschreibt die Zelle Y anhand der Zeile in der sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f42b-106">This table describes the Y cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="6f42b-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="6f42b-107">**Row**</span></span>|<span data-ttu-id="6f42b-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f42b-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6f42b-109">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="6f42b-109">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-110">Wenn die Zeile MoveTo die erste Zeile im Abschnitt ist, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts eines Pfads.</span><span class="sxs-lookup"><span data-stu-id="6f42b-110">If the MoveTo row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="6f42b-111">Wenn die Zeile MoveTo zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.</span><span class="sxs-lookup"><span data-stu-id="6f42b-111">If the MoveTo row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="6f42b-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="6f42b-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-113">Die *y* -Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="6f42b-113">The  *y*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="6f42b-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="6f42b-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-115">Die *y* -Koordinate des Endscheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="6f42b-115">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="6f42b-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="6f42b-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-117">Die *y* -Koordinate des Endscheitelpunkts eines elliptischen Bogens.</span><span class="sxs-lookup"><span data-stu-id="6f42b-117">The  *y*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="6f42b-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="6f42b-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-119">Die *y* -Koordinate des Endscheitelpunkts einer Polylinie.</span><span class="sxs-lookup"><span data-stu-id="6f42b-119">The  *y*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="6f42b-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="6f42b-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-121">Die *y* -Koordinate des letzten Kontrollpunkts von einer nicht einheitlichen rationalen B-Spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="6f42b-121">The  *y*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="6f42b-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="6f42b-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-123">Die *y* -Koordinate des zweiten Kontrollpunkts eines Splines.</span><span class="sxs-lookup"><span data-stu-id="6f42b-123">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="6f42b-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="6f42b-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-125">Die *y* -Koordinate eines Kontrollpunkts.</span><span class="sxs-lookup"><span data-stu-id="6f42b-125">The  *y*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="6f42b-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="6f42b-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-127">Eine *y -* Koordinate eines Punkts auf der unendlichen Linie.</span><span class="sxs-lookup"><span data-stu-id="6f42b-127">A  *y-*  coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="6f42b-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="6f42b-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="6f42b-129">Die *y* -Koordinate des Mittelpunkts der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="6f42b-129">The  *y*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f42b-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6f42b-130">Remarks</span></span>

<span data-ttu-id="6f42b-131">Wenn Sie einen Verweis auf die Zelle Y nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6f42b-131">To get a reference to the Y cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f42b-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6f42b-132">Cell name:</span></span>  <br/> | <span data-ttu-id="6f42b-133">Geometrie *i* . Y *j* wobei *i* und *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6f42b-133">Geometry  *i*  .Y  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="6f42b-134">Geometrie *i* . Y1 (Zeilen UnendlicheLinie und Ellipse) wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="6f42b-134">Geometry  *i*  .Y1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="6f42b-135">Wenn Sie einen Verweis auf die Zelle Y aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6f42b-135">To get a reference to the Y cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f42b-136">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6f42b-136">Section index:</span></span>  <br/> |<span data-ttu-id="6f42b-137">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6f42b-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="6f42b-138">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6f42b-138">Row index:</span></span>  <br/> |<span data-ttu-id="6f42b-139">**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="6f42b-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="6f42b-140">**visRowVertex** (Zeilen UnendlicheLinie und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="6f42b-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="6f42b-141">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6f42b-141">Cell index:</span></span>  <br/> |<span data-ttu-id="6f42b-142">**visY** (Zeilen MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart und SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="6f42b-142">**visY** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="6f42b-143">**visInfiniteLineY1** (Zeile InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="6f42b-143">**visInfiniteLineY1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="6f42b-144">**visEllipseCenterY** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="6f42b-144">**visEllipseCenterY** (Ellipse row)</span></span>  <br/> |
   

