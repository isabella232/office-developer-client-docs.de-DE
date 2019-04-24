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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359647"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="2e5cc-103">Zelle "LockBegin" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="2e5cc-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="2e5cc-104">Sperrt den Anfangspunkt (AnfangX, AnfangY) eines 1D-Shapes an einer bestimmten Position.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="2e5cc-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2e5cc-105">**Value**</span></span>|<span data-ttu-id="2e5cc-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e5cc-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2e5cc-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2e5cc-107">TRUE</span></span>  <br/> | <span data-ttu-id="2e5cc-108">Anfangspunkt ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="2e5cc-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2e5cc-109">FALSE</span></span>  <br/> | <span data-ttu-id="2e5cc-110">Anfang ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2e5cc-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e5cc-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="2e5cc-111">Remarks</span></span>

<span data-ttu-id="2e5cc-112">Wenn Sie einen Verweis auf die Zelle Zelle LockBegin aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2e5cc-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e5cc-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2e5cc-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2e5cc-114">Zelle LockBegin</span><span class="sxs-lookup"><span data-stu-id="2e5cc-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="2e5cc-115">Wenn Sie einen Verweis auf die Zelle Zelle LockBegin aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2e5cc-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e5cc-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2e5cc-116">Section index:</span></span>  <br/> |<span data-ttu-id="2e5cc-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e5cc-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2e5cc-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2e5cc-118">Row index:</span></span>  <br/> |<span data-ttu-id="2e5cc-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2e5cc-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2e5cc-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2e5cc-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2e5cc-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="2e5cc-121">**visLockBegin**</span></span> <br/> |
   

