---
title: Zeile "MoveTo" (Abschnitt "Geometry")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm3030
localization_priority: Normal
ms.assetid: c5b20257-676c-279d-f730-1b6fbbe98305
description: Enthält die x-und y-Koordinaten des ersten Scheitelpunkts einer Form oder stellt die x-und y-Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar.
ms.openlocfilehash: fc414093348b8da04fa3503053584395976982dd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283858"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="73881-103">Zeile "MoveTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="73881-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="73881-104">Enthält die *x* -und *y* -Koordinaten des ersten Scheitelpunkts einer Form oder stellt die *x* -und *y* -Koordinaten des ersten Scheitelpunkts nach einer Unterbrechung in einem Pfad dar.</span><span class="sxs-lookup"><span data-stu-id="73881-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="73881-105">Eine **MoveTo** -Zeile enthält die folgenden Zellen.</span><span class="sxs-lookup"><span data-stu-id="73881-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="73881-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="73881-106">**Cell**</span></span>|<span data-ttu-id="73881-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73881-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73881-108">X</span><span class="sxs-lookup"><span data-stu-id="73881-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="73881-109">Wenn die **MoveTo** -Zeile die erste Zeile im Abschnitt ist, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts einer Form dar.</span><span class="sxs-lookup"><span data-stu-id="73881-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="73881-110">Wenn die **MoveTo** -Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle x die *x* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.</span><span class="sxs-lookup"><span data-stu-id="73881-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="73881-111">Y</span><span class="sxs-lookup"><span data-stu-id="73881-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="73881-112">Wenn die **MoveTo** -Zeile die erste Zeile im Abschnitt ist, stellt die Zelle y die *y* -Koordinate des ersten Scheitelpunkts einer Form dar.</span><span class="sxs-lookup"><span data-stu-id="73881-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="73881-113">Wenn die **MoveTo** -Zeile zwischen zwei Zeilen angezeigt wird, stellt die Zelle y die *y* -Koordinate des ersten Scheitelpunkts nach der Unterbrechung im Pfad dar.</span><span class="sxs-lookup"><span data-stu-id="73881-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="73881-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73881-114">Remarks</span></span>

<span data-ttu-id="73881-115">Die Zeile **MoveTo** enthält die *x* -und *y* -Koordinaten des ersten Scheitelpunkts für das Shape, wenn die **MoveTo** -Zeile die erste Zeile im Abschnitt ist.</span><span class="sxs-lookup"><span data-stu-id="73881-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="73881-116">In der Regel ist dies der erste Scheitelpunkt, der beim Zeichnen des Shapes festgelegt wurde, und es entspricht nicht unbedingt dem Anfangszeitpunkt eines 1D-Shapes.</span><span class="sxs-lookup"><span data-stu-id="73881-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="73881-117">Ein Geometry-Abschnitt muss entweder mit einer **RelMoveTo** -oder einer **MoveTo** -Zeile beginnen, aber Sie können auch die **MoveTo** -und **RelMoveTo** -Zeilen verwenden, um eine Lücke beim streicheln des Pfads einer Form darzustellen.</span><span class="sxs-lookup"><span data-stu-id="73881-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="73881-118">Wenn jedoch der Pfad verwendet wird, um die Grenze eines ausgefüllten Bereichs zu definieren, wird dieser Abstand als gerade Linie interpretiert.</span><span class="sxs-lookup"><span data-stu-id="73881-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="73881-119">Um eine solche Lücke einzufügen, fügen Sie eine Zeile zwischen zwei Zeilen ein, und ändern Sie den Zeilentyp in **MoveTo**.</span><span class="sxs-lookup"><span data-stu-id="73881-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="73881-120">Wenn sich die **MoveTo** -Zeile zwischen zwei Zeilen befindet, enthält Sie die *x* -und *y* -Koordinaten des ersten Scheitelpunkts der Linie nach der Unterbrechung im Pfad des Shapes.</span><span class="sxs-lookup"><span data-stu-id="73881-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

