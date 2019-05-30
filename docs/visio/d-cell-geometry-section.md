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
ms.openlocfilehash: a76093f028986907b58175bc6b8c81a7056cfe07
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/29/2019
ms.locfileid: "34542499"
---
# <a name="d-cell-geometry-section"></a><span data-ttu-id="57628-104">Zelle "D" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="57628-104">D Cell (Geometry Section)</span></span>

<span data-ttu-id="57628-105">Stellt die Informationen in den verschiedenen Zeilen dar.</span><span class="sxs-lookup"><span data-stu-id="57628-105">Represents different information in different rows.</span></span> <span data-ttu-id="57628-106">Diese Tabelle beschreibt die Zelle D anhand der Zeile, in der sie sich befindet.</span><span class="sxs-lookup"><span data-stu-id="57628-106">This table describes the D cell based on the row in which it's located.</span></span>
  
|<span data-ttu-id="57628-107">Row</span><span class="sxs-lookup"><span data-stu-id="57628-107">Row</span></span>|<span data-ttu-id="57628-108">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="57628-108">Description</span></span>|
|:-----|:-----|
|[<span data-ttu-id="57628-109">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="57628-109">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> | <span data-ttu-id="57628-p103">Das Verhältnis zwischen der größeren und der kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die mit dem Ausdruck "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Wenn der Zellwert auf höchstens 0 bzw. auf größer als 1000 festgelegt wird, können unvorhersehbare Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="57628-p103">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="57628-113">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="57628-113">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> | <span data-ttu-id="57628-114">Die erste Stärke des nicht einheitlichen rationalen B-Splines (Nonuniform Rational B-spline, NURBS).</span><span class="sxs-lookup"><span data-stu-id="57628-114">The first weight of the nonuniform rational B-spline (NURBS).</span></span>  <br/> |
|[<span data-ttu-id="57628-115">Zeile SplineStart</span><span class="sxs-lookup"><span data-stu-id="57628-115">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> | <span data-ttu-id="57628-116">Der Grad eines Splines (eine ganze Zahl von 1 bis 25).</span><span class="sxs-lookup"><span data-stu-id="57628-116">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
|[<span data-ttu-id="57628-117">Ellipse</span><span class="sxs-lookup"><span data-stu-id="57628-117">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> | <span data-ttu-id="57628-118">Eine *y* -Koordinate eines Kommas auf einer Ellipse; gepaart mit der *x* -Koordinate, dargestellt durch die Zelle [C](c-cell-geometry-section.md) .</span><span class="sxs-lookup"><span data-stu-id="57628-118">A  *y*  -coordinate of a point on an ellipse; paired with the  *x*  -coordinate represented by the [C](c-cell-geometry-section.md) cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="57628-119">Hinweise</span><span class="sxs-lookup"><span data-stu-id="57628-119">Remarks</span></span>

<span data-ttu-id="57628-120">Wenn Sie einen Verweis auf die Zelle D aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="57628-120">To get a reference to the D cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="57628-121">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="57628-121">Cell name:</span></span>  <br/> | <span data-ttu-id="57628-122">Geometrie *i* . D *j* wobei *i* und *j* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="57628-122">Geometry  *i*  .D  *j*            where  *i*  and  *j*  = <1>, 2, 3...</span></span>  <br/> |
|| <span data-ttu-id="57628-123">Geometrie *i* . D1 (Ellipsen Zeile) wobei *i* = <1>, 2, 3...</span><span class="sxs-lookup"><span data-stu-id="57628-123">Geometry  *i*  .D1 (Ellipse row)            where  *i*  = <1>, 2, 3...</span></span>  <br/> |
   
<span data-ttu-id="57628-124">Wenn Sie einen Verweis auf die Zelle D aus einem Programm aus nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="57628-124">To get a reference to the D cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="57628-125">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="57628-125">Section index:</span></span>  <br/> |<span data-ttu-id="57628-126">**visSectionFirstComponent** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="57628-126">**visSectionFirstComponent** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="57628-127">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="57628-127">Row index:</span></span>  <br/> |<span data-ttu-id="57628-128">**visRowVertex** +  *j* , wobei *j* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="57628-128">**visRowVertex** +  *j*            where  *j*  = 0, 1, 2...</span></span>  <br/> |
||<span data-ttu-id="57628-129">**visRowVertex** (Ellipsen Zeile)</span><span class="sxs-lookup"><span data-stu-id="57628-129">**visRowVertex** (Ellipse row)</span></span>  <br/> |
| <span data-ttu-id="57628-130">Zellenindex</span><span class="sxs-lookup"><span data-stu-id="57628-130">Cell index</span></span>  <br/> |<span data-ttu-id="57628-131">**visAspectRatio** (EllipticalArcTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="57628-131">**visAspectRatio** (EllipticalArcTo row)</span></span>  <br/> |
||<span data-ttu-id="57628-132">**visNURBSWeightPrev** (NURBSTo-Zeile)</span><span class="sxs-lookup"><span data-stu-id="57628-132">**visNURBSWeightPrev** (NURBSTo row)</span></span>  <br/> |
||<span data-ttu-id="57628-133">**visSplineDegree** (Zeile SplineStart-Zeile)</span><span class="sxs-lookup"><span data-stu-id="57628-133">**visSplineDegree** (SplineStart row)</span></span>  <br/> |
||<span data-ttu-id="57628-134">**visEllipseMinorY** (Ellipsen Zeile)</span><span class="sxs-lookup"><span data-stu-id="57628-134">**visEllipseMinorY** (Ellipse row)</span></span>  <br/> |
   

