---
title: RelCubBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Enthält die X - und y - Koordinate des Endpunkts des eine kubische Bézierkurve relativ zu der Breite des Shapes und Höhe, X - und y - Koordinate des Kontrollpunkts des Beginns der Kurve relative Breite des Shapes und Höhe und die X- und y-Koordinaten des das Steuerelement l Kontrollpunkt des beenden, Breite und Höhe des relativen Kurve-Shapes.
ms.openlocfilehash: 918701c19e36753dcbf1a210dda2234d1e540d6d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797806"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="3cde3-103">RelCubBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="3cde3-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="3cde3-104">Enthält die *X* - und *y* - Koordinate des Endpunkts des eine kubische Bézierkurve relativ zu der Breite des Shapes und Höhe, *X* - und *y* -Koordinaten des Kontrollpunkts des Anfang der Breite und Höhe des relativen Kurve-Shapes und die *X* - und *y* -Koordinaten des Kontrollpunkts des beenden, Breite und Höhe des relativen Kurve-Shapes.</span><span class="sxs-lookup"><span data-stu-id="3cde3-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="3cde3-105">Eine Zeile **RelCubBezTo** kann nur in den Dateiformaten .vsdx, .vsdm, .vstx, .vstm, .vssx und .vssm beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="3cde3-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="3cde3-106">Wenn eine Datei in das Visio 2003-2010-Formate gespeichert wird, wird die Zeile **RelCubBezTo** in [eine Zeile NURBSTo](nurbsto-row-geometry-section.md) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="3cde3-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="3cde3-107">Eine Zeile **RelCubBezTo** enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="3cde3-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="3cde3-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="3cde3-108">**Cell**</span></span>|<span data-ttu-id="3cde3-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3cde3-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3cde3-110">X</span><span class="sxs-lookup"><span data-stu-id="3cde3-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="3cde3-111">Die *X* -Koordinate des Endscheitelpunkts einer kubischen Bézier-Kurve relativ zu der Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="3cde3-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3cde3-112">Y</span><span class="sxs-lookup"><span data-stu-id="3cde3-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="3cde3-113">Die *y* -Koordinate des Endscheitelpunkts einer kubischen Bézier-Kurve relativ zur Höhe des Shapes.</span><span class="sxs-lookup"><span data-stu-id="3cde3-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="3cde3-114">A</span><span class="sxs-lookup"><span data-stu-id="3cde3-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="3cde3-115">Die *X* -Koordinate der Kurve des Kontrollpunkts relativ zu der Breite des Shapes; beginnen ein Punkt auf dem Bogen. Kontrollpunkts befindet sich am besten zwischen dem ersten und letzten Scheitelpunkt des Bogens.</span><span class="sxs-lookup"><span data-stu-id="3cde3-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="3cde3-116">B</span><span class="sxs-lookup"><span data-stu-id="3cde3-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="3cde3-117">Die *y* -Koordinate einer Kurve des Kontrollpunkts relativ zur Höhe des Shapes beginnen.</span><span class="sxs-lookup"><span data-stu-id="3cde3-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="3cde3-118">C</span><span class="sxs-lookup"><span data-stu-id="3cde3-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="3cde3-119">Die *X* -Koordinate der Kurve Endpunkt des Kontrollpunkts relativ zu der Breite des Shapes; ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten zwischen die Anfang-Steuerelement Punkt und Beenden der Scheitelpunkte des Bogens.</span><span class="sxs-lookup"><span data-stu-id="3cde3-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="3cde3-120">D</span><span class="sxs-lookup"><span data-stu-id="3cde3-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="3cde3-121">Die *y* -Koordinate einer Kurve Endpunkt des Kontrollpunkts relativ zur Höhe des Shapes.</span><span class="sxs-lookup"><span data-stu-id="3cde3-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

