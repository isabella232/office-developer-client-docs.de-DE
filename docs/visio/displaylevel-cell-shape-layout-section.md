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
ms.openlocfilehash: 516446b2d401aaca614e24a2c5bb5003fafe8574
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796836"
---
# <a name="displaylevel-cell-shape-layout-section"></a><span data-ttu-id="cf962-103">DisplayLevel Cell (Shape Layout Section)</span><span class="sxs-lookup"><span data-stu-id="cf962-103">DisplayLevel Cell (Shape Layout Section)</span></span>

<span data-ttu-id="cf962-104">Bestimmt den Anzeigeebenenbereich (den relativen Bereich der Gruppierung in Z-Reihenfolge) für das Shape.</span><span class="sxs-lookup"><span data-stu-id="cf962-104">Determines the display level band (the relative range of Z-order grouping) for the shape.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cf962-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cf962-105">Remarks</span></span>

<span data-ttu-id="cf962-p101">Die Z-Reihenfolge ist die Anzeigereihenfolge für Shapes auf dem Zeichenblatt. Ein Shape, das sich in der Z-Reihenfolge weiter oben befindet, wird vor einem Shape anzeigt, das sich in der Z-Reihenfolge weiter unten befindet, wenn eines der Shapes das andere überlagert.</span><span class="sxs-lookup"><span data-stu-id="cf962-p101">Z-order is the display order for shapes on the drawing page. A shape that is higher in the Z-order appears in front of a shape that is lower in the Z-order when one of the shapes overlays the other one.</span></span> 
  
<span data-ttu-id="cf962-p102">Mit der Anzeigeebene werden Shapes in Gruppierungen oder Bereiche aufgeteilt. Alle Shapes in einem gegebenen Bereich haben eine höhere Z-Reihenfolge als die Shapes in einem niedrigeren Bereich. Standardmäßig weisen die meisten Shapes eine Anzeigeebene von 0 (null) auf.</span><span class="sxs-lookup"><span data-stu-id="cf962-p102">The display level divides shapes into groupings, or bands. All shapes in a given band have a higher Z-order than the shapes in a lower band. By default, most shapes have a display level of zero (0).</span></span>
  
<span data-ttu-id="cf962-p103">Der Bereich der Anzeigeebenen rangiert von -32.767 bis +32.767. Shapes mit der gleichen Anzeigeebene werden zu einem einzigen Bereich zusammengefasst, in dem sie ebenfalls gemäß der Z-Reihenfolge relativ zueinander in eine Rangfolge gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cf962-p103">The range of display levels is from -32,767 to +32,767. Shapes that have the same display level are combined into a single band, within which they are also ranked relative to one another by Z-order.</span></span>
  
<span data-ttu-id="cf962-113">Sie können mithilfe der Befehle **In den Vordergrund**, **Eine Ebene nach hinten**, **in den Vordergrund**und **in den Hintergrund**der Z-Ordnung der Formen einen Streifen ändern.</span><span class="sxs-lookup"><span data-stu-id="cf962-113">You can change the Z-order of shapes within a band by using the commands **Bring Forward**, **Send Backward**, **Bring to Front**, and **Send to Back**.</span></span> <span data-ttu-id="cf962-114">Diese Befehle eine Form aus der angegebenen Band verschieben, zeigt Microsoft Visio den reservierten Wert-32768 in Zelle DisplayLevel des Shapes, sofern die Zelle geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="cf962-114">If those commands move a shape out of its given band, Microsoft Visio displays the reserved value -32768 in the shape's DisplayLevel cell, unless the cell is guarded.</span></span> <span data-ttu-id="cf962-115">In diesem Fall die Form nicht in einem anderen Band verschoben werden, und Visio zeigt die Warnung "Schutz und/oder Layer Formeigenschaften verhindern Ausführung dieses Befehls abgeschlossen".</span><span class="sxs-lookup"><span data-stu-id="cf962-115">In that case, the shape cannot be moved to a different band, and Visio displays the warning "Shape protection and/or layer properties prevent complete execution of this command."</span></span> 
  
<span data-ttu-id="cf962-116">Zum Abrufen eines Verweises auf die Zelle DisplayLevel nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes.</span><span class="sxs-lookup"><span data-stu-id="cf962-116">To get a reference to the DisplayLevel cell by name from another formula or from a program by using the **CellsU** property, use the following.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf962-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="cf962-117">Cell name:</span></span>  <br/> |<span data-ttu-id="cf962-118">DisplayLevel</span><span class="sxs-lookup"><span data-stu-id="cf962-118">DisplayLevel</span></span>  <br/> |
   
<span data-ttu-id="cf962-119">Wenn Sie einen Verweis auf die Zelle DisplayLevel aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="cf962-119">To get a reference to the DisplayLevel cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="cf962-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="cf962-120">Section index:</span></span>  <br/> |<span data-ttu-id="cf962-121">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="cf962-121">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="cf962-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="cf962-122">Row index:</span></span>  <br/> |<span data-ttu-id="cf962-123">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="cf962-123">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="cf962-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="cf962-124">Cell index:</span></span>  <br/> |<span data-ttu-id="cf962-125">**visSLODisplayLevel**</span><span class="sxs-lookup"><span data-stu-id="cf962-125">**visSLODisplayLevel**</span></span> <br/> |
   

