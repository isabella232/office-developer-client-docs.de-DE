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
# <a name="b-cell-geometry-section"></a><span data-ttu-id="31775-104">Zelle "B" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="31775-104">B Cell (Geometry Section)</span></span>

<span data-ttu-id="31775-105">Stellt die Informationen in den verschiedenen Zeilen dar.</span><span class="sxs-lookup"><span data-stu-id="31775-105">Represents different information in different rows.</span></span> <span data-ttu-id="31775-106">In der Tabelle wird die Zelle B auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="31775-106">This table describes the B cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="31775-107">Row</span><span class="sxs-lookup"><span data-stu-id="31775-107">Row</span></span>|<span data-ttu-id="31775-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="31775-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31775-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="31775-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="31775-110">Die *y* -Koordinate des Kontrollpunktes eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="31775-110">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="31775-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="31775-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="31775-112">Die zuletzt verwendete Linienstärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="31775-112">The last weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="31775-113">Zeile SplineStart</span><span class="sxs-lookup"><span data-stu-id="31775-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="31775-114">Der erste Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="31775-114">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="31775-115">Zeile InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="31775-115">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> | <span data-ttu-id="31775-116">Eine *y* -Koordinate eines Points auf einer unendlichen Leine; gepaart mit einer *x* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="31775-116">A  *y*  -coordinate of a point on an infinite line; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
|[<span data-ttu-id="31775-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="31775-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="31775-118">Eine *y* -Koordinate eines Kommas auf einer Ellipse; gepaart mit einer *x* -Koordinate, dargestellt durch die Zelle [A](a-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="31775-118">A  *y*  -coordinate of a point on an ellipse; paired with  *x*  -coordinate represented by the [A](a-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31775-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="31775-119">Remarks</span></span>

<span data-ttu-id="31775-120">Wenn Sie einen Verweis auf die Zelle B aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="31775-120">To get a reference to the B cell by name from another formula, or from a program, using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31775-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="31775-121">Cell name:</span></span>  <br/> | <span data-ttu-id="31775-122">Geometrie *i* . B *j* wobei *i* und *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="31775-122">Geometry  *i*  .B  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="31775-123">Geometrie *i* . B1 (Zeilen unendlich und Ellipse)</span><span class="sxs-lookup"><span data-stu-id="31775-123">Geometry  *i*  .B1 (InfiniteLine and Ellipse rows)</span></span>  <br/> |
   
<span data-ttu-id="31775-124">Wenn Sie einen Verweis auf die Zelle B aus einem Programm aus nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="31775-124">To get a reference to the B cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="31775-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="31775-125">Section index:</span></span>  <br/> |<span data-ttu-id="31775-126">**visSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="31775-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="31775-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="31775-127">Row index:</span></span>  <br/> |<span data-ttu-id="31775-128">**visRowVertex** +  *j* , wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="31775-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="31775-129">**visRowVertex** (Endlos-und Ellipsen Zeilen)</span><span class="sxs-lookup"><span data-stu-id="31775-129">**visRowVertex** (InfiniteLine and Ellipse rows)</span></span>  <br/> |
| <span data-ttu-id="31775-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="31775-130">Cell index:</span></span>  <br/> |<span data-ttu-id="31775-131">**visControlX** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="31775-131">**visControlX** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="31775-132">**visControlY** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="31775-132">**visControlY** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="31775-133">**visNURBSWeight** (NURBSTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="31775-133">**visNURBSWeight** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="31775-134">**visSplineKnot2** (Zeile SplineStart-Zeile)</span><span class="sxs-lookup"><span data-stu-id="31775-134">**visSplineKnot2** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="31775-135">**visInfiniteLineY2** (Endlos Zeile)</span><span class="sxs-lookup"><span data-stu-id="31775-135">**visInfiniteLineY2** (InfiniteLine row)</span></span>  <br/> |
||<span data-ttu-id="31775-136">**visEllipseMajorY** (Ellipsen Zeile)</span><span class="sxs-lookup"><span data-stu-id="31775-136">**visEllipseMajorY** (Ellipse row)</span></span>  <br/> |
   

