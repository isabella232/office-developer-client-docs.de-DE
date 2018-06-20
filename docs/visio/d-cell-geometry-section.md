---
title: Zelle "D" (Abschnitt "Geometrie")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251753
localization_priority: Normal
ms.assetid: 5f1fdf59-db58-561c-e187-1af72a8b87f2
description: Stellt die Informationen in den verschiedenen Zeilen dar. Diese Tabelle beschreibt die Zelle D anhand der Zeile, in der sie sich befindet.
ms.openlocfilehash: ed67197e46ee159ba2175b0e86623fe1704992d2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796763"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="60715-104">D Cell (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="60715-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="60715-p102">Stellt die Informationen in den verschiedenen Zeilen dar. Diese Tabelle beschreibt die Zelle D anhand der Zeile, in der sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="60715-p102">Represents different information in different rows. This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="60715-107">**Row**</span><span class="sxs-lookup"><span data-stu-id="60715-107">**Row**</span></span>|<span data-ttu-id="60715-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="60715-108">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="60715-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="60715-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="60715-p103">Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="60715-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="60715-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="60715-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="60715-114">Die erste Stärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="60715-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="60715-115">SplineStart</span><span class="sxs-lookup"><span data-stu-id="60715-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="60715-116">Der Grad eines Splines (eine Ganzzahl von 1 bis 25).</span><span class="sxs-lookup"><span data-stu-id="60715-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="60715-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="60715-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="60715-118">Eine *y* -Koordinate eines Punkts auf der Ellipse; gepaart mit einer *X* -Koordinate, dargestellt durch die Zelle [C](c-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="60715-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60715-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="60715-119">Remarks</span></span>

<span data-ttu-id="60715-120">Wenn Sie einen Verweis auf die Zelle D nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="60715-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60715-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="60715-121">Cell name:</span></span>  <br/> | <span data-ttu-id="60715-122">Geometrie *i* . D *j* wobei *i* und *j* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="60715-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="60715-123">Geometrie *i* . D1 (Zeile Ellipse) wobei *i* = < 1 >, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="60715-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="60715-124">Wenn Sie einen Verweis auf die Zelle D aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="60715-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="60715-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="60715-125">Section index:</span></span>  <br/> |<span data-ttu-id="60715-126">**VisSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="60715-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="60715-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="60715-127">Row index:</span></span>  <br/> |<span data-ttu-id="60715-128">**VisRowVertex** +  *j* wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="60715-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="60715-129">**visRowVertex** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="60715-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="60715-130">Zellenindex</span><span class="sxs-lookup"><span data-stu-id="60715-130">Cell index</span></span>  <br/> |<span data-ttu-id="60715-131">**visAspectRatio** (Zeile EllipticalArcTo)</span><span class="sxs-lookup"><span data-stu-id="60715-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="60715-132">**visNURBSWeightPrev** (Zeile NURBSTo)</span><span class="sxs-lookup"><span data-stu-id="60715-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="60715-133">**visSplineDegree** (Zeile SplineStart)</span><span class="sxs-lookup"><span data-stu-id="60715-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="60715-134">**visEllipseMinorY** (Ellipsenzeile)</span><span class="sxs-lookup"><span data-stu-id="60715-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

