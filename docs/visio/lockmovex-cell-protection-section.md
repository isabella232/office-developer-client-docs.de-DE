---
title: Zelle "LockMoveX" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm640
localization_priority: Normal
ms.assetid: 48ceeeed-66ae-a81f-2aee-f0010102dfb7
description: Sperrt die horizontale Position des Shapes, damit es nicht horizontal verschoben werden kann.
ms.openlocfilehash: af0cee32370a540cd8d7aaf960cc0cbc27cc8f97
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348265"
---
# <a name="lockmovex-cell-protection-section"></a><span data-ttu-id="e23cc-103">Zelle "LockMoveX" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="e23cc-103">LockMoveX Cell (Protection Section)</span></span>

<span data-ttu-id="e23cc-104">Sperrt die horizontale Position des Shapes, damit es nicht horizontal verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="e23cc-104">Locks the horizontal position of the shape so it cannot be moved horizontally.</span></span>
  
|<span data-ttu-id="e23cc-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e23cc-105">**Value**</span></span>|<span data-ttu-id="e23cc-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e23cc-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="e23cc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="e23cc-107">TRUE</span></span>  <br/> | <span data-ttu-id="e23cc-108">Horizontale Position ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e23cc-108">Horizontal position is locked.</span></span>  <br/> |
| <span data-ttu-id="e23cc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="e23cc-109">FALSE</span></span>  <br/> | <span data-ttu-id="e23cc-110">Horizontale Position ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="e23cc-110">Horizontal position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e23cc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e23cc-111">Remarks</span></span>

<span data-ttu-id="e23cc-112">Wenn Sie einen Verweis auf die Zelle LockMoveX aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e23cc-112">To get a reference to the LockMoveX cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e23cc-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e23cc-113">Cell name:</span></span>  <br/> | <span data-ttu-id="e23cc-114">LockMoveX</span><span class="sxs-lookup"><span data-stu-id="e23cc-114">LockMoveX</span></span>  <br/> |
   
<span data-ttu-id="e23cc-115">Wenn Sie einen Verweis auf die Zelle LockMoveX aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e23cc-115">To get a reference to the LockMoveX cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e23cc-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e23cc-116">Section index:</span></span>  <br/> |<span data-ttu-id="e23cc-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e23cc-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e23cc-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e23cc-118">Row index:</span></span>  <br/> |<span data-ttu-id="e23cc-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="e23cc-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="e23cc-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e23cc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e23cc-121">**visLockMoveX**</span><span class="sxs-lookup"><span data-stu-id="e23cc-121">**visLockMoveX**</span></span> <br/> |
   

