---
title: Zelle "SketchLineChange" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 39192535-b55b-4c49-b63f-edb542c7a2e5
description: Bestimmt den Umfang der Randomisierung der Linie der Form aus der Geometrie des Shapes, wenn ein Skizzierungseffekt als Prozentsatz der Länge eines Abschnitts verwendet wird. Wenn der Wert der Zelle SketchLineChange auf 0 % festgelegt ist, entspricht die Geometrie der Linie des Shapes der Geometrie des Shapes. Wenn der Wert 100 % beträgt, folgt die Geometrie der Linie des Shapes nicht der Geometrie der Form.
ms.openlocfilehash: ba57a4d2e43a91475f4c3ab4862f723eb2653a89
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419506"
---
# <a name="sketchlinechange-cell-additional-effect-properties-section"></a><span data-ttu-id="09b5e-105">Zelle "SketchLineChange" (Abschnitt "Additional Effect Properties")</span><span class="sxs-lookup"><span data-stu-id="09b5e-105">SketchLineChange Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="09b5e-106">Bestimmt den Umfang der Randomisierung der Linie der Form aus der Geometrie des Shapes, wenn ein Skizzierungseffekt als Prozentsatz der Länge eines Abschnitts verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09b5e-106">Determines the amount of randomization of the shape's line from the shape's geometry when using a sketch effect, as a percentage of the length of a section.</span></span> <span data-ttu-id="09b5e-107">Wenn der Wert der **Zelle SketchLineChange** auf 0 % festgelegt ist, entspricht die Geometrie der Linie des Shapes der Geometrie des Shapes.</span><span class="sxs-lookup"><span data-stu-id="09b5e-107">If the value of the **SketchLineChange** cell is set to 0%, the geometry of the shape's line matches the shape's geometry.</span></span> <span data-ttu-id="09b5e-108">Wenn der Wert 100 % beträgt, folgt die Geometrie der Linie des Shapes nicht der Geometrie der Form.</span><span class="sxs-lookup"><span data-stu-id="09b5e-108">If the value is 100%, the geometry of the shape's line does not follow the geometry of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="09b5e-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="09b5e-109">Remarks</span></span>

<span data-ttu-id="09b5e-110">Für optimale Ergebnisse liegt der ideale Wertebereich für die **Zelle SketchLineChange** zwischen 15 % und 50 %.</span><span class="sxs-lookup"><span data-stu-id="09b5e-110">For best results, the ideal range of values for the **SketchLineChange** cell is between 15% and 50%.</span></span> <span data-ttu-id="09b5e-111">Ein Wert unter 15 % ist kaum wahrnehmbar. Bei einem Wert von mehr als 50 % könnte die Zeile zu viel zufällig gewählt werden.</span><span class="sxs-lookup"><span data-stu-id="09b5e-111">A value below 15% is barely noticeable; a value greater than 50% could randomize the line too much.</span></span> 
  
<span data-ttu-id="09b5e-112">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle SketchLineChange** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="09b5e-112">To get a reference to the **SketchLineChange** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09b5e-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="09b5e-113">Cell name:</span></span>  <br/> | <span data-ttu-id="09b5e-114">SketchLineChange</span><span class="sxs-lookup"><span data-stu-id="09b5e-114">SketchLineChange</span></span>  <br/> |
   
<span data-ttu-id="09b5e-115">Um einen Verweis auf die **Zelle SketchLineChange nach** Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="09b5e-115">To get a reference to the **SketchLineChange** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="09b5e-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="09b5e-116">Section index:</span></span>  <br/> |<span data-ttu-id="09b5e-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="09b5e-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="09b5e-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="09b5e-118">Row index:</span></span>  <br/> |<span data-ttu-id="09b5e-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="09b5e-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="09b5e-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="09b5e-120">Cell index:</span></span>  <br/> |<span data-ttu-id="09b5e-121">**visSketchLineChange**</span><span class="sxs-lookup"><span data-stu-id="09b5e-121">**visSketchLineChange**</span></span> <br/> |
   

