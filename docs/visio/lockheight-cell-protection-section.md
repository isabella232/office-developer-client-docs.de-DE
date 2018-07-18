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
ms.openlocfilehash: f6afe6037ff3d0810cc532bbc18bb749ee589bb1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797383"
---
# <a name="lockheight-cell-protection-section"></a><span data-ttu-id="2e563-103">LockHeight Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="2e563-103">LockHeight Cell (Protection Section)</span></span>

<span data-ttu-id="2e563-104">Sperrt die Höhe des Shapes, sodass sich diese nicht ändert, wenn die Größe des Shapes geändert wird.</span><span class="sxs-lookup"><span data-stu-id="2e563-104">Locks the height of the shape so that its height remains unchanged when the shape is resized.</span></span>
  
|<span data-ttu-id="2e563-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2e563-105">**Value**</span></span>|<span data-ttu-id="2e563-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2e563-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2e563-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="2e563-107">TRUE</span></span>  <br/> | <span data-ttu-id="2e563-108">Höhe ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2e563-108">Height is locked.</span></span>  <br/> |
| <span data-ttu-id="2e563-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="2e563-109">FALSE</span></span>  <br/> | <span data-ttu-id="2e563-110">Höhe ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="2e563-110">Height is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2e563-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2e563-111">Remarks</span></span>

<span data-ttu-id="2e563-112">Wenn Sie einen Verweis auf die Zelle LockHeight aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2e563-112">To get a reference to the LockHeight cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e563-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2e563-113">Cell name:</span></span>  <br/> | <span data-ttu-id="2e563-114">LockHeight</span><span class="sxs-lookup"><span data-stu-id="2e563-114">LockHeight</span></span>  <br/> |
   
<span data-ttu-id="2e563-115">Wenn Sie einen Verweis auf die Zelle LockHeight aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2e563-115">To get a reference to the LockHeight cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2e563-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2e563-116">Section index:</span></span>  <br/> |<span data-ttu-id="2e563-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2e563-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2e563-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2e563-118">Row index:</span></span>  <br/> |<span data-ttu-id="2e563-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="2e563-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="2e563-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2e563-120">Cell index:</span></span>  <br/> |<span data-ttu-id="2e563-121">**visLockHeight**</span><span class="sxs-lookup"><span data-stu-id="2e563-121">**visLockHeight**</span></span> <br/> |
   

