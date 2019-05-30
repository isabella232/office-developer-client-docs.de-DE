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
description: Stellt eine x-Koordinate eines Shapes in lokalen Koordinaten dar. Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: 2b3303533db446780ef797844ac5e1438cec242f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538214"
---
# <a name="x-cell-geometry-section"></a><span data-ttu-id="0f725-104">Zelle "X" (Abschnitt "Geometrie")</span><span class="sxs-lookup"><span data-stu-id="0f725-104">X Cell (Geometry Section)</span></span>

<span data-ttu-id="0f725-105">Stellt eine *x* -Koordinate eines Shapes in lokalen Koordinaten dar.</span><span class="sxs-lookup"><span data-stu-id="0f725-105">Represents an  *x*  -coordinate on a shape in local coordinates.</span></span> <span data-ttu-id="0f725-106">Diese Tabelle beschreibt die Zelle X anhand der Zeile, in der sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="0f725-106">This table describes the X cell based on the row in which it's located.</span></span> 
  
|<span data-ttu-id="0f725-107">Row</span><span class="sxs-lookup"><span data-stu-id="0f725-107">Row</span></span>|<span data-ttu-id="0f725-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0f725-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0f725-109">MoveTo</span><span class="sxs-lookup"><span data-stu-id="0f725-109">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-110">Wenn die MoveTo-Zeile die erste Zeile im Abschnitt ist, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts eines Pfads dar.</span><span class="sxs-lookup"><span data-stu-id="0f725-110">If the MoveTo row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a path.</span></span> <span data-ttu-id="0f725-111">Wenn die Zeile MoveTo zwischen zwei Zeilen angezeigt wird, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.</span><span class="sxs-lookup"><span data-stu-id="0f725-111">If the MoveTo row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="0f725-112">LineTo</span><span class="sxs-lookup"><span data-stu-id="0f725-112">LineTo</span></span>](lineto-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-113">Die *x* -Koordinate des letzten Scheitelpunkts eines geraden Linie Segments.</span><span class="sxs-lookup"><span data-stu-id="0f725-113">The  *x*  -coordinate of the ending vertex of a straight line segment.</span></span>  <br/> |
|[<span data-ttu-id="0f725-114">ArcTo</span><span class="sxs-lookup"><span data-stu-id="0f725-114">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-115">Die *x* -Koordinate des letzten Scheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="0f725-115">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="0f725-116">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="0f725-116">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-117">Die *x* -Koordinate des letzten Scheitelpunkts eines elliptischen Bogens.</span><span class="sxs-lookup"><span data-stu-id="0f725-117">The  *x*  -coordinate of the ending vertex of an elliptical arc.</span></span>  <br/> |
|[<span data-ttu-id="0f725-118">PolyLineTo</span><span class="sxs-lookup"><span data-stu-id="0f725-118">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-119">Die *x* -Koordinate des letzten Scheitelpunkts einer Polylinie.</span><span class="sxs-lookup"><span data-stu-id="0f725-119">The  *x*  -coordinate of the ending vertex of a polyline.</span></span>  <br/> |
|[<span data-ttu-id="0f725-120">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="0f725-120">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-121">Die *x* -Koordinate des letzten Kontrollpunktes eines nicht einheitlichen rationalen B-Splines (NURBS).</span><span class="sxs-lookup"><span data-stu-id="0f725-121">The  *x*  -coordinate of the last control point of a nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="0f725-122">Zeile SplineStart</span><span class="sxs-lookup"><span data-stu-id="0f725-122">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-123">Die *x* -Koordinate des zweiten Kontrollpunktes eines Splines.</span><span class="sxs-lookup"><span data-stu-id="0f725-123">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="0f725-124">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="0f725-124">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-125">Die *x* -Koordinate eines Kontrollpunktes.</span><span class="sxs-lookup"><span data-stu-id="0f725-125">The  *x*  -coordinate of a control point.</span></span>  <br/> |
|[<span data-ttu-id="0f725-126">Zeile InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="0f725-126">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-127">Eine *x* -Koordinate eines Points auf der unendlichen Reihe.</span><span class="sxs-lookup"><span data-stu-id="0f725-127">An  *x*  -coordinate of a point on the infinite line.</span></span>  <br/> |
|[<span data-ttu-id="0f725-128">Ellipse</span><span class="sxs-lookup"><span data-stu-id="0f725-128">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="0f725-129">Die *x* -Koordinate des Mittelpunkts der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="0f725-129">The  *x*  -coordinate of the center of the ellipse.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0f725-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0f725-130">Remarks</span></span>

<span data-ttu-id="0f725-131">Wenn Sie einen Verweis auf die Zelle X aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="0f725-131">To get a reference to the X cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f725-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0f725-132">Cell name:</span></span>  <br/> | <span data-ttu-id="0f725-133">Geometrie *i* . X *j* wobei *i* und *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0f725-133">Geometry  *i*  .X  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="0f725-134">Geometrie *i* . X1 (endlos-und Ellipsen Zeilen) wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="0f725-134">Geometry  *i*  .X1 (InfiniteLine and Ellipse rows)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="0f725-135">Wenn Sie einen Verweis auf die Zelle X aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="0f725-135">To get a reference to the X cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0f725-136">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0f725-136">Section index:</span></span>  <br/> |<span data-ttu-id="0f725-137">**visSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0f725-137">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="0f725-138">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0f725-138">Row index:</span></span>  <br/> |<span data-ttu-id="0f725-139">**visRowVertex** +  *j* , wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="0f725-139">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="0f725-140">**visRowVertex** (Endlos-und Ellipsen Zeilen)</span><span class="sxs-lookup"><span data-stu-id="0f725-140">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="0f725-141">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0f725-141">Cell index:</span></span>  <br/> |<span data-ttu-id="0f725-142">**visX** (MoveTo-, LineTo-, ArcTo-, EllipticalArcTo-, NURBSTo-, Polyline-, Zeile SplineStart-und SplineKnot-Zeilen)</span><span class="sxs-lookup"><span data-stu-id="0f725-142">**visX** (MoveTo, LineTo, ArcTo, EllipticalArcTo, NURBSTo, Polyline, SplineStart, and SplineKnot rows)</span></span>  <br/> |
||<span data-ttu-id="0f725-143">**visInfiniteLineX1** (Endlos Zeile)</span><span class="sxs-lookup"><span data-stu-id="0f725-143">**visInfiniteLineX1** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="0f725-144">**visEllipseCenterX** (Ellipsen Zeile)</span><span class="sxs-lookup"><span data-stu-id="0f725-144">**visEllipseCenterX** (Ellipse row)</span></span>  <br/> |
   

