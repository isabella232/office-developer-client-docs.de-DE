---
title: Zelle "LockHeight" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm635
localization_priority: Normal
ms.assetid: 218b957e-5af6-e53b-1453-a84164ae456e
description: Sperrt die Höhe des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.
ms.openlocfilehash: 099f6597656d4389476818253f34e741ddd404de
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432086"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="432a2-103">Zelle "LockHeight" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="432a2-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="432a2-104">Sperrt die Höhe des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="432a2-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="432a2-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="432a2-105">**Value**</span></span>|<span data-ttu-id="432a2-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="432a2-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="432a2-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="432a2-107">TRUE</span></span>  <br/> | <span data-ttu-id="432a2-108">Höhe ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="432a2-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="432a2-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="432a2-109">FALSE</span></span>  <br/> | <span data-ttu-id="432a2-110">Höhe ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="432a2-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="432a2-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="432a2-111">Remarks</span></span>

<span data-ttu-id="432a2-112">Um einen Verweis auf die Zelle LockHeight anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="432a2-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="432a2-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="432a2-113">Cell name:</span></span>  <br/> | <span data-ttu-id="432a2-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="432a2-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="432a2-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle LockHeight nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="432a2-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="432a2-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="432a2-116">Section index:</span></span>  <br/> |<span data-ttu-id="432a2-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="432a2-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="432a2-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="432a2-118">Row index:</span></span>  <br/> |<span data-ttu-id="432a2-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="432a2-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="432a2-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="432a2-120">Cell index:</span></span>  <br/> |<span data-ttu-id="432a2-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="432a2-121">**visLockHeight**</span></span> <br/> |
   

