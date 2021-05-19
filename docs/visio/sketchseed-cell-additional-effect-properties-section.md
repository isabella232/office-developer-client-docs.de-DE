---
title: Zelle "SketchSeed" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6f62650d-36f8-4c6e-b79f-c9c397a5954d
description: Stellt einen Randomisierungswert dar, der zum Bestimmen der Geometrie eines Skizziereffekts als positive ganze Zahl verwendet wird. Der Wert der Zelle SketchSeed wird zufällig erstellt, wenn ein Skizziereneffekt auf die Form angewendet wird.
ms.openlocfilehash: 3ec58fbfa183d1a6d7bb6960672658f9a6cca073
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434396"
---
# <a name="sketchseed-cell-additional-effect-properties-section"></a><span data-ttu-id="4195d-104">Zelle "SketchSeed" (Abschnitt "Additional Effect Properties")</span><span class="sxs-lookup"><span data-stu-id="4195d-104">SketchSeed Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="4195d-105">Stellt einen Randomisierungswert dar, der zum Bestimmen der Geometrie eines Skizziereffekts als positive ganze Zahl verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4195d-105">Represents a randomization value used to determine the geometry of a sketch effect, as a positive integer.</span></span> <span data-ttu-id="4195d-106">Der Wert der **Zelle SketchSeed** wird zufällig erstellt, wenn ein Skizziereneffekt auf die Form angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4195d-106">The value of the **SketchSeed** cell is randomly created when a sketch effect is applied to the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4195d-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4195d-107">Remarks</span></span>

<span data-ttu-id="4195d-108">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle SketchSeed** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="4195d-108">To get a reference to the **SketchSeed** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4195d-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4195d-109">Cell name:</span></span>  <br/> | <span data-ttu-id="4195d-110">SketchSeed</span><span class="sxs-lookup"><span data-stu-id="4195d-110">SketchSeed</span></span>  <br/> |
   
<span data-ttu-id="4195d-111">Um einen Verweis auf die **Zelle SketchSeed nach** Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="4195d-111">To get a reference to the **SketchSeed** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4195d-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4195d-112">Section index:</span></span>  <br/> |<span data-ttu-id="4195d-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4195d-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4195d-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4195d-114">Row index:</span></span>  <br/> |<span data-ttu-id="4195d-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="4195d-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="4195d-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4195d-116">Cell index:</span></span>  <br/> |<span data-ttu-id="4195d-117">**visSketchSeed**</span><span class="sxs-lookup"><span data-stu-id="4195d-117">**visSketchSeed**</span></span> <br/> |
   

