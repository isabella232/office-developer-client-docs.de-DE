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
description: Enthält Zeilen, in denen die Koordinaten der Scheitelpunkte für die Linien und Bögen, die das Shape bilden aufgeführt.
ms.openlocfilehash: 59f85c512b7038f6cfddcb657435730a2e724bd6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797085"
---
# <a name="geometry-section"></a><span data-ttu-id="6ee2c-103">Geometry Section</span><span class="sxs-lookup"><span data-stu-id="6ee2c-103">Geometry Section</span></span>

<span data-ttu-id="6ee2c-104">Enthält Zeilen, in denen die Koordinaten der Scheitelpunkte für die Linien und Bögen, die das Shape bilden aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-104">Contains rows that list the coordinates of the vertices for the lines and arcs that make up the shape.</span></span> 
  
<span data-ttu-id="6ee2c-105">Die Geometrie eines Shapes kann in mehreren **geometrischen** Abschnitte ausgedrückt werden.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-105">The geometry of a shape can be expressed in multiple **Geometry** sections.</span></span> <span data-ttu-id="6ee2c-106">Mehrere Pfade können hilfreich sein, wenn mehrere Pfade über verschiedene Eigenschaften (z. B. [Bild Clipping](clippingpath-cell-foreign-image-info-section.md) Pfade) verfügen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-106">Multiple paths can be useful when multiple paths have different properties (e.g. [image clipping](clippingpath-cell-foreign-image-info-section.md) paths).</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6ee2c-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6ee2c-107">Remarks</span></span>

<span data-ttu-id="6ee2c-108">Der Abschnitt **"Geometry"** enthält die folgenden Zeilentypen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-108">The **Geometry** section contains the following row types.</span></span> <span data-ttu-id="6ee2c-109">Weitere Informationen hierzu finden Sie unter den Themen Zeile.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-109">For details, see the row topics.</span></span> 
  
|<span data-ttu-id="6ee2c-110">**Row**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-110">**Row**</span></span>|<span data-ttu-id="6ee2c-111">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ee2c-111">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ee2c-112">MoveTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-112">MoveTo</span></span>](moveto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-113">Verschieben zu einer Koordinate.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-113">Move to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-114">LineTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-114">LineTo</span></span>](lineto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-115">Eine Linie bis zu einer Koordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-115">Draw a line to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-116">ArcTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-116">ArcTo</span></span>](arcto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-117">Einen kreisförmigen Bogen bis zu einer Koordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-117">Draw a circular arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-118">EllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-118">EllipticalArcTo</span></span>](ellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-119">Einen elliptischen Bogen bis zu einer Koordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-119">Draw an elliptical arc to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-120">PolylineTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-120">PolylineTo</span></span>](polylineto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-121">Eine Polylinie oder aufeinander folgende Linien bis zu einer Koordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-121">Draw a polyline, or consecutive lines, to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-122">NURBSTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-122">NURBSTo</span></span>](nurbsto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-123">Zeichnen Sie ein nicht einheitlichen rationales B-Spline (NURBS) bis zu einer Koordinate.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-123">Draw a non-uniform rational B-spline (NURBS) to a coordinate.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-124">SplineStart</span><span class="sxs-lookup"><span data-stu-id="6ee2c-124">SplineStart</span></span>](splinestart-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-125">Ein Spline beginnen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-125">Start a spline.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-126">SplineKnot</span><span class="sxs-lookup"><span data-stu-id="6ee2c-126">SplineKnot</span></span>](splineknot-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-127">Ein Splinesegment bis zu einer Knotenkoordinate zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-127">Draw a spline segment to a knot coordinate.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-128">InfiniteLine</span><span class="sxs-lookup"><span data-stu-id="6ee2c-128">InfiniteLine</span></span>](infiniteline-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-129">Eine unendliche Linie von einer Koordinate zu einer anderen zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-129">Draw an infinite line from one coordinate to another.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-130">Ellipse</span><span class="sxs-lookup"><span data-stu-id="6ee2c-130">Ellipse</span></span>](ellipse-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-131">Eine Ellipse von einer Mittelkoordinate und einer großen/kleinen Achse zeichnen.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-131">Draw an ellipse from a center coordinate and a major/minor axis.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-132">RelCubBezTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-132">RelCubBezTo</span></span>](relcubbezto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-133">Zeichnen Sie eine kubische Bézierkurve relativ zu der Breite und Höhe des Shapes.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-133">Draw a cubic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-134">RelEllipticalArcTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-134">RelEllipticalArcTo</span></span>](relellipticalarcto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-135">Zeichnen Sie einen elliptischen Bogen bis zu einer Koordinate relativ zur Höhe und Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-135">Draw an elliptical arc to a coordinate relative to the height and width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-136">RelLineTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-136">RelLineTo</span></span>](rellineto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-137">Zeichnen Sie eine Linie einer relativen Koordinaten, die Höhe und Breite eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-137">Draw a line to a coordinate relative the height and width of a shape.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-138">RelMoveTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-138">RelMoveTo</span></span>](relmoveto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-139">Verschieben Sie zu einer Koordinate relativ zu der Breite und Höhe des Shapes.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-139">Move to a coordinate relative to the width and height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="6ee2c-140">RelQuadBezTo</span><span class="sxs-lookup"><span data-stu-id="6ee2c-140">RelQuadBezTo</span></span>](relquadbezto-row-geometry-section.md) <br/> |<span data-ttu-id="6ee2c-141">Zeichnet eine quadratische Bézierkurve relativ zu der Breite und Höhe des Shapes.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-141">Draws a quadratic Bezier curve relative to the width and height of the shape.</span></span>  <br/> |
   
<span data-ttu-id="6ee2c-142">Wenn Sie einen Zeilentyp in diesem Abschnitt ändern möchten, klicken Sie mit der rechten Maustaste auf die Zeile, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**.</span><span class="sxs-lookup"><span data-stu-id="6ee2c-142">To change a row type in this section, right-click the row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

