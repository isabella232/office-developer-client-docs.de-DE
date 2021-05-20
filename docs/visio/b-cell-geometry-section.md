---
title: Zelle "B" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251751
localization_priority: Normal
ms.assetid: b0fb6a47-47d8-ab9c-854d-0b0bbfdfcc27
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: 46c8aa418f495905630fed2833d84afc93945346
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537794"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="462e7-104">Zelle "B" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="462e7-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="462e7-p102">Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="462e7-p102">Represents different information in different rows. This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="462e7-107">Zeile</span><span class="sxs-lookup"><span data-stu-id="462e7-107">Row</span></span>|<span data-ttu-id="462e7-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="462e7-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="462e7-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="462e7-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="462e7-110">Die  y-Koordinate des Kontrollpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="462e7-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="462e7-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="462e7-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="462e7-112">Die zuletzt verwendete Linienstärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="462e7-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="462e7-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="462e7-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="462e7-114">Der erste Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="462e7-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="462e7-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="462e7-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="462e7-116">Eine  y-Koordinate eines Punkts in einer unendlichen Linie; gekoppelt mit *x* -koordinate, die durch die [Zelle A dargestellt](a-cell-geometry-section.md) wird.</span><span class="sxs-lookup"><span data-stu-id="462e7-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="462e7-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="462e7-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="462e7-118">Eine  y-Koordinate eines Punkts auf einer Ellipse; gekoppelt mit *x* -koordinate, die durch die [Zelle A dargestellt](a-cell-geometry-section.md) wird.</span><span class="sxs-lookup"><span data-stu-id="462e7-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="462e7-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="462e7-119">Remarks</span></span>

<span data-ttu-id="462e7-120">Verwenden Sie zum Erhalten eines Verweises auf die Zelle B anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="462e7-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="462e7-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="462e7-121">Cell name:</span></span>  <br/> | <span data-ttu-id="462e7-122">Geometry  *i*  . B  *j,*            *wobei i*  und  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="462e7-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="462e7-123">Geometry  *i*  . B1 (InfiniteLine- und Ellipsenzeilen)</span><span class="sxs-lookup"><span data-stu-id="462e7-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="462e7-124">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle B nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="462e7-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="462e7-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="462e7-125">Section index:</span></span>  <br/> |<span data-ttu-id="462e7-126">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="462e7-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="462e7-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="462e7-127">Row index:</span></span>  <br/> |<span data-ttu-id="462e7-128">**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="462e7-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="462e7-129">**visRowVertex** (InfiniteLine- und Ellipsenzeilen)</span><span class="sxs-lookup"><span data-stu-id="462e7-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="462e7-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="462e7-130">Cell index:</span></span>  <br/> |<span data-ttu-id="462e7-131">**visControlX** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="462e7-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="462e7-132">**visControlY** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="462e7-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="462e7-133">**visNURBSWeight** (NURBSTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="462e7-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="462e7-134">**visSplineKnot2** (SplineStart-Zeile)</span><span class="sxs-lookup"><span data-stu-id="462e7-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="462e7-135">**visInfiniteLineY2** (InfiniteLine-Zeile)</span><span class="sxs-lookup"><span data-stu-id="462e7-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="462e7-136">**visEllipseMajorY** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="462e7-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

