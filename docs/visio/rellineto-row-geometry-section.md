---
title: RelLineTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a900e174-d26a-4314-ae4f-d89e186350ce
description: Enthält x - und y-Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe des Shapes.
ms.openlocfilehash: 26cb63ac6cc0708be4e5668174022af63391c129
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797810"
---
# <a name="rellineto-row-geometry-section"></a><span data-ttu-id="a6b41-103">RelLineTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="a6b41-103">RelLineTo Row (Geometry Section)</span></span>

<span data-ttu-id="a6b41-104">Enthält die *X* - und *y* -Koordinaten des Endscheitelpunkts eines geraden Linienabschnitts relativ zur Breite und Höhe des Shapes.</span><span class="sxs-lookup"><span data-stu-id="a6b41-104">Contains  *x*  -and  *y*  -coordinates of the ending vertex of a straight line segment relative to a shape's width and height.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a6b41-105">Eine Zeile **RelLineTo** kann nur in den Dateiformaten .vsdx, .vsdm, .vstx, .vstm, .vssx und .vssm beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="a6b41-105">A **RelLineTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="a6b41-106">Wenn eine Datei in das Visio 2003-2010-Formate gespeichert wird, wird die Zeile **RelLineTo** in eine Zeile [LineTo](lineto-row-geometry-section.md) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="a6b41-106">When a file is saved to the Visio 2003-2010 formats, the **RelLineTo** row is converted to a [LineTo](lineto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="a6b41-107">Eine Zeile **RelLineTo** enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="a6b41-107">A **RelLineTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="a6b41-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="a6b41-108">**Cell**</span></span>|<span data-ttu-id="a6b41-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a6b41-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a6b41-110">X</span><span class="sxs-lookup"><span data-stu-id="a6b41-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="a6b41-111">Die *X* -Koordinate des Endscheitelpunkts eines geraden Linienabschnitts relativ zu der Breite des Shapes.</span><span class="sxs-lookup"><span data-stu-id="a6b41-111">The  *x*  -coordinate of the ending vertex of a straight line segment relative to the shape's width.</span></span>  <br/> |
|[<span data-ttu-id="a6b41-112">Y</span><span class="sxs-lookup"><span data-stu-id="a6b41-112">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="a6b41-113">Die *y* -Koordinate des Endscheitelpunkts eines geraden Linienabschnitts relativ zur Höhe des Shapes.</span><span class="sxs-lookup"><span data-stu-id="a6b41-113">The  *y*  -coordinate of the ending vertex of a straight line segment relative to the shape's height.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a6b41-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a6b41-114">Remarks</span></span>

<span data-ttu-id="a6b41-115">Werte in der Zeile **RelLineTo** entsprechen Werte in einer [LineTo](lineto-row-geometry-section.md) -Zeile, die die Breite und Höhe des Shapes multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="a6b41-115">Values in the **RelLineTo** row are equivalent to values in a [LineTo](lineto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="a6b41-116">Beispiel: eine Zeile **RelLineTo** , in denen der Wert der Zelle **X** ist "0" und der Wert der Zelle **Y** ist "0,5" kann mit der Zeile " **LineTo"** , in dem der Wert der Zelle **X** die Formel lautet, ersetzt werden "Breite*0" und die Zelle **Y** ist die Formel "Höhe*0,5."</span><span class="sxs-lookup"><span data-stu-id="a6b41-116">For example: a **RelLineTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" can be replaced with **LineTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  

