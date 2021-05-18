---
title: Zelle "ReflectionSize" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: Bestimmt die Größe der Spiegelung relativ zur Form als Prozentsatz von 0,0 bis 100,0 %. Ein Shape mit einem Wert von 0 % in der Zelle ReflectionSize verfügt nicht über eine Spiegelung. Bei einem Wert von 100 % wird ein vollständiges Spiegelbild der Form angezeigt.
ms.openlocfilehash: 60fcb315ec1b6187082bdcdbbdcfaa4b80bbcfb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409076"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a><span data-ttu-id="224c1-104">Zelle "ReflectionSize" (Abschnitt "Additional Effect Properties")</span><span class="sxs-lookup"><span data-stu-id="224c1-104">ReflectionSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="224c1-105">Bestimmt die Größe der Spiegelung relativ zur Form als Prozentsatz von 0,0 bis 100,0 %.</span><span class="sxs-lookup"><span data-stu-id="224c1-105">Determines the size of the reflection relative to the shape, as a percentage from 0.0 to 100.0%.</span></span> <span data-ttu-id="224c1-106">Ein Shape mit einem Wert von 0 % in der **Zelle ReflectionSize** verfügt nicht über eine Spiegelung. Bei einem Wert von 100 % wird ein vollständiges Spiegelbild der Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="224c1-106">A shape with a value of 0% in the **ReflectionSize** cell does not have a reflection; a value of 100% displays a complete mirror image of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="224c1-107">Hinweise</span><span class="sxs-lookup"><span data-stu-id="224c1-107">Remarks</span></span>

<span data-ttu-id="224c1-108">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle ReflectionSize** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="224c1-108">To get a reference to the **ReflectionSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="224c1-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="224c1-109">Cell name:</span></span>  <br/> | <span data-ttu-id="224c1-110">ReflectionSize</span><span class="sxs-lookup"><span data-stu-id="224c1-110">ReflectionSize</span></span>  <br/> |
   
<span data-ttu-id="224c1-111">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **ReflectionSize-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="224c1-111">To get a reference to the **ReflectionSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="224c1-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="224c1-112">Section index:</span></span>  <br/> |<span data-ttu-id="224c1-113">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="224c1-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="224c1-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="224c1-114">Row index:</span></span>  <br/> |<span data-ttu-id="224c1-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="224c1-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="224c1-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="224c1-116">Cell index:</span></span>  <br/> |<span data-ttu-id="224c1-117">**visReflectionSize**</span><span class="sxs-lookup"><span data-stu-id="224c1-117">**visReflectionSize**</span></span> <br/> |
   

