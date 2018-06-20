---
title: RelMoveTo Row (Geometry Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 04a0ba9f-48dd-488f-9c87-3890a12adf89
description: Enthält die X - und y - Koordinaten des ersten Scheitelpunkts eines Shapes oder die X- und y-Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad, relativ zur Höhe und Breite der Form.
ms.openlocfilehash: 77b3e731bfd1f35abe34ffbf3155b57133e56412
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797821"
---
# <a name="relmoveto-row-geometry-section"></a><span data-ttu-id="6ae94-103">RelMoveTo Row (Geometry Section)</span><span class="sxs-lookup"><span data-stu-id="6ae94-103">RelMoveTo Row (Geometry Section)</span></span>

<span data-ttu-id="6ae94-104">Enthält die *X* - und *y* - Koordinaten des ersten Scheitelpunkts eines Shapes oder die *X* - und *y* -Koordinaten des ersten Scheitelpunkts hinter einer Pfadlücke in einem Pfad, relativ zur Höhe und Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="6ae94-104">Contains the  *x*  - and  *y*  -coordinates of the first vertex of a shape or the  *x*  - and  *y*  -coordinates of the first vertex after a break in a path, relative to the height and width of the shape.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="6ae94-105">Eine Zeile **RelMoveTo** kann nur in den Dateiformaten .vsdx, .vsdm, .vstx, .vstm, .vssx und .vssm beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="6ae94-105">A **RelMoveTo** row can only be persisted in the .vsdx, .vsdm, .vstx, .vstm, .vssx, and .vssm file formats.</span></span> <span data-ttu-id="6ae94-106">Wenn eine Datei in das Visio 2003-2010-Formate gespeichert wird, wird die Zeile **RelMoveTo** in eine Zeile [MoveTo](moveto-row-geometry-section.md) konvertiert.</span><span class="sxs-lookup"><span data-stu-id="6ae94-106">When a file is saved to the Visio 2003-2010 formats, the **RelMoveTo** row is converted to a [MoveTo](moveto-row-geometry-section.md) row.</span></span> 
  
<span data-ttu-id="6ae94-107">Eine Zeile **RelMoveTo** enthält folgende Zellen.</span><span class="sxs-lookup"><span data-stu-id="6ae94-107">A **RelMoveTo** row contains the following cells.</span></span> 
  
|<span data-ttu-id="6ae94-108">**Cell**</span><span class="sxs-lookup"><span data-stu-id="6ae94-108">**Cell**</span></span>|<span data-ttu-id="6ae94-109">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6ae94-109">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="6ae94-110">X</span><span class="sxs-lookup"><span data-stu-id="6ae94-110">X</span></span>](x-cell-geometry-section.md) <br/> |<span data-ttu-id="6ae94-111">Wenn die **RelMoveTo** Zeile der ersten Zeile im Abschnitt ist, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts eines Shapes relativ zu der Breite der Form.</span><span class="sxs-lookup"><span data-stu-id="6ae94-111">If the **RelMoveTo** row is the first row in the section, the X cell represents the  *x*  -coordinate of the first vertex of a shape relative to the width of the shape.</span></span> <span data-ttu-id="6ae94-112">Wenn die Zeile **RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle X die *X* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.</span><span class="sxs-lookup"><span data-stu-id="6ae94-112">If the **RelMoveTo** row appears between two rows, the X cell represents the  *x*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
|[<span data-ttu-id="6ae94-113">Y</span><span class="sxs-lookup"><span data-stu-id="6ae94-113">Y</span></span>](y-cell-geometry-section.md) <br/> |<span data-ttu-id="6ae94-114">Wenn die **RelMoveTo** Zeile der ersten Zeile im Abschnitt ist, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts eines Shapes.</span><span class="sxs-lookup"><span data-stu-id="6ae94-114">If the **RelMoveTo** row is the first row in the section, the Y cell represents the  *y*  -coordinate of the first vertex of a shape.</span></span> <span data-ttu-id="6ae94-115">Wenn die Zeile **RelMoveTo** zwischen zwei Zeilen angezeigt wird, stellt die Zelle Y die *y* -Koordinate des ersten Scheitelpunkts hinter der Pfadlücke.</span><span class="sxs-lookup"><span data-stu-id="6ae94-115">If the **RelMoveTo** row appears between two rows, the Y cell represents the  *y*  -coordinate of the first vertex after the break in the path.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6ae94-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6ae94-116">Remarks</span></span>

<span data-ttu-id="6ae94-117">Werte in der Zeile **RelMoveTo** entsprechen Werten in einer Zeile [MoveTo](moveto-row-geometry-section.md) , die die Breite und Höhe des Shapes multipliziert werden.</span><span class="sxs-lookup"><span data-stu-id="6ae94-117">Values in the **RelMoveTo** row are equivalent to values in a [MoveTo](moveto-row-geometry-section.md) row that are multiplied by the width and height of the shape.</span></span> <span data-ttu-id="6ae94-118">Beispiel: eine Zeile **RelMoveTo** , in denen der Wert der Zelle **X** ist "0" und der Wert der Zelle **Y** ist "0,5" konnte mit **MoveTo** -Zeile, in dem der Wert der Zelle **X** die Formel lautet, ersetzt werden "Breite*0" und die Zelle **Y** ist die Formel "Höhe*0,5."</span><span class="sxs-lookup"><span data-stu-id="6ae94-118">For example: a **RelMoveTo** row where the value of the **X** cell is "0" and the value of the **Y** cell is "0.5" could be replaced with **MoveTo** row where the value of the **X** cell is the formula "Width*0" and the **Y** cell is the formula "Height*0.5."</span></span> 
  
<span data-ttu-id="6ae94-119">Die **RelMoveTo** Zeile enthält, die *X* - und *y* -Koordinaten des ersten Scheitelpunkts für das Shape, wenn die Zeile MoveTo die erste Zeile im Abschnitt ist.</span><span class="sxs-lookup"><span data-stu-id="6ae94-119">The **RelMoveTo** row contains the  *x*  - and  *y*  -coordinates of the first vertex for the shape if the MoveTo row is the first row in the section.</span></span> <span data-ttu-id="6ae94-120">In der Regel ist dies dem ersten Scheitelpunkt und es entspricht nicht notwendigerweise auf den Anfangspunkt eines 1D-Shapes Shapes beim Zeichnen des Shapes platziert.</span><span class="sxs-lookup"><span data-stu-id="6ae94-120">Usually this is the first vertex placed when the shape was drawn, and it does not necessarily correspond to the begin point of a 1-D shape.</span></span> 
  
<span data-ttu-id="6ae94-121">Ein Abschnitt **Geometry** muss mit einem **MoveTo** oder eine Zeile **RelMoveTo** beginnen, aber Sie können der **RelMoveTo** Zeile und die Zeile **MoveTo** auch verwenden, um eine Lücke im Verlauf des Pfads einer Form, relativ zur Breite und Höhe des Shapes darzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ae94-121">A **Geometry** section must begin with a **MoveTo** or a **RelMoveTo** row, but you can also use the **RelMoveTo** row and **MoveTo** row to represent a gap in the stroking of a shape's path relative to the shape's width and height.</span></span> <span data-ttu-id="6ae94-122">Wenn der Pfad verwendet wird, um die Grenze eines ausgefüllten Bereichs zu definieren, wird die Lücke als eines geraden Linienabschnitts interpretiert.</span><span class="sxs-lookup"><span data-stu-id="6ae94-122">However, when the path is used to define the boundary of a filled region, this gap is interpreted as a straight line segment.</span></span> <span data-ttu-id="6ae94-123">Um solche eine Lücke einfügen möchten, fügen Sie eine Zeile zwischen zwei Zeilen, und ändern Sie den Zeilentyp in **RelMoveTo**.</span><span class="sxs-lookup"><span data-stu-id="6ae94-123">To insert such a gap, insert a row between two rows and change the row type to **RelMoveTo**.</span></span> <span data-ttu-id="6ae94-124">Wenn die Zeile **RelMoveTo** zwischen zwei Zeilen befindet, enthält die *X* - und *y* -Koordinaten des ersten Scheitelpunkts des Linie nach der Unterbrechung im Pfad des Shapes.</span><span class="sxs-lookup"><span data-stu-id="6ae94-124">If the **RelMoveTo** row is between two rows, it contains the  *x*  - and  *y*  -coordinates of the first vertex of the line after the break in the shape's path.</span></span> 
  
