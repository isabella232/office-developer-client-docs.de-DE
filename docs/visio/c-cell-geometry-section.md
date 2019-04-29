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
ms.openlocfilehash: 5599c09ad3656653c486d7feff9aed2ee89e4614
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413367"
---
# <a name="c-cell-geometry-section"></a><span data-ttu-id="3b329-104">Zelle "C" (Abschnitt "Geometrie")</span><span class="sxs-lookup"><span data-stu-id="3b329-104">C Cell (Geometry Section)</span></span>

<span data-ttu-id="3b329-105">Stellt die Informationen in den verschiedenen Zeilen dar.</span><span class="sxs-lookup"><span data-stu-id="3b329-105">Represents different information in different rows.</span></span> <span data-ttu-id="3b329-106">In der Tabelle wird die Zelle C auf der Grundlage der Zeile beschrieben, in der sie enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3b329-106">This table describes the C cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="3b329-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="3b329-107">**Row**</span></span>|<span data-ttu-id="3b329-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b329-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b329-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="3b329-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="3b329-110">Der Winkel der Hauptachse eines Bogens relativ zur *x* -Achse des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="3b329-110">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="3b329-111">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="3b329-111">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="3b329-112">Der erste Knoten des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="3b329-112">The first knot of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="3b329-113">Zeile SplineStart</span><span class="sxs-lookup"><span data-stu-id="3b329-113">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="3b329-114">Der letzte Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="3b329-114">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="3b329-115">Ellipse</span><span class="sxs-lookup"><span data-stu-id="3b329-115">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="3b329-116">Eine *x* -Koordinate eines Punkts auf einer Ellipse; gepaart mit der *y* -Koordinate, dargestellt durch die Zelle [D](d-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="3b329-116">An  *x*  -coordinate of a point on an ellipse; paired with the  *y*  -coordinate represented by the [D](d-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b329-117">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b329-117">Remarks</span></span>

<span data-ttu-id="3b329-118">Wenn Sie einen Verweis auf die Zelle C aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3b329-118">To get a reference to the C cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b329-119">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3b329-119">Cell name:</span></span>  <br/> | <span data-ttu-id="3b329-120">Geometrie *i* . C *j* wobei *i* und *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="3b329-120">Geometry  *i*  .C  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="3b329-121">Geometrie *i* . C1 (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="3b329-121">Geometry  *i*  .C1 (Ellipse row)</span></span>  <br/> |
   
<span data-ttu-id="3b329-122">Wenn Sie einen Verweis auf die Zelle C aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3b329-122">To get a reference to the C cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3b329-123">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3b329-123">Section index:</span></span>  <br/> |<span data-ttu-id="3b329-124">**visSectionFirstComponent** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3b329-124">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="3b329-125">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3b329-125">Row index:</span></span>  <br/> |<span data-ttu-id="3b329-126">**visRowVertex** +  *j* = \*\* 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="3b329-126">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="3b329-127">**visRowVertex** (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="3b329-127">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="3b329-128">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3b329-128">Cell index:</span></span>  <br/> |<span data-ttu-id="3b329-129">**visEccentricityAngle** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="3b329-129">**visEccentricityAngle** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="3b329-130">**visNURBSKnotPrev** (NURBSTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="3b329-130">**visNURBSKnotPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="3b329-131">**visSplineKnot3** (Zeile SplineStart-Zeile)</span><span class="sxs-lookup"><span data-stu-id="3b329-131">**visSplineKnot3** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="3b329-132">**visEllipseMinorX** (Zeile Ellipse)</span><span class="sxs-lookup"><span data-stu-id="3b329-132">**visEllipseMinorX** (Ellipse row)</span></span>  <br/> |
   

