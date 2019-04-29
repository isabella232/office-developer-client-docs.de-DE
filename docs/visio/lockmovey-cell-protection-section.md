---
title: Zelle "LockMoveY" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm645
localization_priority: Normal
ms.assetid: 4ed8cab4-112a-e96a-f4e3-02490a6f87fa
description: Sperrt die vertikale Position des Shapes, damit es nicht vertikal verschoben werden kann.
ms.openlocfilehash: 6666d47555f8175b4950f95e1fb15abb8b11bfd5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434046"
---
# <a name="lockmovey-cell-protection-section"></a><span data-ttu-id="ca6cc-103">Zelle "LockMoveY" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="ca6cc-103">LockMoveY Cell (Protection Section)</span></span>

<span data-ttu-id="ca6cc-104">Sperrt die vertikale Position des Shapes, damit es nicht vertikal verschoben werden kann.</span><span class="sxs-lookup"><span data-stu-id="ca6cc-104">Locks the vertical position of the shape so it cannot be moved vertically.</span></span>
  
|<span data-ttu-id="ca6cc-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="ca6cc-105">**Value**</span></span>|<span data-ttu-id="ca6cc-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ca6cc-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="ca6cc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="ca6cc-107">TRUE</span></span>  <br/> | <span data-ttu-id="ca6cc-108">Vertikale Position ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="ca6cc-108">Vertical position is locked.</span></span>  <br/> |
| <span data-ttu-id="ca6cc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="ca6cc-109">FALSE</span></span>  <br/> | <span data-ttu-id="ca6cc-110">Vertikale Position ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="ca6cc-110">Vertical position is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ca6cc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="ca6cc-111">Remarks</span></span>

<span data-ttu-id="ca6cc-112">Wenn Sie einen Verweis auf die Zelle Zelle LockMoveY aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="ca6cc-112">To get a reference to the LockMoveY cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca6cc-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="ca6cc-113">Cell name:</span></span>  <br/> | <span data-ttu-id="ca6cc-114">Zelle LockMoveY</span><span class="sxs-lookup"><span data-stu-id="ca6cc-114">LockMoveY</span></span>  <br/> |
   
<span data-ttu-id="ca6cc-115">Wenn Sie einen Verweis auf die Zelle Zelle LockMoveY aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="ca6cc-115">To get a reference to the LockMoveY cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="ca6cc-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="ca6cc-116">Section index:</span></span>  <br/> |<span data-ttu-id="ca6cc-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="ca6cc-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="ca6cc-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="ca6cc-118">Row index:</span></span>  <br/> |<span data-ttu-id="ca6cc-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="ca6cc-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="ca6cc-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="ca6cc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="ca6cc-121">**visLockMoveY**</span><span class="sxs-lookup"><span data-stu-id="ca6cc-121">**visLockMoveY**</span></span> <br/> |
   

