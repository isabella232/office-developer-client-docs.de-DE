---
title: Abschnitt "Geometrie"
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm2055
localization_priority: Normal
ms.assetid: 75601a1e-6b1a-27ee-a2bd-69e569315982
description: Enthält Zeilen, die die Koordinaten der Scheitelpunkte für die Linien und Bögen auflisten, aus denen das Shape besteht.
ms.openlocfilehash: 32a815015c7d1764399215767b674668b7235832
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423909"
---
# <a name="geometry-section"></a><span data-ttu-id="086f0-103">Abschnitt "Geometrie"</span><span class="sxs-lookup"><span data-stu-id="086f0-103">Geometry Section</span></span>

<span data-ttu-id="086f0-104">Enthält Zeilen, die die Koordinaten der Scheitelpunkte für die Linien und Bögen auflisten, aus denen das Shape besteht.</span><span class="sxs-lookup"><span data-stu-id="086f0-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="086f0-105">Die Geometrie einer Form kann in mehreren **Geometrie** Abschnitten ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="086f0-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="086f0-106">Mehrere Pfade können nützlich sein, wenn mehrere Pfade unterschiedliche Eigenschaften aufweisen (z. b. [Bild](clippingpath-cell-foreign-image-info-section.md) Beschneidungspfade).</span><span class="sxs-lookup"><span data-stu-id="086f0-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="086f0-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="086f0-107">Remarks</span></span>

<span data-ttu-id="086f0-108">Der Abschnitt **Geometry** enthält die folgenden Zeilentypen.</span><span class="sxs-lookup"><span data-stu-id="086f0-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="086f0-109">Weitere Details finden Sie unter den Zellenthemen.</span><span class="sxs-lookup"><span data-stu-id="086f0-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="086f0-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="086f0-110">**Row**</span></span>|<span data-ttu-id="086f0-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="086f0-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="086f0-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="086f0-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-113">Verschieben zu einer Koordinate.</span><span class="sxs-lookup"><span data-stu-id="086f0-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="086f0-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="086f0-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-115">Eine Linie bis zu einer Koordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="086f0-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="086f0-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="086f0-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-117">Einen kreisförmigen Bogen bis zu einer Koordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="086f0-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="086f0-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="086f0-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-119">Einen elliptischen Bogen bis zu einer Koordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="086f0-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="086f0-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="086f0-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-121">Eine Polylinie oder aufeinander folgende Linien bis zu einer Koordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="086f0-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="086f0-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="086f0-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-123">Zeichnen Sie einen nicht einheitlichen rationalen B-Spline (NURBS) zu einer Koordinate.</span><span class="sxs-lookup"><span data-stu-id="086f0-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="086f0-124">Zeile SplineStart</span><span class="sxs-lookup"><span data-stu-id="086f0-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-125">Ein Spline beginnen.</span><span class="sxs-lookup"><span data-stu-id="086f0-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="086f0-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="086f0-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-127">Ein Splinesegment bis zu einer Knotenkoordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="086f0-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="086f0-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="086f0-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-129">Eine unendliche Linie von einer Koordinate zu einer anderen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="086f0-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="086f0-130">Ellipse</span><span class="sxs-lookup"><span data-stu-id="086f0-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-131">Eine Ellipse von einer Mittelkoordinate und einer großen/kleinen Achse zeichnen.</span><span class="sxs-lookup"><span data-stu-id="086f0-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="086f0-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="086f0-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-133">Zeichnen Sie eine kubische Bézierkurve relativ zur Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="086f0-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="086f0-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="086f0-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-135">Zeichnen Sie einen elliptischen Bogen zu einer Koordinate relativ zur Höhe und Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="086f0-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="086f0-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="086f0-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-137">Ziehen Sie eine Koordinate zu einem Koordinaten relativ zur Höhe und Breite einer Form.</span><span class="sxs-lookup"><span data-stu-id="086f0-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="086f0-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="086f0-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-139">Wechseln Sie zu einer Koordinate relativ zur Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="086f0-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="086f0-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="086f0-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="086f0-141">Zeichnet eine quadratische Bézierkurve relativ zur Breite und Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="086f0-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="086f0-142">Wenn Sie einen Zeilentyp in diesem Abschnitt ändern möchten, klicken Sie mit der rechten Maustaste auf die Zeile, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**.</span><span class="sxs-lookup"><span data-stu-id="086f0-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

