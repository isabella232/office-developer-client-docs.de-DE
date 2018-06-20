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
ms.openlocfilehash: 1b9a813be825f2deeb5c90d596ffd9f3705bcef6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796569"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="f448f-104">Zelle "C" (Abschnitt "Geometrie")</span><span class="sxs-lookup"><span data-stu-id="f448f-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="f448f-p102">Stellt die Informationen in den verschiedenen Zeilen dar. In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="f448f-p102">Represents different information in different rows. This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="f448f-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="f448f-107">**Row**</span></span>|<span data-ttu-id="f448f-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f448f-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f448f-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="f448f-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="f448f-110">Der Winkel der Größenachse des Bogens relativ zu der *X* -Achse des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="f448f-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="f448f-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="f448f-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="f448f-112">Der erste Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="f448f-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="f448f-113">SplineStart</span><span class="sxs-lookup"><span data-stu-id="f448f-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="f448f-114">Der letzte Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="f448f-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="f448f-115">Ellipse</span><span class="sxs-lookup"><span data-stu-id="f448f-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="f448f-116">Eine *X* -Koordinate eines Punkts auf der Ellipse; gepaart mit einer *y* -Koordinate, dargestellt durch die Zelle [D](d-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="f448f-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f448f-117">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f448f-117">Remarks</span></span>

<span data-ttu-id="f448f-118">Wenn Sie einen Verweis auf die Zelle C nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="f448f-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f448f-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="f448f-119">Cell name:</span></span>  <br/> | <span data-ttu-id="f448f-120">Geometrie *i* . C *j* wobei *i* und *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="f448f-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="f448f-121">Geometrie *i* . C1 (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="f448f-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="f448f-122">Wenn Sie einen Verweis auf die Zelle C aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="f448f-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="f448f-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="f448f-123">Section index:</span></span>  <br/> |<span data-ttu-id="f448f-124">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f448f-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="f448f-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="f448f-125">Row index:</span></span>  <br/> |<span data-ttu-id="f448f-126">**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="f448f-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="f448f-127">**visRowVertex** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="f448f-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="f448f-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="f448f-128">Cell index:</span></span>  <br/> |<span data-ttu-id="f448f-129">**visEccentricityAngle** (Zeile EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="f448f-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="f448f-130">**visNURBSKnotPrev** (Zeile NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="f448f-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="f448f-131">**visSplineKnot3** (Zeile SplineStart)</span><span class="sxs-lookup"><span data-stu-id="f448f-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="f448f-132">**visEllipseMinorX** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="f448f-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

