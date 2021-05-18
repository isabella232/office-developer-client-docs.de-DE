---
title: Zeile "Ellipse" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3010
localization_priority: Normal
ms.assetid: 183fb303-4acb-a486-7b97-f11f7ae3978f
description: Enthält die x- und y-Koordinaten des Mittelpunkts der Ellipse und zwei Punkte auf der Ellipse.
ms.openlocfilehash: 5121ba0c7bf97eaeaaf8a438dd40eccddada4362
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421830"
---
# <a name="ellipse-row-geometry-section"></a><span data-ttu-id="e59ef-103">Zeile "Ellipse" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="e59ef-103">Ellipse Row (Geometry Section)</span></span>

<span data-ttu-id="e59ef-104">Enthält die  *x-*  und  *y-Koordinaten*  des Mittelpunkts der Ellipse und zwei Punkte auf der Ellipse.</span><span class="sxs-lookup"><span data-stu-id="e59ef-104">Contains the  *x*  - and  *y*  -coordinates of the ellipse's center point and two points on the ellipse.</span></span> 
  
<span data-ttu-id="e59ef-105">Eine Zeile Ellipse enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="e59ef-105">An Ellipse row contains the following cells.</span></span>
  
|<span data-ttu-id="e59ef-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e59ef-106">**Cell**</span></span>|<span data-ttu-id="e59ef-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e59ef-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e59ef-108">X</span><span class="sxs-lookup"><span data-stu-id="e59ef-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="e59ef-109">Die  x-Koordinate des Mittelpunkts.</span><span class="sxs-lookup"><span data-stu-id="e59ef-109">The  *x*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="e59ef-110">Y</span><span class="sxs-lookup"><span data-stu-id="e59ef-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="e59ef-111">Die  y-Koordinate des Mittelpunkts.</span><span class="sxs-lookup"><span data-stu-id="e59ef-111">The  *y*  -coordinate of the center point.</span></span>  <br/> |
|[<span data-ttu-id="e59ef-112">A</span><span class="sxs-lookup"><span data-stu-id="e59ef-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="e59ef-113">Die x-Koordinate eines Punkts auf der Ellipse; gekoppelt mit  *y*  -koordinate, die durch die Zelle B dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e59ef-113">The x-coordinate of one point on the ellipse; paired with  *y*  -coordinate represented by the B cell.</span></span>  <br/> |
|[<span data-ttu-id="e59ef-114">B</span><span class="sxs-lookup"><span data-stu-id="e59ef-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="e59ef-115">Die  y-Koordinate eines Punkts auf der Ellipse; gekoppelt mit x-Koordinate, die durch die Zelle A dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="e59ef-115">The  *y*  -coordinate of one point on the ellipse; paired with x-coordinate represented by the A cell.</span></span>  <br/> |
|[<span data-ttu-id="e59ef-116">C</span><span class="sxs-lookup"><span data-stu-id="e59ef-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="e59ef-117">Die  x-Koordinate eines anderen Punkts auf der Ellipse; gekoppelt mit der y-Koordinate, die durch die Zelle D dargestellt wird. </span><span class="sxs-lookup"><span data-stu-id="e59ef-117">The  *x*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the D cell.</span></span>  <br/> |
|[<span data-ttu-id="e59ef-118">D</span><span class="sxs-lookup"><span data-stu-id="e59ef-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="e59ef-119">Die  y-Koordinate eines anderen Punkts auf der Ellipse; gekoppelt mit der y-Koordinate, die durch die Zelle C dargestellt wird. </span><span class="sxs-lookup"><span data-stu-id="e59ef-119">The  *y*  -coordinate of another point on the ellipse; paired with  *y*  -coordinate represented by the C cell.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e59ef-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e59ef-120">Remarks</span></span>

<span data-ttu-id="e59ef-121">Ein Abschnitt Geometry, der eine Zeile Ellipse oder InfiniteLine enthält, sollte keine anderen Zeilen enthalten.</span><span class="sxs-lookup"><span data-stu-id="e59ef-121">A geometry section that contains an Ellipse or an InfiniteLine row should not contain any other rows.</span></span>
  

