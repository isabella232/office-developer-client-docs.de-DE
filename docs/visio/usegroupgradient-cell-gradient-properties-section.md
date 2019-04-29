---
title: Zelle "UseGroupGradient" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f1dcf0ec-8b4a-4ee1-9208-b1c84e30d37b
description: Bestimmt, ob die Form einen Farbverlauf annimmt, wenn das Shape zusammen mit anderen Formen als boolescher Wert gruppiert wird. Der Wert der Zelle UseGroupGradient wirkt sich nur auf die Formfüllung aus.
ms.openlocfilehash: a69b48095aec93705c686a5401051f1d1e368d18
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411365"
---
# <a name="usegroupgradient-cell-gradient-properties-section"></a><span data-ttu-id="6c5e4-104">Zelle "UseGroupGradient" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="6c5e4-104">UseGroupGradient Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="6c5e4-105">Bestimmt, ob die Form einen Farbverlauf annimmt, wenn das Shape zusammen mit anderen Formen als boolescher Wert gruppiert wird.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-105">Determines whether the shape takes on a gradient when the shape is grouped together with other shapes, as a Boolean.</span></span> <span data-ttu-id="6c5e4-106">Der Wert der Zelle **UseGroupGradient** wirkt sich nur auf die Formfüllung aus.</span><span class="sxs-lookup"><span data-stu-id="6c5e4-106">The value of **UseGroupGradient** cell affects the shape fill only.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="6c5e4-107">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6c5e4-107">Remarks</span></span>

<span data-ttu-id="6c5e4-108">Wenn Sie einen Verweis auf die Zelle **UseGroupGradient** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6c5e4-108">To get a reference to the **UseGroupGradient** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c5e4-109">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6c5e4-109">Cell name:</span></span>  <br/> | <span data-ttu-id="6c5e4-110">UseGroupGradient</span><span class="sxs-lookup"><span data-stu-id="6c5e4-110">UseGroupGradient</span></span>  <br/> |
   
<span data-ttu-id="6c5e4-111">Wenn Sie einen Verweis auf die Zelle **UseGroupGradient** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6c5e4-111">To get a reference to the **UseGroupGradient** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c5e4-112">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6c5e4-112">Section index:</span></span>  <br/> |<span data-ttu-id="6c5e4-113">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6c5e4-113">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6c5e4-114">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6c5e4-114">Row index:</span></span>  <br/> |<span data-ttu-id="6c5e4-115">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="6c5e4-115">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="6c5e4-116">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6c5e4-116">Cell index:</span></span>  <br/> |<span data-ttu-id="6c5e4-117">\* \* visUseGroupGradient \* \*</span><span class="sxs-lookup"><span data-stu-id="6c5e4-117">\*\*visUseGroupGradient \*\*</span></span> <br/> |
   

