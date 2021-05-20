---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Enthält x- und y-Koordinaten des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite und Höhe eines Shapes.
ms.openlocfilehash: 2e85033b4a2e16c2df09b1a09655fcd4b97dd03d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33437161"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="e7d10-103">RelLineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="e7d10-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="e7d10-104">Enthält  *x-*  und  *y-Koordinaten*  des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite und Höhe eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="e7d10-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e7d10-105">Eine **RelLineTo-Zeile** kann nur in den Dateiformaten VSDX, VSDM, VSTX, VSTM, VSSX und VSSM beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="e7d10-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="e7d10-106">Wenn eine Datei in den Formaten Visio 2003-2010 gespeichert wird, wird die **Zeile RelLineTo** in eine [Zeile LineTo](lineto-row-geometry-section.md) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="e7d10-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="e7d10-107">Eine **RelLineTo-Zeile** enthält die folgenden Zellen.</span><span class="sxs-lookup"><span data-stu-id="e7d10-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="e7d10-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="e7d10-108">**Cell**</span></span>|<span data-ttu-id="e7d10-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e7d10-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e7d10-110">X</span><span class="sxs-lookup"><span data-stu-id="e7d10-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="e7d10-111">Die  x-Koordinate des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Breite des Shapes.</span><span class="sxs-lookup"><span data-stu-id="e7d10-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="e7d10-112">Y</span><span class="sxs-lookup"><span data-stu-id="e7d10-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="e7d10-113">Die  y-Koordinate des endenden Scheitelpunkts eines geraden Abschnitts relativ zur Höhe des Shapes.</span><span class="sxs-lookup"><span data-stu-id="e7d10-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e7d10-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e7d10-114">Remarks</span></span>

<span data-ttu-id="e7d10-115">Werte in der **Zeile RelLineTo** entsprechen Werten in einer [Zeile LineTo,](lineto-row-geometry-section.md) die mit der Breite und Höhe der Form multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="e7d10-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="e7d10-116">Beispiel: Eine **RelLineTo-Zeile,** in der der Wert der **Zelle X** "0" und der Wert der Zelle Y "0,5" ist, kann durch die Zeile **LineTo** ersetzt werden, wobei der Wert der Zelle **X** die Formel "Breite 0" und die *Zelle **Y*** die Formel "Höhe 0,5" ist. </span><span class="sxs-lookup"><span data-stu-id="e7d10-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width *0" and the **Y** cell is the formula "Height* 0.5."</span></span> 
  

