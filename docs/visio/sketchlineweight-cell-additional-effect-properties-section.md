---
title: Zelle "SketchLineWeight" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6cb838be-1d6d-48e1-8e9e-bd126f0c2385
description: Bestimmt die zusätzliche Stärke, die der Linienstärke als Ergebnis eines Skizziereffekts hinzugefügt wird, in Punkten von 0 bis 50. Die Dicke der Linie einer Form nimmt zu, wenn der Wert der Zelle SketchLineWeight zunimmt.
ms.openlocfilehash: 0ee71bbaec59f5c79b72314b08478f8028b4e0ba
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404512"
---
# <a name="sketchlineweight-cell-additional-effect-properties-section"></a><span data-ttu-id="62a42-104">Zelle "SketchLineWeight" (Abschnitt "Additional Effect Properties")</span><span class="sxs-lookup"><span data-stu-id="62a42-104">SketchLineWeight Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="62a42-105">Bestimmt die zusätzliche Stärke, die der Linienstärke als Ergebnis eines Skizziereffekts hinzugefügt wird, in Punkten von 0 bis 50.</span><span class="sxs-lookup"><span data-stu-id="62a42-105">Determines the additional thickness added to line weight as the result of a sketch effect, in points from 0 to 50.</span></span> <span data-ttu-id="62a42-106">Die Dicke der Linie einer Form nimmt zu, wenn der Wert der **Zelle SketchLineWeight** zunimmt.</span><span class="sxs-lookup"><span data-stu-id="62a42-106">The thickness of a shape's line increases as the value of the **SketchLineWeight** cell increases.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="62a42-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="62a42-107">Remarks</span></span>

<span data-ttu-id="62a42-108">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle SketchLineWeight** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="62a42-108">To get a reference to the **SketchLineWeight** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62a42-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="62a42-109">Cell name:</span></span>  <br/> | <span data-ttu-id="62a42-110">SketchLineWeight</span><span class="sxs-lookup"><span data-stu-id="62a42-110">SketchLineWeight</span></span>  <br/> |
   
<span data-ttu-id="62a42-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle SketchLineWeight** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="62a42-111">To get a reference to the **SketchLineWeight** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="62a42-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="62a42-112">Section index:</span></span>  <br/> |<span data-ttu-id="62a42-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="62a42-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="62a42-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="62a42-114">Row index:</span></span>  <br/> |<span data-ttu-id="62a42-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="62a42-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="62a42-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="62a42-116">Cell index:</span></span>  <br/> |<span data-ttu-id="62a42-117">**visSketchLineWeight**</span><span class="sxs-lookup"><span data-stu-id="62a42-117">**visSketchLineWeight**</span></span> <br/> |
   

