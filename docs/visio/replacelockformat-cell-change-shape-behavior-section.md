---
title: ReplaceLockFormat Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Wenn die Zelle ReplaceLockFormat eines master-Shapes (1) "true" festgelegt ist, überschreiben die Formatierung Werte des Master-Shapes alle entsprechenden Werte eines Shapes, die durch das Master-Shape ersetzt wird.
ms.openlocfilehash: bf1e28353cc1e2d737a7d7a6dcd90caf14e19dc8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797825"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="df756-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="df756-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="df756-105">Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben.</span><span class="sxs-lookup"><span data-stu-id="df756-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="df756-106">Wenn die Zelle **ReplaceLockFormat** eines master-Shapes (1) "true" festgelegt ist, überschreiben die Formatierung Werte des Master-Shapes alle entsprechenden Werte eines Shapes, die durch das Master-Shape ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="df756-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="df756-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="df756-107">**Value**</span></span>|<span data-ttu-id="df756-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df756-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="df756-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="df756-109">TRUE</span></span>  <br/> |<span data-ttu-id="df756-110">Wenn die Zelle **ReplaceLockFormat** eines master-Shapes auf TRUE festgelegt ist, überschreiben die Formatierung Werte des Master-Shapes alle entsprechenden Werte eines Shapes, die durch das Master-Shape ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="df756-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="df756-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="df756-111">FALSE</span></span>  <br/> |<span data-ttu-id="df756-112">Wenn die Zelle **ReplaceLockFormat** eines master-Shapes auf FALSE festgelegt ist, enthält Ersatz-Shapes die Werte der lokalen Formatierung von der alten Form nach der Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="df756-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df756-113">Hinweise</span><span class="sxs-lookup"><span data-stu-id="df756-113">Remarks</span></span>

<span data-ttu-id="df756-114">Die Zelle **ReplaceLockFormat** bestimmt, ob das master-Shape der lokalen Formatierung Werte von Zellen in den folgenden Abschnitten während einer Form Ersetzungsvorgang überschreibt:</span><span class="sxs-lookup"><span data-stu-id="df756-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="df756-115">Abschnitt " **Fill Format** "</span><span class="sxs-lookup"><span data-stu-id="df756-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="df756-116">Abschnitt " **Line Format** "</span><span class="sxs-lookup"><span data-stu-id="df756-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="df756-117">**Schnellformatvorlagen** -Abschnitt</span><span class="sxs-lookup"><span data-stu-id="df756-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="df756-118">Abschnitt **Design-Eigenschaften**</span><span class="sxs-lookup"><span data-stu-id="df756-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="df756-119">**Farbverlauf Eigenschaften** im Abschnitt</span><span class="sxs-lookup"><span data-stu-id="df756-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="df756-120">Im Abschnitt **Eigenschaften für die Abschrägung**</span><span class="sxs-lookup"><span data-stu-id="df756-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="df756-121">**Zusätzliche Eigenschaften von Animationseffekten** -Abschnitt</span><span class="sxs-lookup"><span data-stu-id="df756-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="df756-122">**Zeile Farbverlaufstopps** -Abschnitt</span><span class="sxs-lookup"><span data-stu-id="df756-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="df756-123">**Füllen Sie Farbverlaufstopps** -Abschnitt</span><span class="sxs-lookup"><span data-stu-id="df756-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="df756-124">Wenn Sie einen Verweis auf die Zelle **ReplaceLockFormat** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="df756-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df756-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="df756-125">Cell name:</span></span>  <br/> | <span data-ttu-id="df756-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="df756-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="df756-127">Wenn Sie einen Verweis auf die Zelle **ReplaceLockFormat** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="df756-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="df756-128">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="df756-128">Section index:</span></span>  <br/> |<span data-ttu-id="df756-129">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="df756-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="df756-130">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="df756-130">Row index:</span></span>  <br/> |<span data-ttu-id="df756-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="df756-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="df756-132">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="df756-132">Cell index:</span></span>  <br/> |<span data-ttu-id="df756-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="df756-133">**visReplaceLockFormat**</span></span> <br/> |
   

