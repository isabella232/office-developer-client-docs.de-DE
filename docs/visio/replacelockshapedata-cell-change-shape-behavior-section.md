---
title: Zelle ReplaceLockShapeData (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. ReplaceLockShapeData bestimmt, ob die Formdaten der Masterform alle Formdaten der ersetzten Form überschreiben.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408873"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="b864c-104">Zelle ReplaceLockShapeData (Abschnitt "Change Shape Behavior")</span><span class="sxs-lookup"><span data-stu-id="b864c-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="b864c-105">Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b864c-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="b864c-106">**ReplaceLockShapeData** bestimmt, ob die Formdaten der Masterform alle Formdaten der ersetzten Form überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b864c-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="b864c-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b864c-107">**Value**</span></span>|<span data-ttu-id="b864c-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b864c-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b864c-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="b864c-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="b864c-110">Alle Zeilen und Werte des Abschnitts **"Shape Data"** der Masterform werden in die Ersatzform kopiert, und alle lokalen Werte aus dem alten Shape, das ersetzt wird, werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="b864c-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="b864c-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="b864c-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="b864c-112">Die Zeilen und Werte des **Abschnitts Shape Data** des Master-Shapes werden in die Ersetzungsform kopiert.</span><span class="sxs-lookup"><span data-stu-id="b864c-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="b864c-113">Alle Zeilen im **Abschnitt Shape Data** der alten Form mit lokalen Werten werden auf die Ersatzform übertragen.</span><span class="sxs-lookup"><span data-stu-id="b864c-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b864c-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b864c-114">Remarks</span></span>

<span data-ttu-id="b864c-115">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle ReplaceLockShapeData** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="b864c-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b864c-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b864c-116">Cell name:</span></span>  <br/> | <span data-ttu-id="b864c-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="b864c-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="b864c-118">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ReplaceLockShapeData** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b864c-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b864c-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b864c-119">Section index:</span></span>  <br/> |<span data-ttu-id="b864c-120">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b864c-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b864c-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b864c-121">Row index:</span></span>  <br/> |<span data-ttu-id="b864c-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="b864c-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="b864c-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b864c-123">Cell index:</span></span>  <br/> |<span data-ttu-id="b864c-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="b864c-124">**visReplaceLockShapeData**</span></span> <br/> |
   

