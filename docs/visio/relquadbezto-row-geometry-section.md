---
title: RelQuadBezTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5ae57707-5a50-43f0-8c78-516790b5034e
description: Enthält die x- und y-Koordinaten des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe der Form sowie die x- und y-Koordinaten des Kontrollpunkts der Breite und Höhe der Kurve relativer Form.
ms.openlocfilehash: f517fa006c6630a26e9162adfbb1be2139487e63
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423356"
---
# <a name="relquadbezto-row-geometry-section"></a><span data-ttu-id="c1c03-103">RelQuadBezTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="c1c03-103">RelQuadBezTo Row (Geometry Section)</span></span>

<span data-ttu-id="c1c03-104">Enthält die  *x-*  und  *y-Koordinaten*  des Endpunkts einer quadratischen Bézierkurve relativ zur Breite und Höhe der Form sowie die  *x-*  und  *y-Koordinaten*  des Kontrollpunkts der Breite und Höhe der Kurve relativer Form.</span><span class="sxs-lookup"><span data-stu-id="c1c03-104">Contains the  *x*  - and  *y*  -coordinates of the endpoint of a quadratic Bézier curve relative to the shape's width and height and the  *x*  - and  *y*  -coordinates of the control point of the curve relative shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="c1c03-105">Eine **RelQuadBezTo-Zeile** kann nur in den Dateiformaten VSDX, VSDM, VSTX, VSTM, VSSX und VSSM beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="c1c03-105">A **RelQuadBezTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="c1c03-106">Wenn eine Datei in den Formaten Visio 2003-2010 gespeichert wird, wird die **Zeile RelQuadBezTo** in eine [NURBSTo-Zeile](nurbsto-row-geometry-section.md) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="c1c03-106">When a file is saved to the Visio 2003-2010 formats, the **RelQuadBezTo** row is converted to a [NURBSTo](nurbsto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="c1c03-107">Eine **RelQuadBezTo-Zeile** enthält die folgenden Zellen.</span><span class="sxs-lookup"><span data-stu-id="c1c03-107">A **RelQuadBezTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="c1c03-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="c1c03-108">**Cell**</span></span>|<span data-ttu-id="c1c03-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1c03-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c1c03-110">X</span><span class="sxs-lookup"><span data-stu-id="c1c03-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="c1c03-111">Die  x-Koordinate des endenden Scheitelpunkts einer quadratischen Bézierkurve relativ zur Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="c1c03-111">The  *x*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the width of the shape.</span></span>  <br/> |
|[<span data-ttu-id="c1c03-112">Y</span><span class="sxs-lookup"><span data-stu-id="c1c03-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="c1c03-113">Die  y-Koordinate des endenden Scheitelpunkts einer quadratischen Bézierkurve relativ zur Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="c1c03-113">The  *y*  -coordinate of the ending vertex of a quadratic Bézier curve relative to the height of the shape.</span></span>  <br/> |
|[<span data-ttu-id="c1c03-114">A</span><span class="sxs-lookup"><span data-stu-id="c1c03-114">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="c1c03-115">Die  x-Koordinate des Kontrollpunkts der Kurve relativ zur Breite der Form; einen Punkt im Bogen. Der Kontrollpunkt befindet sich am besten ungefähr auf halbem Weg zwischen den Scheitelpunkte am Anfang und Ende des Bogens.</span><span class="sxs-lookup"><span data-stu-id="c1c03-115">The  *x*  -coordinate of the curve's control point relative to the shape's width; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc.</span></span>  <br/> |
|[<span data-ttu-id="c1c03-116">B</span><span class="sxs-lookup"><span data-stu-id="c1c03-116">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="c1c03-117">Die  y-Koordinate des Kontrollpunkts einer Kurve relativ zur Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="c1c03-117">The  *y*  -coordinate of a curve's control point relative to the shape's height.</span></span>  <br/> |
   

