---
title: LockVariation Cell (Protection section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 36acb95d-5d3b-4d8b-9b6c-effbc78c84c2
description: Bestimmt, ob die Design Variation, die auf die Seite oder Form angewendet wird, als boolescher Wert geändert werden kann.
ms.openlocfilehash: 69c991e3da7a96d6c59dc825dfb78fdad3d432e7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358065"
---
# <a name="lockvariation-cell-protection-section"></a><span data-ttu-id="fd056-103">LockVariation Cell (Protection section)</span><span class="sxs-lookup"><span data-stu-id="fd056-103">LockVariation Cell (Protection Section)</span></span>

<span data-ttu-id="fd056-104">Bestimmt, ob die Design Variation, die auf die Seite oder Form angewendet wird, als boolescher Wert geändert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fd056-104">Determines whether the theme variation applied to the page or shape can be changed, as a Boolean.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="fd056-105">TRUE</span><span class="sxs-lookup"><span data-stu-id="fd056-105">TRUE</span></span>  <br/> |<span data-ttu-id="fd056-106">Die aktuelle Variation, die auf die Seite oder Form angewendet wird, kann nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fd056-106">The current variation applied to the page or shape cannot be changed.</span></span>  <br/> |
|<span data-ttu-id="fd056-107">FALSE</span><span class="sxs-lookup"><span data-stu-id="fd056-107">FALSE</span></span>  <br/> |<span data-ttu-id="fd056-108">Die Variation der Seite oder Form kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fd056-108">The variation of the page or shape can be changed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd056-109">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd056-109">Remarks</span></span>

<span data-ttu-id="fd056-110">Wenn Sie einen Verweis auf die Zelle **LockVariation** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fd056-110">To get a reference to the **LockVariation** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd056-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fd056-111">Cell name:</span></span>  <br/> | <span data-ttu-id="fd056-112">LockVariation</span><span class="sxs-lookup"><span data-stu-id="fd056-112">LockVariation</span></span>  <br/> |
   
<span data-ttu-id="fd056-113">Wenn Sie einen Verweis auf die Zelle **LockVariation** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="fd056-113">To get a reference to the **LockVariation** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fd056-114">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fd056-114">Section index:</span></span>  <br/> |<span data-ttu-id="fd056-115">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fd056-115">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fd056-116">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fd056-116">Row index:</span></span>  <br/> |<span data-ttu-id="fd056-117">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="fd056-117">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="fd056-118">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fd056-118">Cell index:</span></span>  <br/> |<span data-ttu-id="fd056-119">**visLockVariation**</span><span class="sxs-lookup"><span data-stu-id="fd056-119">**visLockVariation**</span></span> <br/> |
   

