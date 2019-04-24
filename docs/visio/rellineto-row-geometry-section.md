---
title: Zeile "RelLineTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Enthält die x-und y-Koordinaten des Endpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe eines Shapes.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320069"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="867d0-103">Zeile "RelLineTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="867d0-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="867d0-104">Enthält die *x* -und *y* -Koordinaten des Endpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="867d0-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="867d0-105">Eine **RelLineTo** -Zeile kann nur im. vsdx-, vsdm-, vstx-, VSTM-, vssx-und VSSM-Dateiformat gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="867d0-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="867d0-106">Wenn eine Datei im Visio 2003-2010-Format gespeichert wird, wird die **RelLineTo** -Zeile in eine [LineTo](lineto-row-geometry-section.md) -Zeile konvertiert.</span><span class="sxs-lookup"><span data-stu-id="867d0-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="867d0-107">Eine **RelLineTo** -Zeile enthält die folgenden Zellen.</span><span class="sxs-lookup"><span data-stu-id="867d0-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="867d0-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="867d0-108">**Cell**</span></span>|<span data-ttu-id="867d0-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="867d0-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="867d0-110">X</span><span class="sxs-lookup"><span data-stu-id="867d0-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="867d0-111">Die *x* -Koordinate des Endpunkts eines geraden Linienabschnitts relativ zur Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="867d0-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="867d0-112">Y</span><span class="sxs-lookup"><span data-stu-id="867d0-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="867d0-113">Die *y* -Koordinate des Endpunkts eines geraden Linienabschnitts relativ zur Höhe der Form.</span><span class="sxs-lookup"><span data-stu-id="867d0-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="867d0-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="867d0-114">Remarks</span></span>

<span data-ttu-id="867d0-115">Werte in der **RelLineTo** -Zeile sind äquivalent zu Werten in einer [LineTo](lineto-row-geometry-section.md) -Zeile, die mit der Breite und Höhe der Form multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="867d0-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="867d0-116">Beispiel: eine **RelLineTo** Zeile, bei der der Wert der Zelle **x** "0" ist und der Wert der Zelle **y** "0,5" ist, kann durch **LineTo** Zeile ersetzt werden, wobei der Wert der Zelle **x** die Formel "Breite*0" ist und die **y** -Zelle die Formel "Height*0,5."</span><span class="sxs-lookup"><span data-stu-id="867d0-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

