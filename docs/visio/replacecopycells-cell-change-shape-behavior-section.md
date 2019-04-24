---
title: Zelle "ReplaceCopyCells" (Abschnitt "Shape-Verhalten ändern")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Gibt eine Liste der Zellen im ShapeSheet an, die während einer Form Ersetzung aus einem alten Shape in die Ersatzform kopiert werden.
ms.openlocfilehash: f2a7908a623c861d0284821b2d8ae5fc71690685
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32320174"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="d0925-103">Zelle "ReplaceCopyCells" (Abschnitt "Shape-Verhalten ändern")</span><span class="sxs-lookup"><span data-stu-id="d0925-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="d0925-104">Gibt eine Liste der Zellen im ShapeSheet an, die während einer Form Ersetzung aus einem alten Shape in die Ersatzform kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="d0925-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d0925-105">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d0925-105">Remarks</span></span>

<span data-ttu-id="d0925-106">Die Master-Form der Ersetzung muss einen **DependsOn** -Funktionsaufruf in der **ReplaceCopyCells** -Zelle enthalten, wobei jedes Argument in der Funktion ein Verweis auf eine Zelle ist.</span><span class="sxs-lookup"><span data-stu-id="d0925-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="d0925-107">Diese Zellen werden von der alten Form in die Form kopiert, die aus einem Shape-Ersetzungsvorgang resultiert, unabhängig davon, wo Sie sich im ShapeSheet befinden.</span><span class="sxs-lookup"><span data-stu-id="d0925-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="d0925-108">Werte und/oder Formeln, die auf andere Zellen verweisen, werden in die resultierende Form kopiert.</span><span class="sxs-lookup"><span data-stu-id="d0925-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="d0925-109">Wenn die resultierende Form nicht über die Zelle referenziert wird, enthält die kopierte Zelle nur den Wert.</span><span class="sxs-lookup"><span data-stu-id="d0925-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="d0925-110">Verweise in der **ReplaceCopyCells** Zellen Außerkraftsetzung für Zellen wie im Abschnitt **Protection** und die Zellen **ReplaceLockFormat**, **ReplaceLockShapeData**und **ReplaceLockText** definiert.</span><span class="sxs-lookup"><span data-stu-id="d0925-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="d0925-111">Wenn Sie einen Verweis auf die Zelle **ReplaceCopyCells** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d0925-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0925-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d0925-112">Cell name:</span></span>  <br/> | <span data-ttu-id="d0925-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="d0925-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="d0925-114">Wenn Sie einen Verweis auf die Zelle **ReplaceCopyCells** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d0925-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d0925-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d0925-115">Section index:</span></span>  <br/> |<span data-ttu-id="d0925-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d0925-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d0925-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d0925-117">Row index:</span></span>  <br/> |<span data-ttu-id="d0925-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="d0925-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="d0925-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d0925-119">Cell index:</span></span>  <br/> |<span data-ttu-id="d0925-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="d0925-120">**visReplaceCopyCells**</span></span> <br/> |
   

