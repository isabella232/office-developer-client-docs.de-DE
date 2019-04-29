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
description: Enthält die x-und y-Koordinaten des Endpunkts eines elliptischen Bogens, die x-und y-Koordinaten der Steuerpunkte des Bogens, den Winkel von der x-Achse zur Hauptachse der Ellipse und das Verhältnis zwischen Haupt-und Nebenachsen der Ellipse.
ms.openlocfilehash: c6db7560a05652ca3bfcadb2fd4857ac39370562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421403"
---
# <a name="ellipticalarcto-row-geometry-section"></a><span data-ttu-id="5c57c-103">Zeile "EllipticalArcTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="5c57c-103">EllipticalArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="5c57c-104">Enthält die *x* -und *y* -Koordinaten des Endpunkts eines elliptischen Bogens, die *x* -und *y* -Koordinaten der Kontrollpunkte des Bogens, den Winkel von der *x* -Achse zur Hauptachse der Ellipse und das Verhältnis zwischen dem großen und dem Mino r-Achsen.</span><span class="sxs-lookup"><span data-stu-id="5c57c-104">Contains  *x*  - and  *y*  -coordinates of an elliptical arc's endpoint,  *x*  - and  *y*  -coordinates of the control points on the arc, angle from the  *x*  -axis to the ellipse's major axis, and ratio between the ellipse's major and minor axes.</span></span> 
  
<span data-ttu-id="5c57c-105">Eine Zeile EllipticalArcTo enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="5c57c-105">An EllipticalArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="5c57c-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="5c57c-106">**Cell**</span></span>|<span data-ttu-id="5c57c-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5c57c-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5c57c-108">X</span><span class="sxs-lookup"><span data-stu-id="5c57c-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="5c57c-109">Die *x* -Koordinate des Endpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="5c57c-109">The  *x*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="5c57c-110">Y</span><span class="sxs-lookup"><span data-stu-id="5c57c-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="5c57c-111">Die *y* -Koordinate des Endpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="5c57c-111">The  *y*  -coordinate of the ending vertex on an arc.</span></span>  <br/> |
|[<span data-ttu-id="5c57c-112">A</span><span class="sxs-lookup"><span data-stu-id="5c57c-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="5c57c-113">Die *x* -Koordinate des Kontrollpunkts des Bogens; ein Punkt auf dem Bogen. Der Steuerpunkt befindet sich am besten in der Mitte zwischen dem Anfangs-und Endscheitel des Bogens. Andernfalls kann der Bogen zu einer extremen Größe anwachsen, um den Kontrollpunkt mit unvorhersehbaren Ergebnissen zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5c57c-113">The  *x*  -coordinate of the arc's control point; a point on the arc. The control point is best located about halfway between the beginning and ending vertices of the arc. Otherwise, the arc may grow to an extreme size in order to pass through the control point, with unpredictable results.</span></span>  <br/> |
|[<span data-ttu-id="5c57c-114">B</span><span class="sxs-lookup"><span data-stu-id="5c57c-114">B</span></span>](b-cell-geometry-section.md) <br/> |<span data-ttu-id="5c57c-115">Die *y* -Koordinate des Kontrollpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="5c57c-115">The  *y*  -coordinate of an arc's control point.</span></span>  <br/> |
|[<span data-ttu-id="5c57c-116">C</span><span class="sxs-lookup"><span data-stu-id="5c57c-116">C</span></span>](c-cell-geometry-section.md) <br/> |<span data-ttu-id="5c57c-117">Der Winkel der Hauptachse eines Bogens relativ zur *x* -Achse des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="5c57c-117">The angle of an arc's major axis relative to the  *x*  -axis of its parent.</span></span>  <br/> |
|[<span data-ttu-id="5c57c-118">D</span><span class="sxs-lookup"><span data-stu-id="5c57c-118">D</span></span>](d-cell-geometry-section.md) <br/> |<span data-ttu-id="5c57c-p101">Das Verhältnis der größeren zur kleineren Achse eines Bogens. Im Gegensatz zu der normalen Bedeutung der Bezeichnungen muss die als "große" Achse bezeichnete Achse nicht unbedingt größer als die "kleine" Achse sein, sodass das Größenverhältnis nicht größer als 1 sein muss. Beim Festlegen des Zellwerts gleich 0 bzw. größer als 1000 können unvorhergesehene Ergebnisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="5c57c-p101">The ratio of an arc's major axis to its minor axis. Despite the usual meaning of these words, the "major" axis does not have to be greater than the "minor" axis, so this ratio does not have to be greater than 1. Setting this cell to a value less than or equal to 0 or greater than 1000 can lead to unpredictable results.</span></span>  <br/> |
   

