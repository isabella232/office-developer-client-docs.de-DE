---
title: Zelle "SketchFillChange" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 939f8f90-dee5-4175-b32a-e2964eb40681
description: Bestimmt den Umfang der Randomisierung der Füllung der Form aus der Geometrie der Form, wenn ein Skizzierungseffekt als Prozentsatz der Länge eines Abschnitts verwendet wird. Wenn der Wert der Zelle SketchFillChange auf 0 % festgelegt ist, entspricht die umgebende Geometrie der Füllung eines Shapes der Geometrie der Form. Wenn der Wert 100 % beträgt, folgt die umgebende Geometrie der Füllung des Shapes nicht der Geometrie der Form.
ms.openlocfilehash: 8726e9dd6ca6257fb8dbbbef3dce1d4ec344e28b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408075"
---
# <a name="sketchfillchange-cell-additional-effect-properties-section"></a><span data-ttu-id="0ed64-105">Zelle "SketchFillChange" (Abschnitt "Additional Effect Properties")</span><span class="sxs-lookup"><span data-stu-id="0ed64-105">SketchFillChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="0ed64-106">Bestimmt den Umfang der Randomisierung der Füllung der Form aus der Geometrie der Form, wenn ein Skizzierungseffekt als Prozentsatz der Länge eines Abschnitts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="0ed64-106">Determines the amount of randomization of the shape's fill from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="0ed64-107">Wenn der Wert der **Zelle SketchFillChange** auf 0 % festgelegt ist, entspricht die umgebende Geometrie der Füllung eines Shapes der Geometrie der Form.</span><span class="sxs-lookup"><span data-stu-id="0ed64-107">If the value of the **SketchFillChange** cell is set to 0%, the bounding geometry of a shape's fill matches the shape's geometry.</span></span> <span data-ttu-id="0ed64-108">Wenn der Wert 100 % beträgt, folgt die umgebende Geometrie der Füllung des Shapes nicht der Geometrie der Form.</span><span class="sxs-lookup"><span data-stu-id="0ed64-108">If the value is 100%, the bounding geometry of the shape's fill does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="0ed64-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0ed64-109">Remarks</span></span>

<span data-ttu-id="0ed64-110">Für optimale Ergebnisse liegt der ideale Wertebereich für die **Zelle SketchFillChange** zwischen 15 % und 50 %.</span><span class="sxs-lookup"><span data-stu-id="0ed64-110">For best results, the ideal range of values for the **SketchFillChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="0ed64-111">Ein Wert unter 15 % ist kaum wahrnehmbar. Ein Wert größer als 50 % wird zunehmend randomisiert.</span><span class="sxs-lookup"><span data-stu-id="0ed64-111">A value below 15% is barely noticeable; a value greater than 50% is increasingly more randomized.</span></span> 
  
<span data-ttu-id="0ed64-112">Um einen Verweis auf die **Zelle SketchFillChange** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="0ed64-112">To get a reference to the **SketchFillChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ed64-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="0ed64-113">Cell name:</span></span>  <br/> | <span data-ttu-id="0ed64-114">SketchFillChange</span><span class="sxs-lookup"><span data-stu-id="0ed64-114">SketchFillChange</span></span>  <br/> |
   
<span data-ttu-id="0ed64-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle SketchFillChange** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="0ed64-115">To get a reference to the **SketchFillChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="0ed64-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="0ed64-116">Section index:</span></span>  <br/> |<span data-ttu-id="0ed64-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="0ed64-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="0ed64-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="0ed64-118">Row index:</span></span>  <br/> |<span data-ttu-id="0ed64-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="0ed64-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="0ed64-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="0ed64-120">Cell index:</span></span>  <br/> |<span data-ttu-id="0ed64-121">**visSketchFillChange**</span><span class="sxs-lookup"><span data-stu-id="0ed64-121">**visSketchFillChange**</span></span> <br/> |
   

