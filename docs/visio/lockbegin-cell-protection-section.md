---
title: Zelle "LockBegin" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm600
localization_priority: Normal
ms.assetid: cce34aba-caae-51ee-992e-92a490b68ea5
description: Sperrt den Anfangspunkt (AnfangX, AnfangY) eines 1D-Shapes an einer bestimmten Position.
ms.openlocfilehash: 2e6c6284ff82a88677eb46bb13b8ab8afa986584
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407760"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="9d2ce-103">Zelle "LockBegin" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="9d2ce-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="9d2ce-104">Sperrt den Anfangspunkt (AnfangX, AnfangY) eines 1D-Shapes an einer bestimmten Position.</span><span class="sxs-lookup"><span data-stu-id="9d2ce-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="9d2ce-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9d2ce-105">**Value**</span></span>|<span data-ttu-id="9d2ce-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d2ce-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="9d2ce-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="9d2ce-107">TRUE</span></span>  <br/> | <span data-ttu-id="9d2ce-108">Anfangspunkt ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="9d2ce-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="9d2ce-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="9d2ce-109">FALSE</span></span>  <br/> | <span data-ttu-id="9d2ce-110">Anfang ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="9d2ce-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d2ce-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d2ce-111">Remarks</span></span>

<span data-ttu-id="9d2ce-112">Um einen Verweis auf die Zelle LockBegin anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="9d2ce-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d2ce-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9d2ce-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9d2ce-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="9d2ce-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="9d2ce-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockBegin nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="9d2ce-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9d2ce-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9d2ce-116">Section index:</span></span>  <br/> |<span data-ttu-id="9d2ce-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9d2ce-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9d2ce-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9d2ce-118">Row index:</span></span>  <br/> |<span data-ttu-id="9d2ce-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="9d2ce-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="9d2ce-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9d2ce-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9d2ce-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="9d2ce-121">**visLockBegin**</span></span> <br/> |
   

