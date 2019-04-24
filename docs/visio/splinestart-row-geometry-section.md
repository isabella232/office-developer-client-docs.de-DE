---
title: Zeile "SplineStart" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3055
localization_priority: Normal
ms.assetid: 8e327e00-0844-efa4-900b-6954d3b009bb
description: Enthält x-und y-Koordinaten für den zweiten Kontrollpunkt eines Splines, den zweiten Knoten, den ersten Knoten, den letzten Knoten und den Grad des Splines.
ms.openlocfilehash: 2ec06619770af4e5dbcc1a763595b6e01a39052b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358793"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="53519-103">Zeile "SplineStart" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="53519-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="53519-104">Enthält *x* -und *y* -Koordinaten für den zweiten Kontrollpunkt eines Splines, den zweiten Knoten, den ersten Knoten, den letzten Knoten und den Grad des Splines.</span><span class="sxs-lookup"><span data-stu-id="53519-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="53519-105">Eine Zeile SplineStart enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="53519-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="53519-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="53519-106">**Cell**</span></span>|<span data-ttu-id="53519-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="53519-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="53519-108">X</span><span class="sxs-lookup"><span data-stu-id="53519-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="53519-109">Die *x* -Koordinate des zweiten Kontrollpunkts eines Splines.</span><span class="sxs-lookup"><span data-stu-id="53519-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="53519-110">Y</span><span class="sxs-lookup"><span data-stu-id="53519-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="53519-111">Die *y* -Koordinate des zweiten Kontrollpunkts eines Splines.</span><span class="sxs-lookup"><span data-stu-id="53519-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="53519-112">A</span><span class="sxs-lookup"><span data-stu-id="53519-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="53519-113">Der zweite Knoten des Splines.</span><span class="sxs-lookup"><span data-stu-id="53519-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="53519-114">B</span><span class="sxs-lookup"><span data-stu-id="53519-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="53519-115">Der erste Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="53519-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="53519-116">C</span><span class="sxs-lookup"><span data-stu-id="53519-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="53519-117">Der letzte Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="53519-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="53519-118">D</span><span class="sxs-lookup"><span data-stu-id="53519-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="53519-119">Der Grad eines Splines (eine Ganzzahl von 1 bis 25).</span><span class="sxs-lookup"><span data-stu-id="53519-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="53519-120">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="53519-120">Remarks</span></span>

<span data-ttu-id="53519-p101">Visio zeigt die Definition eines Splines im Abschnitt Geometry, in dem die Zeile SplineStart enthalten ist, der eine oder mehrere Zeile(n) SplineKnoten nachgestellt ist (sind). Der Zeile SplineStart muss eine andere Art von Zeile vorangehen, etwa MoveTo, die den ersten Kontrollpunkt des Splines anzeigt. Die vorangehende Zeile kann vom Typ LineTo, ArcTo, NURBSTo, PolylineTo oder EllipticalArcTo sein, wenn der Spline einem Segment dieses Typs folgt.</span><span class="sxs-lookup"><span data-stu-id="53519-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

