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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341776"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="545e9-103">Zelle "LockHeight" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="545e9-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="545e9-104">Sperrt die Höhe des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="545e9-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="545e9-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="545e9-105">**Value**</span></span>|<span data-ttu-id="545e9-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="545e9-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="545e9-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="545e9-107">TRUE</span></span>  <br/> | <span data-ttu-id="545e9-108">Höhe ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="545e9-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="545e9-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="545e9-109">FALSE</span></span>  <br/> | <span data-ttu-id="545e9-110">Höhe ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="545e9-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="545e9-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="545e9-111">Remarks</span></span>

<span data-ttu-id="545e9-112">Wenn Sie einen Verweis auf die Zelle Zelle LockHeight aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="545e9-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="545e9-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="545e9-113">Cell name:</span></span>  <br/> | <span data-ttu-id="545e9-114">Zelle LockHeight</span><span class="sxs-lookup"><span data-stu-id="545e9-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="545e9-115">Wenn Sie einen Verweis auf die Zelle Zelle LockHeight aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="545e9-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="545e9-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="545e9-116">Section index:</span></span>  <br/> |<span data-ttu-id="545e9-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="545e9-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="545e9-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="545e9-118">Row index:</span></span>  <br/> |<span data-ttu-id="545e9-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="545e9-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="545e9-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="545e9-120">Cell index:</span></span>  <br/> |<span data-ttu-id="545e9-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="545e9-121">**visLockHeight**</span></span> <br/> |
   

