---
title: Zelle "DisplayLevel" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm80001
localization_priority: Normal
ms.assetid: 08b730c4-5dd8-106e-ddf3-da2c942e2ef6
description: Bestimmt den Anzeigeebenenbereich (den relativen Bereich der Gruppierung in Z-Reihenfolge) für das Shape.
ms.openlocfilehash: 4f7e3fcb2d28f8c4c0706502c66444c121ae6ee6
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408145"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="9393b-103">Zelle "DisplayLevel" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="9393b-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="9393b-104">Bestimmt den Anzeigeebenenbereich (den relativen Bereich der Gruppierung in Z-Reihenfolge) für das Shape.</span><span class="sxs-lookup"><span data-stu-id="9393b-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9393b-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9393b-105">Remarks</span></span>

<span data-ttu-id="9393b-p101">Die Z-Reihenfolge ist die Anzeigereihenfolge für Shapes auf dem Zeichenblatt. Ein Shape, das sich in der Z-Reihenfolge weiter oben befindet, wird vor einem Shape anzeigt, das sich in der Z-Reihenfolge weiter unten befindet, wenn eines der Shapes das andere überlagert.</span><span class="sxs-lookup"><span data-stu-id="9393b-p101">Z-order is the display order for shapes on the drawing page. A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="9393b-p102">Mit der Anzeigeebene werden Shapes in Gruppierungen oder Bereiche aufgeteilt. Alle Shapes in einem gegebenen Bereich haben eine höhere Z-Reihenfolge als die Shapes in einem niedrigeren Bereich. Standardmäßig weisen die meisten Shapes eine Anzeigeebene von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="9393b-p102">The display level divides shapes into groupings, or bands. All shapes in a given band have a higher Z-order than the shapes in a lower band. By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="9393b-p103">Der Bereich der Anzeigeebenen rangiert von -32.767 bis +32.767. Shapes mit der gleichen Anzeigeebene werden zu einem einzigen Bereich zusammengefasst, in dem sie ebenfalls gemäß der Z-Reihenfolge relativ zueinander in eine Rangfolge gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="9393b-p103">The range of display levels is from -32,767 to +32,767. Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="9393b-113">Sie können die Z-Reihenfolge von Formen innerhalb eines Bandes ändern, indem Sie die Befehle **Bring Forward,** **Send Backward,** **Bring to Front** und Send to **Back verwenden.**</span><span class="sxs-lookup"><span data-stu-id="9393b-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="9393b-114">Wird ein Shape mit diesen Befehlen aus dem angestammten Bereich verschoben, zeigt Microsoft Visio den reservierten Wert -32768 in der Zelle "DisplayLevel" des Shapes an, sofern die Zelle nicht geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="9393b-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="9393b-115">In dem Fall kann das Shape nicht in einen anderen Bereich verschoben werden, und Visio gibt die Warnung "Aktiver Shape-Schutz oder Container- und/oder Layereigenschaften verhindern die vollständige Ausführung dieses Befehls" aus.</span><span class="sxs-lookup"><span data-stu-id="9393b-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="9393b-116">Verwenden Sie folgendes, um einen Verweis auf die Zelle DisplayLevel anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft** zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9393b-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9393b-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9393b-117">Cell name:</span></span>  <br/> |<span data-ttu-id="9393b-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="9393b-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="9393b-119">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DisplayLevel-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="9393b-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9393b-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9393b-120">Section index:</span></span>  <br/> |<span data-ttu-id="9393b-121">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9393b-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9393b-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9393b-122">Row index:</span></span>  <br/> |<span data-ttu-id="9393b-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="9393b-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="9393b-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9393b-124">Cell index:</span></span>  <br/> |<span data-ttu-id="9393b-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="9393b-125">**visSLODisplayLevel**</span></span> <br/> |
   

