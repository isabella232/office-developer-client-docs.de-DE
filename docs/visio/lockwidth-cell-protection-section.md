---
title: Zelle "LockWidth" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm675
localization_priority: Normal
ms.assetid: fef022ea-38ab-2b66-60c8-b94a6b0bdfbf
description: Sperrt die Breite des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.
ms.openlocfilehash: 84c89b5f264c00d6fe5f95cb27eae74b91b88dc3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439807"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="d55b6-103">Zelle "LockWidth" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="d55b6-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="d55b6-104">Sperrt die Breite des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="d55b6-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="d55b6-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d55b6-105">**Value**</span></span>|<span data-ttu-id="d55b6-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d55b6-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="d55b6-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="d55b6-107">TRUE</span></span>  <br/> | <span data-ttu-id="d55b6-108">Breite ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d55b6-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="d55b6-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="d55b6-109">FALSE</span></span>  <br/> | <span data-ttu-id="d55b6-110">Breite ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="d55b6-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d55b6-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d55b6-111">Remarks</span></span>

<span data-ttu-id="d55b6-112">Um einen Verweis auf die Zelle LockWidth anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="d55b6-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d55b6-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d55b6-113">Cell name:</span></span>  <br/> | <span data-ttu-id="d55b6-114">LockWidth</span><span class="sxs-lookup"><span data-stu-id="d55b6-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="d55b6-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockWidth nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="d55b6-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d55b6-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d55b6-116">Section index:</span></span>  <br/> |<span data-ttu-id="d55b6-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d55b6-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d55b6-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d55b6-118">Row index:</span></span>  <br/> |<span data-ttu-id="d55b6-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="d55b6-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="d55b6-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d55b6-120">Cell index:</span></span>  <br/> |<span data-ttu-id="d55b6-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="d55b6-121">**visLockWidth**</span></span> <br/> |
   

