---
title: Zelle "FillGradientEnabled" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Bestimmt, ob für diese Form ein Füllgradient aktiviert ist.
ms.openlocfilehash: 17f617c13b632318be22b86a3354a194f0f835f5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431211"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="13672-103">Zelle "FillGradientEnabled" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="13672-103">FillGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="13672-104">Bestimmt, ob für diese Form ein Füllgradient aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="13672-104">Determines whether a fill gradient is enabled for this shape.</span></span> 
  
|<span data-ttu-id="13672-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="13672-105">**Value**</span></span>|<span data-ttu-id="13672-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13672-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="13672-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="13672-107">TRUE</span></span>  <br/> |<span data-ttu-id="13672-108">Die Farbverlaufsfüllung wird auf der Form angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13672-108">Gradient fill is displayed on the shape.</span></span>  <br/> |
|<span data-ttu-id="13672-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="13672-109">FALSE</span></span>  <br/> |<span data-ttu-id="13672-110">Farbverlaufsfüllungen werden in der Form nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="13672-110">Gradient fills are not displayed on the shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="13672-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="13672-111">Remarks</span></span>

<span data-ttu-id="13672-112">Um einen Verweis auf die **FillGradientEnabled-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="13672-112">To get a reference to the **FillGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13672-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="13672-113">Cell name:</span></span>  <br/> | <span data-ttu-id="13672-114">FillGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="13672-114">FillGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="13672-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **FillGradientEnabled-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="13672-115">To get a reference to the **FillGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="13672-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="13672-116">Section index:</span></span>  <br/> |<span data-ttu-id="13672-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="13672-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="13672-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="13672-118">Row index:</span></span>  <br/> |<span data-ttu-id="13672-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="13672-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="13672-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="13672-120">Cell index:</span></span>  <br/> |<span data-ttu-id="13672-121">\*\*visFillGradientEnabled \*\*</span><span class="sxs-lookup"><span data-stu-id="13672-121">\*\*visFillGradientEnabled \*\*</span></span> <br/> |
   

