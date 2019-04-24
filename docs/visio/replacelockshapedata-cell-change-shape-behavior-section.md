---
title: Zelle "ReplaceLockShapeData" (Abschnitt "Shape-Verhalten ändern")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6a089266-7b19-4310-8cb5-4373ea3b2d64
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Die ReplaceLockShapeData bestimmt, ob die Shape-Daten des Master-Shapes alle Shape-Daten der Form überschreiben, die ersetzt wird.
ms.openlocfilehash: d2349da96bde7d141aada9066d56a4379f425fee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348342"
---
# <a name="replacelockshapedata-cell-change-shape-behavior-section"></a><span data-ttu-id="c1b91-104">Zelle "ReplaceLockShapeData" (Abschnitt "Shape-Verhalten ändern")</span><span class="sxs-lookup"><span data-stu-id="c1b91-104">ReplaceLockShapeData Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="c1b91-105">Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c1b91-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="c1b91-106">Die **ReplaceLockShapeData** bestimmt, ob die Shape-Daten des Master-Shapes alle Shape-Daten der Form überschreiben, die ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="c1b91-106">The **ReplaceLockShapeData** determines whether the shape data of the master shape overwrites all of the shape data of the shape being replaced.</span></span> 
  
|<span data-ttu-id="c1b91-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c1b91-107">**Value**</span></span>|<span data-ttu-id="c1b91-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c1b91-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c1b91-109">1 (TRUE)</span><span class="sxs-lookup"><span data-stu-id="c1b91-109">1 (TRUE)</span></span>  <br/> |<span data-ttu-id="c1b91-110">Alle Zeilen und Werte des **Shape-Daten** Abschnitts des Master-Shapes werden in das Ersatz-Shape kopiert, und alle lokalen Werte aus dem alten zu ersetzenden Shape werden verworfen.</span><span class="sxs-lookup"><span data-stu-id="c1b91-110">All rows and values of the **Shape Data** section of the master shape are copied onto the replacement shape and any local values from the old shape being replaced are discarded.</span></span>  <br/> |
|<span data-ttu-id="c1b91-111">0 (FALSCH)</span><span class="sxs-lookup"><span data-stu-id="c1b91-111">0 (FALSE)</span></span>  <br/> |<span data-ttu-id="c1b91-112">Die Zeilen und Werte des **Shape-Daten** Abschnitts des Master-Shapes werden in die Ersatzform kopiert.</span><span class="sxs-lookup"><span data-stu-id="c1b91-112">The rows and values of the **Shape Data** section of the master shape are copied to the replacement shape.</span></span> <span data-ttu-id="c1b91-113">Alle Zeilen im **Shape-Daten** Abschnitt des alten Shapes mit lokalen Werten werden an das Ersatz-Shape übertragen.</span><span class="sxs-lookup"><span data-stu-id="c1b91-113">Any rows in the **Shape Data** section of the old shape with local values are transferred to the replacement shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c1b91-114">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c1b91-114">Remarks</span></span>

<span data-ttu-id="c1b91-115">Wenn Sie einen Verweis auf die Zelle **ReplaceLockShapeData** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c1b91-115">To get a reference to the **ReplaceLockShapeData** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1b91-116">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c1b91-116">Cell name:</span></span>  <br/> | <span data-ttu-id="c1b91-117">ReplaceLockShapeData</span><span class="sxs-lookup"><span data-stu-id="c1b91-117">ReplaceLockShapeData</span></span>  <br/> |
   
<span data-ttu-id="c1b91-118">Wenn Sie einen Verweis auf die Zelle **ReplaceLockShapeData** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c1b91-118">To get a reference to the **ReplaceLockShapeData** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c1b91-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c1b91-119">Section index:</span></span>  <br/> |<span data-ttu-id="c1b91-120">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c1b91-120">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c1b91-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c1b91-121">Row index:</span></span>  <br/> |<span data-ttu-id="c1b91-122">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="c1b91-122">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="c1b91-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c1b91-123">Cell index:</span></span>  <br/> |<span data-ttu-id="c1b91-124">**visReplaceLockShapeData**</span><span class="sxs-lookup"><span data-stu-id="c1b91-124">**visReplaceLockShapeData**</span></span> <br/> |
   

