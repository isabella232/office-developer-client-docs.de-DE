---
title: Zelle "X" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1135
localization_priority: Normal
ms.assetid: 2416b323-e084-18e1-c9be-a797078dfab9
description: Stellt eine X-Koordinate eines Shapes in lokalen Koordinaten. Die folgende Tabelle beschreibt die Zelle X anhand der Zeile in der sie enthalten.
ms.openlocfilehash: e5bc99d4f73d49741c4378009dfc2a883bb655ed
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798429"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="854f4-104">X Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="854f4-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="854f4-105">Stellt eine *X* -Koordinate eines Shapes in lokalen Koordinaten.</span><span class="sxs-lookup"><span data-stu-id="854f4-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="854f4-106">Die folgende Tabelle beschreibt die Zelle X anhand der Zeile in der sie enthalten.</span><span class="sxs-lookup"><span data-stu-id="854f4-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="854f4-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="854f4-107">**Row**</span></span>|<span data-ttu-id="854f4-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="854f4-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="854f4-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="854f4-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-110">Wenn die Zeile MoveTo die erste Zeile im Abschnitt ist, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts eines Pfads.</span><span class="sxs-lookup"><span data-stu-id="854f4-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="854f4-111">Wenn die Zeile MoveTo zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.</span><span class="sxs-lookup"><span data-stu-id="854f4-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="854f4-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="854f4-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-113">Die *X* -Koordinate des Endscheitelpunkts eines geraden Linienabschnitts.</span><span class="sxs-lookup"><span data-stu-id="854f4-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="854f4-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="854f4-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-115">Die *X* -Koordinate des Endscheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="854f4-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="854f4-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="854f4-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-117">Die *X* -Koordinate des Endscheitelpunkts eines elliptischen Bogens.</span><span class="sxs-lookup"><span data-stu-id="854f4-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="854f4-118">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="854f4-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-119">Die *X* -Koordinate des Endscheitelpunkts einer Polylinie.</span><span class="sxs-lookup"><span data-stu-id="854f4-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="854f4-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="854f4-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-121">Die *X* -Koordinate des letzten Kontrollpunkts von einer nicht einheitlichen rationalen B-Spline (NURBS).</span><span class="sxs-lookup"><span data-stu-id="854f4-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="854f4-122">SplineStart</span><span class="sxs-lookup"><span data-stu-id="854f4-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-123">Die *X* -Koordinate des zweiten Kontrollpunkts eines Splines.</span><span class="sxs-lookup"><span data-stu-id="854f4-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="854f4-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="854f4-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-125">Die *X* -Koordinate eines Kontrollpunkts.</span><span class="sxs-lookup"><span data-stu-id="854f4-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="854f4-126">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="854f4-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-127">Eine *X* -Koordinate eines Punkts auf der unendlichen Linie.</span><span class="sxs-lookup"><span data-stu-id="854f4-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="854f4-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="854f4-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="854f4-129">Die *X* -Koordinate des Mittelpunkts der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="854f4-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="854f4-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="854f4-130">Remarks</span></span>

<span data-ttu-id="854f4-131">Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="854f4-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="854f4-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="854f4-132">Cell name:</span></span>  <br/> | <span data-ttu-id="854f4-133">Geometrie *i* . X *j* wobei *i* und *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="854f4-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="854f4-134">Geometrie *i* . X1 (Zeilen UnendlicheLinie und Ellipse) wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="854f4-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="854f4-135">Wenn Sie einen Verweis auf die Zelle X aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="854f4-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="854f4-136">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="854f4-136">Section index:</span></span>  <br/> |<span data-ttu-id="854f4-137">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="854f4-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="854f4-138">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="854f4-138">Row index:</span></span>  <br/> |<span data-ttu-id="854f4-139">**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="854f4-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="854f4-140">visRowVertex (Zeilen InfiniteLine und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="854f4-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="854f4-141">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="854f4-141">Cell index:</span></span>  <br/> |<span data-ttu-id="854f4-142">visX (Zeilen MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart und SplineKnot)</span><span class="sxs-lookup"><span data-stu-id="854f4-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="854f4-143">visInfiniteLineX1 (Zeile InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="854f4-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="854f4-144">visEllipseCenterX (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="854f4-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

