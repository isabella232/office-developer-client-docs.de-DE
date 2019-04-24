---
title: Zelle "ReplaceLockFormat" (Abschnitt "Shape-Verhalten ändern")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6973e2e6-7e7f-48ba-95b3-37c959f6ffb1
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Wenn die Zelle ReplaceLockFormat eines Master-Shapes auf TRUE (1) festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das vom Master ersetzt wird.
ms.openlocfilehash: 88af22accb7a80640e7553338dae1af48934f246
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329890"
---
# <a name="replacelockformat-cell-change-shape-behavior-section"></a><span data-ttu-id="176bd-104">Zelle "ReplaceLockFormat" (Abschnitt "Shape-Verhalten ändern")</span><span class="sxs-lookup"><span data-stu-id="176bd-104">ReplaceLockFormat Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="176bd-105">Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="176bd-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="176bd-106">Wenn die Zelle **ReplaceLockFormat** eines Master-Shapes auf true (1) festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das vom Master ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="176bd-106">If the **ReplaceLockFormat** cell of a master shape is set to TRUE (1), the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span> 
  
|<span data-ttu-id="176bd-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="176bd-107">**Value**</span></span>|<span data-ttu-id="176bd-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="176bd-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="176bd-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="176bd-109">TRUE</span></span>  <br/> |<span data-ttu-id="176bd-110">Wenn die Zelle **ReplaceLockFormat** eines Master-Shapes auf true festgelegt ist, überschreiben die Formatierungswerte des Masters alle entsprechenden Werte eines Shapes, das vom Master ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="176bd-110">If the **ReplaceLockFormat** cell of a master shape is set to TRUE, the formatting values of the master overwrite all corresponding values of a shape being replaced by the master.</span></span>  <br/> |
|<span data-ttu-id="176bd-111">FALSE</span><span class="sxs-lookup"><span data-stu-id="176bd-111">FALSE</span></span>  <br/> |<span data-ttu-id="176bd-112">Wenn die Zelle **ReplaceLockFormat** eines Master-Shapes auf false festgelegt ist, enthält die Ersatzform die lokalen Formatierungswerte aus dem alten Shape nach der Ersetzung.</span><span class="sxs-lookup"><span data-stu-id="176bd-112">If the **ReplaceLockFormat** cell of a master shape is set to FALSE, the replacement shape contains the local formatting values from the old shape after the replacement operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="176bd-113">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="176bd-113">Remarks</span></span>

<span data-ttu-id="176bd-114">Die **ReplaceLockFormat** -Zelle bestimmt, ob das Master-Shape die lokalen Formatierungswerte der Zellen in den folgenden Abschnitten während einer Form Ersetzung überschreibt:</span><span class="sxs-lookup"><span data-stu-id="176bd-114">The **ReplaceLockFormat** cell determines whether the master shape overwrites the local formatting values of the cells in the following sections during a shape replacement operation:</span></span> 
  
- <span data-ttu-id="176bd-115">Abschnitt " **Fill Format** "</span><span class="sxs-lookup"><span data-stu-id="176bd-115">**Fill Format** section</span></span> 
    
- <span data-ttu-id="176bd-116">Abschnitt " **Linien Format** "</span><span class="sxs-lookup"><span data-stu-id="176bd-116">**Line Format** section</span></span> 
    
- <span data-ttu-id="176bd-117">Abschnitt " **Schnellformatvorlage** "</span><span class="sxs-lookup"><span data-stu-id="176bd-117">**Quick Style** section</span></span> 
    
- <span data-ttu-id="176bd-118">Abschnitt " **Design Properties** "</span><span class="sxs-lookup"><span data-stu-id="176bd-118">**Theme Properties** section</span></span> 
    
- <span data-ttu-id="176bd-119">Abschnitt " **Gradient Properties** "</span><span class="sxs-lookup"><span data-stu-id="176bd-119">**Gradient Properties** section</span></span> 
    
- <span data-ttu-id="176bd-120">Abschnitt " **Fase Properties** "</span><span class="sxs-lookup"><span data-stu-id="176bd-120">**Bevel Properties** section</span></span> 
    
- <span data-ttu-id="176bd-121">Abschnitt " **additional Effect Properties** "</span><span class="sxs-lookup"><span data-stu-id="176bd-121">**Additional Effect Properties** section</span></span> 
    
- <span data-ttu-id="176bd-122">Abschnitt " **Linienverlauf beendet** "</span><span class="sxs-lookup"><span data-stu-id="176bd-122">**Line Gradient Stops** section</span></span> 
    
- <span data-ttu-id="176bd-123">Abschnitt " **Farbverlaufsstopps** "</span><span class="sxs-lookup"><span data-stu-id="176bd-123">**Fill Gradient Stops** section</span></span> 
    
<span data-ttu-id="176bd-124">Wenn Sie einen Verweis auf die Zelle **ReplaceLockFormat** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="176bd-124">To get a reference to the **ReplaceLockFormat** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="176bd-125">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="176bd-125">Cell name:</span></span>  <br/> | <span data-ttu-id="176bd-126">ReplaceLockFormat</span><span class="sxs-lookup"><span data-stu-id="176bd-126">ReplaceLockFormat</span></span>  <br/> |
   
<span data-ttu-id="176bd-127">Wenn Sie einen Verweis auf die Zelle **ReplaceLockFormat** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="176bd-127">To get a reference to the **ReplaceLockFormat** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="176bd-128">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="176bd-128">Section index:</span></span>  <br/> |<span data-ttu-id="176bd-129">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="176bd-129">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="176bd-130">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="176bd-130">Row index:</span></span>  <br/> |<span data-ttu-id="176bd-131">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="176bd-131">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="176bd-132">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="176bd-132">Cell index:</span></span>  <br/> |<span data-ttu-id="176bd-133">**visReplaceLockFormat**</span><span class="sxs-lookup"><span data-stu-id="176bd-133">**visReplaceLockFormat**</span></span> <br/> |
   

