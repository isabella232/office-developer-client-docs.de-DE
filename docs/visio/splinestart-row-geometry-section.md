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
description: Enthält X- und y-Koordinaten des zweiten Kontrollpunkts eines Splines, dessen zweiten Knoten, dessen ersten Knoten, der letzte Knoten und den Grad eines Splines.
ms.openlocfilehash: 0944da12e6090fde41dc5927b5705e103d29f76d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798182"
---
# <a name="splinestart-row-geometry-section"></a><span data-ttu-id="f9ee2-103">SplineStart Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="f9ee2-103">SplineStart Row (Geometry Section)</span></span>

<span data-ttu-id="f9ee2-104">Enthält die *X* - und *y* -Koordinaten des zweiten Kontrollpunkts eines Splines, dessen zweiten Knoten, dessen ersten Knoten, der letzte Knoten und den Grad eines Splines.</span><span class="sxs-lookup"><span data-stu-id="f9ee2-104">Contains  *x*  - and  *y*  -coordinates for a spline's second control point, its second knot, its first knot, the last knot, and the degree of the spline.</span></span> 
  
<span data-ttu-id="f9ee2-105">Eine Zeile SplineStart enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="f9ee2-105">A SplineStart row contains the following cells.</span></span>
  
|<span data-ttu-id="f9ee2-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="f9ee2-106">**Cell**</span></span>|<span data-ttu-id="f9ee2-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f9ee2-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f9ee2-108">X</span><span class="sxs-lookup"><span data-stu-id="f9ee2-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="f9ee2-109">Die *X* -Koordinate des zweiten Kontrollpunkts eines Splines.</span><span class="sxs-lookup"><span data-stu-id="f9ee2-109">The  *x*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="f9ee2-110">Y</span><span class="sxs-lookup"><span data-stu-id="f9ee2-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="f9ee2-111">Die *y* -Koordinate des zweiten Kontrollpunkts eines Splines.</span><span class="sxs-lookup"><span data-stu-id="f9ee2-111">The  *y*  -coordinate of a spline's second control point.</span></span>  <br/> |
|[<span data-ttu-id="f9ee2-112">A</span><span class="sxs-lookup"><span data-stu-id="f9ee2-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="f9ee2-113">Der zweite Knoten des Splines.</span><span class="sxs-lookup"><span data-stu-id="f9ee2-113">The second knot of the spline.</span></span>  <br/> |
|[<span data-ttu-id="f9ee2-114">B</span><span class="sxs-lookup"><span data-stu-id="f9ee2-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="f9ee2-115">Der erste Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="f9ee2-115">The first knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="f9ee2-116">C</span><span class="sxs-lookup"><span data-stu-id="f9ee2-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="f9ee2-117">Der letzte Knoten eines Splines.</span><span class="sxs-lookup"><span data-stu-id="f9ee2-117">The last knot of a spline.</span></span>  <br/> |
|[<span data-ttu-id="f9ee2-118">D</span><span class="sxs-lookup"><span data-stu-id="f9ee2-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="f9ee2-119">Der Grad eines Splines (eine Ganzzahl von 1 bis 25).</span><span class="sxs-lookup"><span data-stu-id="f9ee2-119">The degree of a spline (an integer from 1 to 25).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f9ee2-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f9ee2-120">Remarks</span></span>

<span data-ttu-id="f9ee2-p101">Visio zeigt die Definition eines Splines im Abschnitt Geometry, in dem die Zeile SplineStart enthalten ist, der eine oder mehrere Zeile(n) SplineKnoten nachgestellt ist (sind). Der Zeile SplineStart muss eine andere Art von Zeile vorangehen, etwa MoveTo, die den ersten Kontrollpunkt des Splines anzeigt. Die vorangehende Zeile kann vom Typ LineTo, ArcTo, NURBSTo, PolylineTo oder EllipticalArcTo sein, wenn der Spline einem Segment dieses Typs folgt.</span><span class="sxs-lookup"><span data-stu-id="f9ee2-p101">Visio displays the definition of a spline in a Geometry section that contains a SplineStart row followed by one or more SplineKnot rows. The SplineStart row must be preceded by another kind of row, such as a MoveTo row, to indicate the first control point of the spline. The preceding row can be a LineTo, ArcTo, NURBSTo, PolylineTo, or EllipticalArcTo row if the spline follows a segment of that type.</span></span>
  

