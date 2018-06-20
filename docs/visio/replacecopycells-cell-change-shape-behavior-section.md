---
title: ReplaceCopyCells Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2f36aefd-da49-47ea-9b90-2fa1a2298849
description: Gibt eine Liste der Zellen im ShapeSheet, die während ein Shape Ersetzungsvorgang aus einer alten Form zum Ersatz-Shape kopiert werden.
ms.openlocfilehash: 1e3b5e4dbc29372f75b7a7ed8013a7dd82d94e1d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797812"
---
# <a name="replacecopycells-cell-change-shape-behavior-section"></a><span data-ttu-id="54df2-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="54df2-103">ReplaceCopyCells Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="54df2-104">Gibt eine Liste der Zellen im ShapeSheet, die während ein Shape Ersetzungsvorgang aus einer alten Form zum Ersatz-Shape kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="54df2-104">Indicates a list of cells in the ShapeSheet that are copied from an old shape to the replacement shape during a shape replacement operation.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="54df2-105">Hinweise</span><span class="sxs-lookup"><span data-stu-id="54df2-105">Remarks</span></span>

<span data-ttu-id="54df2-106">Das master-Shape die Ersetzung muss einen Funktionsaufruf **DEPENDSON** in der Zelle **ReplaceCopyCells** enthalten, wobei jedes Argument in der Funktion einen Verweis auf eine Zelle ist.</span><span class="sxs-lookup"><span data-stu-id="54df2-106">The master shape of the replacement must contain a **DEPENDSON** function call in the **ReplaceCopyCells** cell, where each argument in the function is a reference to a cell.</span></span> <span data-ttu-id="54df2-107">Betroffenen Zellen werden von der alten Form mit dem Shape kopiert, die eine Form Ersetzungsoperation, unabhängig davon, wo sie sich im ShapeSheet sind ergibt.</span><span class="sxs-lookup"><span data-stu-id="54df2-107">Those cells are copied from the old shape to the shape that results from a shape replacement operation, regardless of where they are in the ShapeSheet.</span></span> 
  
<span data-ttu-id="54df2-108">Werte und/oder Formeln, die von anderen Zellen referenziert werden im resultierenden Shape kopiert.</span><span class="sxs-lookup"><span data-stu-id="54df2-108">Values and/or formulas that reference other cells are copied to the resulting shape.</span></span> <span data-ttu-id="54df2-109">Wenn das resultierende Shape die referenzierte Zelle nicht vorhanden ist, enthält die kopierte Zelle nur den Wert.</span><span class="sxs-lookup"><span data-stu-id="54df2-109">If the resulting shape does not have the referenced cell, the copied cell contains the value only.</span></span> 
  
<span data-ttu-id="54df2-110">Verweise in der Zelle **ReplaceCopyCells** außer Kraft setzen Schutz auf Zellen gemäß Definition im Abschnitt " **Protection** " und die **ReplaceLockFormat**, **ReplaceLockShapeData**und **ReplaceLockText** Zellen festgelegt.</span><span class="sxs-lookup"><span data-stu-id="54df2-110">References in the **ReplaceCopyCells** cell override protection set on cells as defined in the **Protection** section and the **ReplaceLockFormat**, **ReplaceLockShapeData**, and **ReplaceLockText** cells.</span></span> 
  
<span data-ttu-id="54df2-111">Wenn Sie einen Verweis auf die Zelle **ReplaceCopyCells** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="54df2-111">To get a reference to the **ReplaceCopyCells** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54df2-112">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="54df2-112">Cell name:</span></span>  <br/> | <span data-ttu-id="54df2-113">ReplaceCopyCells</span><span class="sxs-lookup"><span data-stu-id="54df2-113">ReplaceCopyCells</span></span>  <br/> |
   
<span data-ttu-id="54df2-114">Wenn Sie einen Verweis auf die Zelle **ReplaceCopyCells** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="54df2-114">To get a reference to the **ReplaceCopyCells** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="54df2-115">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="54df2-115">Section index:</span></span>  <br/> |<span data-ttu-id="54df2-116">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="54df2-116">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="54df2-117">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="54df2-117">Row index:</span></span>  <br/> |<span data-ttu-id="54df2-118">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="54df2-118">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="54df2-119">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="54df2-119">Cell index:</span></span>  <br/> |<span data-ttu-id="54df2-120">**visReplaceCopyCells**</span><span class="sxs-lookup"><span data-stu-id="54df2-120">**visReplaceCopyCells**</span></span> <br/> |
   

