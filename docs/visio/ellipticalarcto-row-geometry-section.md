---
title: Zeile "EllipticalArcTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm3015
localization_priority: Normal
ms.assetid: 7ceb30a8-1d05-feff-35d8-08a198784a27
description: Enthält X- und y-Koordinaten des eines elliptischen Bogens Endpunkt, X- und y-Koordinaten der Kontrollpunkte des Bogens, den Winkel von X-Achse zu großen Achse der Ellipse und das Verhältnis zwischen der Ellipse Haupt- und Hilfsintervalle Achsen.
ms.openlocfilehash: 9a356429f14a20b72a8bd55689855e2954d4a807
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796925"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="31e32-103">EllipticalArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="31e32-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="31e32-104">Enthält die *X* - und *y* - Koordinaten des Endpunkts eines elliptischen Bogens, *X* - und *y* -Koordinaten der Kontrollpunkte des Bogens, Winkel von der *x* -Achse zu großen Achse der Ellipse und das Verhältnis zwischen der Ellipse Haupt- und Mino R Achsen.</span><span class="sxs-lookup"><span data-stu-id="31e32-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="31e32-105">Eine Zeile EllipticalArcTo enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="31e32-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="31e32-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="31e32-106">**Cell**</span></span>|<span data-ttu-id="31e32-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31e32-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31e32-108">X</span><span class="sxs-lookup"><span data-stu-id="31e32-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="31e32-109">Die *X* -Koordinate des Endscheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="31e32-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="31e32-110">Y</span><span class="sxs-lookup"><span data-stu-id="31e32-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="31e32-111">Die *y* -Koordinate des Endscheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="31e32-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="31e32-112">A</span><span class="sxs-lookup"><span data-stu-id="31e32-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="31e32-113">Die *X* -Koordinate des Kontrollpunkts des Bogens; ein Punkt auf dem Bogen. Kontrollpunkts ist die beste in der Mitte zwischen dem ersten und letzten Scheitelpunkt des Bogens. Andernfalls kann Bogens extrem große anwachsen, um passieren Kontrollpunkts weitergibt.</span><span class="sxs-lookup"><span data-stu-id="31e32-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="31e32-114">B</span><span class="sxs-lookup"><span data-stu-id="31e32-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="31e32-115">Die *y* -Koordinate des Kontrollpunkts des Bogens.</span><span class="sxs-lookup"><span data-stu-id="31e32-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="31e32-116">C</span><span class="sxs-lookup"><span data-stu-id="31e32-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="31e32-117">Der Winkel der Größenachse des Bogens relativ zu der *X* -Achse des übergeordneten Objekts.</span><span class="sxs-lookup"><span data-stu-id="31e32-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="31e32-118">D</span><span class="sxs-lookup"><span data-stu-id="31e32-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="31e32-p101">Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="31e32-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

