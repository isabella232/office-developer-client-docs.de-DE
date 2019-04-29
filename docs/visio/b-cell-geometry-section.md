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
ms.openlocfilehash: ff032b5af2918ec9865360ede5c3d76e8e872e9a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423307"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="1df7e-104">Zelle "B" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="1df7e-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="1df7e-105">Stellt die Informationen in den verschiedenen Zeilen dar.</span><span class="sxs-lookup"><span data-stu-id="1df7e-105">Represents different information in different rows.</span></span> <span data-ttu-id="1df7e-106">In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="1df7e-106">This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="1df7e-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="1df7e-107">**Row**</span></span>|<span data-ttu-id="1df7e-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1df7e-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1df7e-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="1df7e-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="1df7e-110">Die *y* -Koordinate des Kontrollpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="1df7e-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="1df7e-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="1df7e-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="1df7e-112">Die zuletzt verwendete Linienstärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="1df7e-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="1df7e-113">Zeile SplineStart</span><span class="sxs-lookup"><span data-stu-id="1df7e-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="1df7e-114">Der erste Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="1df7e-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="1df7e-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="1df7e-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="1df7e-116">Eine *y* -Koordinate eines Punkts auf einer unendlichen Achse. gepaart mit einer *x* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="1df7e-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="1df7e-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="1df7e-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="1df7e-118">Eine *y* -Koordinate eines Punkts auf einer Ellipse; gepaart mit einer *x* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="1df7e-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1df7e-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="1df7e-119">Remarks</span></span>

<span data-ttu-id="1df7e-120">Wenn Sie einen Verweis auf die Zelle B aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="1df7e-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1df7e-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="1df7e-121">Cell name:</span></span>  <br/> | <span data-ttu-id="1df7e-122">Geometrie *i* . B *j* wobei *i* und *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="1df7e-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="1df7e-123">Geometrie *i* . B1 (Zeilen für unendliche und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="1df7e-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="1df7e-124">Wenn Sie einen Verweis auf die Zelle B aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="1df7e-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="1df7e-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="1df7e-125">Section index:</span></span>  <br/> |<span data-ttu-id="1df7e-126">**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1df7e-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="1df7e-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="1df7e-127">Row index:</span></span>  <br/> |<span data-ttu-id="1df7e-128">**visRowVertex** +  *j* = \*\* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="1df7e-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="1df7e-129">**visRowVertex** (Zeilen für unendliche und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="1df7e-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="1df7e-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="1df7e-130">Cell index:</span></span>  <br/> |<span data-ttu-id="1df7e-131">**visControlX** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1df7e-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="1df7e-132">**visControlY** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1df7e-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="1df7e-133">**visNURBSWeight** (NURBSTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1df7e-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="1df7e-134">**visSplineKnot2** (Zeile SplineStart-Zeile)</span><span class="sxs-lookup"><span data-stu-id="1df7e-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="1df7e-135">**visInfiniteLineY2** (Unendliche Zeile)</span><span class="sxs-lookup"><span data-stu-id="1df7e-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="1df7e-136">**visEllipseMajorY** (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="1df7e-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

