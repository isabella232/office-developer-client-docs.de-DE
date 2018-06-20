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
description: Enthält die X- und y - Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die X - und y-Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad.
ms.openlocfilehash: cee62701074269350ae52c6fa7f7aee5cb612f49
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797532"
---
# <a name="moveto-row-geometry-section"></a><span data-ttu-id="bf8ce-103">Zeile "MoveTo" (Abschnitt "Geometry")</span><span class="sxs-lookup"><span data-stu-id="bf8ce-103">MoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="bf8ce-104">Enthält die *X* - und *y* - Koordinaten des ersten Scheitelpunkts eines Shapes oder stellt die *X* - und *y* -Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape, or represents the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path.</span></span> 
  
<span data-ttu-id="bf8ce-105">Eine Zeile **MoveTo** enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-105">A **MoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="bf8ce-106">**Cell**</span><span class="sxs-lookup"><span data-stu-id="bf8ce-106">**Cell**</span></span>|<span data-ttu-id="bf8ce-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bf8ce-107">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="bf8ce-108">X</span><span class="sxs-lookup"><span data-stu-id="bf8ce-108">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="bf8ce-109">Wenn die Zeile **MoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-109">If the **MoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="bf8ce-110">Wenn die Zeile **MoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-110">If the **MoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="bf8ce-111">Y</span><span class="sxs-lookup"><span data-stu-id="bf8ce-111">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="bf8ce-112">Wenn die Zeile **MoveTo** die erste Zeile im Abschnitt ist, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-112">If the **MoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="bf8ce-113">Wenn die Zeile **MoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-113">If the **MoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf8ce-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="bf8ce-114">Remarks</span></span>

<span data-ttu-id="bf8ce-115">Die Zeile **MoveTo** enthält die *X* - und *y* -Koordinaten des ersten Scheitelpunkts für das Shape, wenn die Zeile **MoveTo** die erste Zeile im Abschnitt ist.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-115">The **MoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the **MoveTo** row is the first row in the section.</span></span> <span data-ttu-id="bf8ce-116">In der Regel ist dies dem ersten Scheitelpunkt und es entspricht nicht notwendigerweise auf den Anfangspunkt eines 1D-Shapes Shapes beim Zeichnen des Shapes platziert.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-116">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="bf8ce-117">Ein Geometrieabschnitt muss mit einem **RelMoveTo** oder eine Zeile **MoveTo** beginnen, aber Sie können auch die Zeilen **MoveTo** und **RelMoveTo** verwenden, um eine Lücke im Verlauf des Shape Pfades darzustellen.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-117">A geometry section must begin with either a **RelMoveTo** or a **MoveTo** row, but you can also use the **MoveTo** and **RelMoveTo** rows to represent a gap in the stroking of a shape's path.</span></span> <span data-ttu-id="bf8ce-118">Wenn der Pfad verwendet wird, um die Grenze eines ausgefüllten Bereichs zu definieren, wird die Lücke als eines geraden Linienabschnitts interpretiert.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-118">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="bf8ce-119">Um solche eine Lücke einfügen möchten, fügen Sie eine Zeile zwischen zwei Zeilen, und ändern Sie den Zeilentyp in **MoveTo**.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-119">To insert such a gap, insert a row between two rows and change the row type to **MoveTo**.</span></span> <span data-ttu-id="bf8ce-120">Wenn die Zeile **MoveTo** zwischen zwei Zeilen befindet, enthält die *X* - und *y* -Koordinaten des ersten Scheitelpunkts des Linie nach der Unterbrechung im Pfad des Shapes.</span><span class="sxs-lookup"><span data-stu-id="bf8ce-120">If the **MoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  

