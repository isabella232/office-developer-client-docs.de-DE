---
title: Zelle "LockVariation" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Bestimmt, ob die auf die Seite oder Form angewendete Designvariation als boolescher Wert geändert werden kann.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427927"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="89c1d-103">Zelle "LockVariation" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="89c1d-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="89c1d-104">Bestimmt, ob die auf die Seite oder Form angewendete Designvariation als boolescher Wert geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="89c1d-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="89c1d-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="89c1d-105">TRUE</span></span>  <br/> |<span data-ttu-id="89c1d-106">Die aktuelle Variation, die auf die Seite oder Form angewendet wird, kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="89c1d-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="89c1d-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="89c1d-107">FALSE</span></span>  <br/> |<span data-ttu-id="89c1d-108">Die Variation der Seite oder Form kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="89c1d-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="89c1d-109">Hinweise</span><span class="sxs-lookup"><span data-stu-id="89c1d-109">Remarks</span></span>

<span data-ttu-id="89c1d-110">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LockVariation** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="89c1d-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="89c1d-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="89c1d-111">Cell name:</span></span>  <br/> | <span data-ttu-id="89c1d-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="89c1d-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="89c1d-113">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **LockVariation-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="89c1d-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="89c1d-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="89c1d-114">Section index:</span></span>  <br/> |<span data-ttu-id="89c1d-115">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="89c1d-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="89c1d-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="89c1d-116">Row index:</span></span>  <br/> |<span data-ttu-id="89c1d-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="89c1d-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="89c1d-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="89c1d-118">Cell index:</span></span>  <br/> |<span data-ttu-id="89c1d-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="89c1d-119">**visLockVariation**</span></span> <br/> |
   

