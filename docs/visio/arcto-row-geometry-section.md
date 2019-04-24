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
description: Enthält die x-und y-Koordinaten und den Bogen eines kreisförmigen Bogens.
ms.openlocfilehash: 222edea250be794adc964345384f2c08a7798f2f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341405"
---
# <a name="arcto-row-geometry-section"></a><span data-ttu-id="28b87-103">Zeile "ArcTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="28b87-103">ArcTo Row (Geometry Section)</span></span>

<span data-ttu-id="28b87-104">Enthält die *x* -und *y* -Koordinaten und den Bogen eines kreisförmigen Bogens.</span><span class="sxs-lookup"><span data-stu-id="28b87-104">Contains the  *x*  - and  *y*  -coordinates and bow of a circular arc.</span></span> 
  
<span data-ttu-id="28b87-105">Eine Zeile ArcTo enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="28b87-105">An ArcTo row contains the following cells.</span></span>
  
|<span data-ttu-id="28b87-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="28b87-106">**Cell**</span></span>|<span data-ttu-id="28b87-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28b87-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28b87-108">X</span><span class="sxs-lookup"><span data-stu-id="28b87-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="28b87-109">Die *x* -Koordinate des Endpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="28b87-109">The  *x*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="28b87-110">Y</span><span class="sxs-lookup"><span data-stu-id="28b87-110">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="28b87-111">Die *y* -Koordinate des Endpunkts eines Bogens.</span><span class="sxs-lookup"><span data-stu-id="28b87-111">The  *y*  -coordinate of the ending vertex of an arc.</span></span>  <br/> |
|[<span data-ttu-id="28b87-112">A</span><span class="sxs-lookup"><span data-stu-id="28b87-112">A</span></span>](a-cell-geometry-section.md) <br/> |<span data-ttu-id="28b87-113">Die Entfernung zwischen dem Mittelpunkt des Bogens und dem Mittelpunkt seiner Sehne.</span><span class="sxs-lookup"><span data-stu-id="28b87-113">The distance from the arc's midpoint to the midpoint of its chord.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="28b87-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="28b87-114">Remarks</span></span>

<span data-ttu-id="28b87-p101">In Visio gezeichnete Bögen sind elliptisch, auch wenn sie auf einem Kreis basieren. Standardmäßig werden gezeichnete Bögen durch eine Zeile EllipticalArcTo in einem ShapeSheet-Fenster dargestellt. Wenn Sie eine Zeile ArcTo in einem ShapeSheet-Fenster anzeigen möchten, müssen Sie einen Bogen zeichnen und dann den Zeilentyp EllipticalArcTo in den Zeilentyp ArcTo ändern, wodurch Sie einen elliptischen Bogen letztendlich in einen kreisförmigen Bogen ändern.</span><span class="sxs-lookup"><span data-stu-id="28b87-p101">Arcs drawn in Visio are elliptical arcs, even if they are based on a circle. By default, drawn arcs are represented by an EllipticalArcTo row in a ShapeSheet window. To show an ArcTo row in a ShapeSheet window, you must draw an arc, and then change the EllipticalArcTo row type to an ArcTo row type; in effect you are changing an elliptical arc to a circular arc.</span></span>
  
<span data-ttu-id="28b87-118">Klicken Sie mit der rechten Maustaste auf eine Zeile, um den Zeilentyp zu ändern, und klicken Sie dann im Kontextmenü auf **Zeilentyp ändern**.</span><span class="sxs-lookup"><span data-stu-id="28b87-118">To change a row type, right-click a row, and then click **Change Row Type** on the shortcut menu.</span></span> 
  

