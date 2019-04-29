---
title: Zeile "RelCubBezTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 77777dd4-5a2c-4048-9ea4-9bd876862963
description: Enthält die x-und y-Koordinaten des Endpunkts einer kubischen Bézier-Kurve im Verhältnis zur Breite und Höhe der Form, die x-und y-Koordinaten des Steuerelements am Anfang der Breite und Höhe des Kurven relativen Shapes sowie die x-und y-Koordinaten des contro l Punkt des Endes der Breite und Höhe der Kurven relativen Form.
ms.openlocfilehash: cb886706c4c5cbb3488a95b57dcc84e0e45ee326
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430329"
---
# <a name="relcubbezto-row-geometry-section"></a><span data-ttu-id="bb3ce-103">Zeile "RelCubBezTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="bb3ce-103">RelCubBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="bb3ce-104">Enthält die *x* -und *y* -Koordinaten des Endpunkts einer kubischen Bézier-Kurve im Verhältnis zur Breite und Höhe der Form, die *x* -und *y* -Koordinaten des Steuerelements am Anfang der Breite und Höhe des Kurven relativen Shapes. und die *x* -und *y* -Koordinate des Kontrollpunkts des Endes der Breite und Höhe der Kurven relativen Form.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a cubic Bézier curve relative to the shape's width and height, the  *x*  - and  *y*  -coordinates of the control point of the beginning of the curve relative shape's width and height, and the  *x*  - and  *y*  -coordinates of the control point of the ending of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="bb3ce-105">Eine **RelCubBezTo** -Zeile kann nur im. vsdx-, vsdm-, vstx-, VSTM-, vssx-und VSSM-Dateiformat gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-105">A **RelCubBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="bb3ce-106">Wenn eine Datei im Visio 2003-2010-Format gespeichert wird, wird die **RelCubBezTo** -Zeile in eine [NURBSTo](nurbsto-row-geometry-section.md) -Zeile konvertiert.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-106">When a file is saved to the Visio 2003-2010 formats, the **RelCubBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="bb3ce-107">Eine **RelCubBezTo** -Zeile enthält die folgenden Zellen.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-107">A **RelCubBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="bb3ce-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="bb3ce-108">**Cell**</span></span>|<span data-ttu-id="bb3ce-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bb3ce-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bb3ce-110">X</span><span class="sxs-lookup"><span data-stu-id="bb3ce-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="bb3ce-111">Die *x* -Koordinate des Endpunkts einer kubischen Bézier-Kurve relativ zur Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-111">The  *x*  -coordinate of the ending vertex of a cubic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="bb3ce-112">Y</span><span class="sxs-lookup"><span data-stu-id="bb3ce-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="bb3ce-113">Die *y* -Koordinate des Endpunkts einer kubischen Bézier-Kurve relativ zur Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-113">The  *y*  -coordinate of the ending vertex of a cubic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="bb3ce-114">A</span><span class="sxs-lookup"><span data-stu-id="bb3ce-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="bb3ce-115">Die *x* -Koordinate des Anfangs Kontrollpunkts der Kurve relativ zur Breite der Form; ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten zwischen dem Anfangs-und Endscheitel des Bogens.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-115">The  *x*  -coordinate of the curve's beginning control point relative to the shape's width; a point on the arc. The control point is best located between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="bb3ce-116">B</span><span class="sxs-lookup"><span data-stu-id="bb3ce-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="bb3ce-117">Die *y* -Koordinate des Anfangs Steuerpunkts einer Kurve relativ zur Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-117">The  *y*  -coordinate of a curve's beginning control point relative to the shape's height.</span></span>  <br/> |
|[<span data-ttu-id="bb3ce-118">C</span><span class="sxs-lookup"><span data-stu-id="bb3ce-118">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="bb3ce-119">Die *x* -Koordinate des Endpunkts der Kurve, relativ zur Breite der Form; ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten zwischen dem Anfangs Steuerpunkt und den Endknoten des Bogens.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-119">The  *x*  -coordinate of the curve's ending control point relative to the shape's width; a point on the arc. The control point is best located between the beginning control point and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="bb3ce-120">D</span><span class="sxs-lookup"><span data-stu-id="bb3ce-120">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="bb3ce-121">Die *y* -Koordinate des Endpunkts eines Bogens relativ zur Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="bb3ce-121">The  *y*  -coordinate of a curve's ending control point relative to the shape's height.</span></span>  <br/> |
   

