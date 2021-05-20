---
title: Zelle ReplaceLockFormat (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. Wenn die Zelle ReplaceLockFormat eines Master-Shapes auf TRUE (1) festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das durch den Master ersetzt wird.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427234"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="14156-104">Zelle ReplaceLockFormat (Abschnitt "Change Shape Behavior")</span><span class="sxs-lookup"><span data-stu-id="14156-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="14156-105">Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="14156-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="14156-106">Wenn die **Zelle ReplaceLockFormat** eines Master-Shapes auf TRUE (1) festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das durch den Master ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="14156-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="14156-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="14156-107">**Value**</span></span>|<span data-ttu-id="14156-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="14156-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="14156-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="14156-109">TRUE</span></span>  <br/> |<span data-ttu-id="14156-110">Wenn die **Zelle ReplaceLockFormat** eines Master-Shapes auf TRUE festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das durch den Master ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="14156-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="14156-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="14156-111">FALSE</span></span>  <br/> |<span data-ttu-id="14156-112">Wenn die **Zelle ReplaceLockFormat** eines Master-Shapes auf FALSE festgelegt ist, enthält die Ersatzform die lokalen Formatierungswerte aus der alten Form nach dem Ersetzungsvorgang.</span><span class="sxs-lookup"><span data-stu-id="14156-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="14156-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="14156-113">Remarks</span></span>

<span data-ttu-id="14156-114">Die **Zelle ReplaceLockFormat** bestimmt, ob die Masterform die lokalen Formatierungswerte der Zellen in den folgenden Abschnitten während eines Shapeersetzungsvorgangs überschreibt:</span><span class="sxs-lookup"><span data-stu-id="14156-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="14156-115">**Abschnitt "Fill Format"**</span><span class="sxs-lookup"><span data-stu-id="14156-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="14156-116">**Abschnitt "Linienformat"**</span><span class="sxs-lookup"><span data-stu-id="14156-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="14156-117">**Abschnitt "Quick Style"**</span><span class="sxs-lookup"><span data-stu-id="14156-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="14156-118">**Abschnitt "Designeigenschaften"**</span><span class="sxs-lookup"><span data-stu-id="14156-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="14156-119">**Abschnitt "Gradient Properties"**</span><span class="sxs-lookup"><span data-stu-id="14156-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="14156-120">**Abschnitt "Abschrägungseigenschaften"**</span><span class="sxs-lookup"><span data-stu-id="14156-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="14156-121">**Abschnitt "Zusätzliche Effekteigenschaften"**</span><span class="sxs-lookup"><span data-stu-id="14156-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="14156-122">**Abschnitt "Line Gradient Stops"**</span><span class="sxs-lookup"><span data-stu-id="14156-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="14156-123">**Abschnitt "Füllgradientenstopps"**</span><span class="sxs-lookup"><span data-stu-id="14156-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="14156-124">Um einen Verweis auf die **Zelle ReplaceLockFormat** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="14156-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14156-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="14156-125">Cell name:</span></span>  <br/> | <span data-ttu-id="14156-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="14156-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="14156-127">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ReplaceLockFormat** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="14156-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="14156-128">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="14156-128">Section index:</span></span>  <br/> |<span data-ttu-id="14156-129">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="14156-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="14156-130">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="14156-130">Row index:</span></span>  <br/> |<span data-ttu-id="14156-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="14156-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="14156-132">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="14156-132">Cell index:</span></span>  <br/> |<span data-ttu-id="14156-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="14156-133">**visReplaceLockFormat**</span></span> <br/> |
   

