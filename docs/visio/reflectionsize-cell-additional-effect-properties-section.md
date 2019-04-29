---
title: Reflexions Zelle (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7dfeb78e-a0fa-4492-b35f-70b1e2975d38
description: Bestimmt die Größe der Reflektion relativ zum Shape, als Prozentsatz von 0,0 bis 100,0%. Ein Shape mit dem Wert 0% in der Zelle reFlexe hat keine Reflexion; ein Wert von 100% zeigt ein vollständiges Spiegelbild der Form an.
ms.openlocfilehash: 60fcb315ec1b6187082bdcdbbdcfaa4b80bbcfb3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409076"
---
# <a name="reflectionsize-cell-additional-effect-properties-section"></a><span data-ttu-id="c55a7-104">Reflexions Zelle (Abschnitt "Additional Effect Properties")</span><span class="sxs-lookup"><span data-stu-id="c55a7-104">ReflectionSize Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="c55a7-105">Bestimmt die Größe der Reflektion relativ zum Shape, als Prozentsatz von 0,0 bis 100,0%.</span><span class="sxs-lookup"><span data-stu-id="c55a7-105">Determines the size of the reflection relative to the shape, as a percentage from 0.0 to 100.0%.</span></span> <span data-ttu-id="c55a7-106">Ein Shape mit dem Wert 0% in der Zelle \*\*\*\* Reflexe hat keine Reflexion; ein Wert von 100% zeigt ein vollständiges Spiegelbild der Form an.</span><span class="sxs-lookup"><span data-stu-id="c55a7-106">A shape with a value of 0% in the **ReflectionSize** cell does not have a reflection; a value of 100% displays a complete mirror image of the shape.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c55a7-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c55a7-107">Remarks</span></span>

<span data-ttu-id="c55a7-108">Wenn Sie einen Verweis auf die \*\*\*\* Zelle Reflexe aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="c55a7-108">To get a reference to the **ReflectionSize** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c55a7-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c55a7-109">Cell name:</span></span>  <br/> | <span data-ttu-id="c55a7-110">Reflexion</span><span class="sxs-lookup"><span data-stu-id="c55a7-110">ReflectionSize</span></span>  <br/> |
   
<span data-ttu-id="c55a7-111">Wenn Sie einen Verweis auf die \*\*\*\* Zelle Reflexe aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="c55a7-111">To get a reference to the **ReflectionSize** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c55a7-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c55a7-112">Section index:</span></span>  <br/> |<span data-ttu-id="c55a7-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c55a7-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c55a7-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c55a7-114">Row index:</span></span>  <br/> |<span data-ttu-id="c55a7-115">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="c55a7-115">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="c55a7-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c55a7-116">Cell index:</span></span>  <br/> |<span data-ttu-id="c55a7-117">**visReflectionSize**</span><span class="sxs-lookup"><span data-stu-id="c55a7-117">**visReflectionSize**</span></span> <br/> |
   

