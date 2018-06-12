---
title: Zeile "ArcTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82253229
localization_priority: Normal
ms.assetid: 612b605d-a703-b08f-2e8e-7bc1624b5370
description: Enthält die X- und y-Koordinaten und die Krümmung eines kreisförmigen Bogens.
ms.openlocfilehash: 77ed0dcaee7ddefa8771d3e890776d4adfcc3b40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796405"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="69df5-103">ArcTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="69df5-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="69df5-104">Enthält die *X* - und *y* -Koordinaten und die Krümmung eines kreisförmigen Bogens.</span><span class="sxs-lookup"><span data-stu-id="69df5-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="69df5-105">Eine Zeile ArcTo enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="69df5-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="69df5-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="69df5-106">**Cell**</span></span>|<span data-ttu-id="69df5-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69df5-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69df5-108">X</span><span class="sxs-lookup"><span data-stu-id="69df5-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="69df5-109">Die *X* -Koordinate des Endscheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="69df5-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="69df5-110">Y</span><span class="sxs-lookup"><span data-stu-id="69df5-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="69df5-111">Die *y* -Koordinate des Endscheitelpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="69df5-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="69df5-112">A</span><span class="sxs-lookup"><span data-stu-id="69df5-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="69df5-113">Die Entfernung zwischen dem Mittelpunkt des Bogens und dem Mittelpunkt seiner Sehne.</span><span class="sxs-lookup"><span data-stu-id="69df5-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="69df5-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="69df5-114">Remarks</span></span>

<span data-ttu-id="69df5-p101">In Visio gezeichnete Bögen sind elliptisch, auch wenn sie auf einem Kreis basieren. Standardmäßig werden gezeichnete Bögen durch eine Zeile EllipticalArcTo in einem ShapeSheet-Fenster dargestellt. Wenn Sie eine Zeile ArcTo in einem ShapeSheet-Fenster anzeigen möchten, müssen Sie einen Bogen zeichnen und dann den Zeilentyp EllipticalArcTo in den Zeilentyp ArcTo ändern, wodurch Sie einen elliptischen Bogen letztendlich in einen kreisförmigen Bogen ändern.</span><span class="sxs-lookup"><span data-stu-id="69df5-p101">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window. To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="69df5-118">Um den Zeilentyp zu ändern, mit der rechten Maustaste in einer Zeile, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern** .</span><span class="sxs-lookup"><span data-stu-id="69df5-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

