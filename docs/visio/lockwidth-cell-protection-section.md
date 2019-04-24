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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314833"
---
# <a name="lockwidth-cell-protection-section"></a><span data-ttu-id="96633-103">Zelle "LockWidth" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="96633-103">LockWidth Cell (Protection Section)</span></span>

<span data-ttu-id="96633-104">Sperrt die Breite des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="96633-104">Locks the width of the shape so that its width remains unchanged when the shape is sized.</span></span>
  
|<span data-ttu-id="96633-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="96633-105">**Value**</span></span>|<span data-ttu-id="96633-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="96633-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="96633-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="96633-107">TRUE</span></span>  <br/> | <span data-ttu-id="96633-108">Breite ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="96633-108">Width is locked.</span></span>  <br/> |
| <span data-ttu-id="96633-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="96633-109">FALSE</span></span>  <br/> | <span data-ttu-id="96633-110">Breite ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="96633-110">Width is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="96633-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="96633-111">Remarks</span></span>

<span data-ttu-id="96633-112">Wenn Sie einen Verweis auf die Zelle Zelle LockWidth aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="96633-112">To get a reference to the LockWidth cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="96633-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="96633-113">Cell name:</span></span>  <br/> | <span data-ttu-id="96633-114">Zelle LockWidth</span><span class="sxs-lookup"><span data-stu-id="96633-114">LockWidth</span></span>  <br/> |
   
<span data-ttu-id="96633-115">Wenn Sie einen Verweis auf die Zelle Zelle LockWidth aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="96633-115">To get a reference to the LockWidth cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="96633-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="96633-116">Section index:</span></span>  <br/> |<span data-ttu-id="96633-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="96633-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="96633-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="96633-118">Row index:</span></span>  <br/> |<span data-ttu-id="96633-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="96633-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="96633-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="96633-120">Cell index:</span></span>  <br/> |<span data-ttu-id="96633-121">**visLockWidth**</span><span class="sxs-lookup"><span data-stu-id="96633-121">**visLockWidth**</span></span> <br/> |
   

