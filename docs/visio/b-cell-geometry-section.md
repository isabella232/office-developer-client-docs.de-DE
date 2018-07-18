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
ms.openlocfilehash: 7d6f51d037be4852c6a101ad6e576a3a13488cb7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796421"
---
# <a name="b-cell-geometry-section"></a><span data-ttu-id="87615-104">B Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="87615-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="87615-p102">Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="87615-p102">Represents different information in different rows. This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="87615-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="87615-107">**Row**</span></span>|<span data-ttu-id="87615-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87615-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87615-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="87615-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="87615-110">Die *y* -Koordinate des Kontrollpunkts des Bogens.</span><span class="sxs-lookup"><span data-stu-id="87615-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="87615-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="87615-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="87615-112">Die zuletzt verwendete Linienstärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="87615-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="87615-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="87615-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="87615-114">Der erste Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="87615-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="87615-115">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="87615-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="87615-116">Eine *y* -Koordinate eines Punkts auf der unendlichen Linie; gepaart mit einer *X* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="87615-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="87615-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="87615-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="87615-118">Eine *y* -Koordinate eines Punkts auf der Ellipse; gepaart mit einer *X* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="87615-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87615-119">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="87615-119">Remarks</span></span>

<span data-ttu-id="87615-120">Wenn Sie eine Referenz auf die Zelle B nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="87615-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87615-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="87615-121">Cell name:</span></span>  <br/> | <span data-ttu-id="87615-122">Geometrie *i* . B *j* wobei *i* und *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="87615-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="87615-123">Geometrie *i* . B1 (Zeilen UnendlicheLinie und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="87615-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="87615-124">Wenn Sie eine Referenz auf die Zelle B aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="87615-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="87615-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="87615-125">Section index:</span></span>  <br/> |<span data-ttu-id="87615-126">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="87615-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="87615-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="87615-127">Row index:</span></span>  <br/> |<span data-ttu-id="87615-128">**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="87615-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="87615-129">visRowVertex (Zeilen InfiniteLine und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="87615-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="87615-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="87615-130">Cell index:</span></span>  <br/> |<span data-ttu-id="87615-131">visControlX (Zeile EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="87615-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="87615-132">visControlY (Zeile EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="87615-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="87615-133">visNURBSWeight (Zeile NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="87615-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="87615-134">visSplineKnot2 (Zeile SplineStart)</span><span class="sxs-lookup"><span data-stu-id="87615-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="87615-135">visInfiniteLineY2 (Zeile InfiniteLine)</span><span class="sxs-lookup"><span data-stu-id="87615-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="87615-136">visEllipseMajorY (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="87615-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

