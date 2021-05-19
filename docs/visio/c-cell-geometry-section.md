---
title: Zelle "C" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm140
localization_priority: Normal
ms.assetid: d51a1dd8-678a-a34d-658d-bd7a027dd379
description: Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.
ms.openlocfilehash: 0284fea02c7eb890b56b6c865a69eb36662d8ae6
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541890"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="ce158-104">Zelle "C" (Abschnitt "Geometrie")</span><span class="sxs-lookup"><span data-stu-id="ce158-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="ce158-p102">Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="ce158-p102">Represents different information in different rows. This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="ce158-107">Zeile</span><span class="sxs-lookup"><span data-stu-id="ce158-107">Row</span></span>|<span data-ttu-id="ce158-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="ce158-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ce158-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="ce158-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="ce158-110">Der Winkel der Hauptachse eines Bogens relativ zur  *x-Achse*  des übergeordneten Bogens.</span><span class="sxs-lookup"><span data-stu-id="ce158-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="ce158-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="ce158-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="ce158-112">Der erste Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="ce158-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="ce158-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="ce158-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="ce158-114">Der letzte Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="ce158-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="ce158-115">Ellipse</span><span class="sxs-lookup"><span data-stu-id="ce158-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="ce158-116">Eine  x-Koordinate eines Punkts auf einer Ellipse; gekoppelt mit der y-Koordinate, die durch die [Zelle D dargestellt](d-cell-geometry-section.md) wird. </span><span class="sxs-lookup"><span data-stu-id="ce158-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ce158-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ce158-117">Remarks</span></span>

<span data-ttu-id="ce158-118">Um einen Verweis auf die Zelle C anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="ce158-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ce158-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ce158-119">Cell name:</span></span>  <br/> | <span data-ttu-id="ce158-120">Geometry  *i*  . C  *j,*            *wobei i*  und  *j*  = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="ce158-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="ce158-121">Geometry  *i*  . C1 (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="ce158-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="ce158-122">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle C nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="ce158-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ce158-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ce158-123">Section index:</span></span>  <br/> |<span data-ttu-id="ce158-124">**visSectionFirstComponent**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ce158-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="ce158-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ce158-125">Row index:</span></span>  <br/> |<span data-ttu-id="ce158-126">**visRowVertex**  +   *j,* *wobei j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="ce158-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="ce158-127">**visRowVertex** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="ce158-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="ce158-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ce158-128">Cell index:</span></span>  <br/> |<span data-ttu-id="ce158-129">**visEccentricityAngle** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="ce158-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="ce158-130">**visNURBSKnotPrev** (NURBSTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="ce158-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="ce158-131">**visSplineKnot3** (SplineStart-Zeile)</span><span class="sxs-lookup"><span data-stu-id="ce158-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="ce158-132">**visEllipseMinorX** (Ellipse-Zeile)</span><span class="sxs-lookup"><span data-stu-id="ce158-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

