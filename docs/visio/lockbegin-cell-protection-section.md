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
ms.openlocfilehash: c9b9a0e9b69de9b76d78ca7cebfb69116bd2fb72
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797359"
---
# <a name="lockbegin-cell-protection-section"></a><span data-ttu-id="5ce36-103">LockBegin Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="5ce36-103">LockBegin Cell (Protection Section)</span></span>

<span data-ttu-id="5ce36-104">Sperrt den Anfangspunkt (AnfangX, AnfangY) eines 1D-Shapes an einer bestimmten Position.</span><span class="sxs-lookup"><span data-stu-id="5ce36-104">Locks the begin point (BeginX, BeginY) of a 1-D shape to a specific location.</span></span>
  
|<span data-ttu-id="5ce36-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5ce36-105">**Value**</span></span>|<span data-ttu-id="5ce36-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5ce36-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="5ce36-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="5ce36-107">TRUE</span></span>  <br/> | <span data-ttu-id="5ce36-108">Anfangspunkt ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5ce36-108">Begin point is locked.</span></span>  <br/> |
| <span data-ttu-id="5ce36-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="5ce36-109">FALSE</span></span>  <br/> | <span data-ttu-id="5ce36-110">Anfang ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="5ce36-110">Begin is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5ce36-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ce36-111">Remarks</span></span>

<span data-ttu-id="5ce36-112">Wenn Sie einen Verweis auf die Zelle LockBegin aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="5ce36-112">To get a reference to the LockBegin cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ce36-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="5ce36-113">Cell name:</span></span>  <br/> | <span data-ttu-id="5ce36-114">LockBegin</span><span class="sxs-lookup"><span data-stu-id="5ce36-114">LockBegin</span></span>  <br/> |
   
<span data-ttu-id="5ce36-115">Wenn Sie einen Verweis auf die Zelle LockBegin aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="5ce36-115">To get a reference to the LockBegin cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="5ce36-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="5ce36-116">Section index:</span></span>  <br/> |<span data-ttu-id="5ce36-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="5ce36-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="5ce36-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="5ce36-118">Row index:</span></span>  <br/> |<span data-ttu-id="5ce36-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="5ce36-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="5ce36-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="5ce36-120">Cell index:</span></span>  <br/> |<span data-ttu-id="5ce36-121">**visLockBegin**</span><span class="sxs-lookup"><span data-stu-id="5ce36-121">**visLockBegin**</span></span> <br/> |
   

