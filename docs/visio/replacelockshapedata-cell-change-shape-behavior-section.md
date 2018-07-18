---
title: ReplaceLockShapeData Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Die ReplaceLockShapeData bestimmt, ob die Shape-Daten des master-Shapes überschreibt alle Shape-Daten der Form ersetzt werden.
ms.openlocfilehash: 07547140c7c96e49663270e51a90fd559afedf29
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797847"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="2ca86-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="2ca86-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="2ca86-105">Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben.</span><span class="sxs-lookup"><span data-stu-id="2ca86-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="2ca86-106">Die **ReplaceLockShapeData** bestimmt, ob die Shape-Daten des master-Shapes aller der Form ersetzt die Shape-Daten überschreibt.</span><span class="sxs-lookup"><span data-stu-id="2ca86-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="2ca86-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2ca86-107">**Value**</span></span>|<span data-ttu-id="2ca86-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2ca86-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2ca86-109">1 (WAHR)</span><span class="sxs-lookup"><span data-stu-id="2ca86-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="2ca86-110">Alle Zeilen und Werte des **Shape** -Datenabschnitt des master-Shapes auf das Ersatz-Shape kopiert wurden, und alle lokalen Werte vom alten Shape ersetzt werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="2ca86-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="2ca86-111">0 (FALSE)</span><span class="sxs-lookup"><span data-stu-id="2ca86-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="2ca86-112">Die Zeilen und Werte der **Shape** -Datenabschnitt des master-Shapes werden zum Ersatz-Shape kopiert.</span><span class="sxs-lookup"><span data-stu-id="2ca86-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="2ca86-113">Alle Zeilen in der **Shape** -Datenabschnitt der alten Form mit lokalen Werte werden zum Ersatz-Shape übertragen.</span><span class="sxs-lookup"><span data-stu-id="2ca86-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2ca86-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2ca86-114">Remarks</span></span>

<span data-ttu-id="2ca86-115">Wenn Sie einen Verweis auf die Zelle **ReplaceLockShapeData** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2ca86-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ca86-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2ca86-116">Cell name:</span></span>  <br/> | <span data-ttu-id="2ca86-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="2ca86-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="2ca86-118">Wenn Sie einen Verweis auf die Zelle **ReplaceLockShapeData** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2ca86-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2ca86-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2ca86-119">Section index:</span></span>  <br/> |<span data-ttu-id="2ca86-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2ca86-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2ca86-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2ca86-121">Row index:</span></span>  <br/> |<span data-ttu-id="2ca86-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="2ca86-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="2ca86-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2ca86-123">Cell index:</span></span>  <br/> |<span data-ttu-id="2ca86-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="2ca86-124">**visReplaceLockShapeData**</span></span> <br/> |
   

