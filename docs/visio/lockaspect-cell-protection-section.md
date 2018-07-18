---
title: Zelle "LockAspect" (Abschnitt "Protection")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251218
localization_priority: Normal
ms.assetid: e9bfced5-af29-f86c-8604-44ec9a573229
description: Sperrt das Seitenverhältnis des Shapes, sodass die Größe des Shapes nur proportional geändert werden kann. Die Größe kann nicht in einer einzelnen Dimension geändert werden.
ms.openlocfilehash: fb5736add65f548f06697077bc539ec7fac5feb2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797370"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="3be0c-103">LockAspect Cell (Protection Section)</span><span class="sxs-lookup"><span data-stu-id="3be0c-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="3be0c-104">Sperrt das Seitenverhältnis des Shapes, sodass die Größe des Shapes nur proportional geändert werden kann. Die Größe kann nicht in einer einzelnen Dimension geändert werden.</span><span class="sxs-lookup"><span data-stu-id="3be0c-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="3be0c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="3be0c-105">**Value**</span></span>|<span data-ttu-id="3be0c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3be0c-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="3be0c-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="3be0c-107">TRUE</span></span>  <br/> | <span data-ttu-id="3be0c-108">Seitenverhältnis ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="3be0c-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="3be0c-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="3be0c-109">FALSE</span></span>  <br/> | <span data-ttu-id="3be0c-110">Seitenverhältnis ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="3be0c-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3be0c-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3be0c-111">Remarks</span></span>

<span data-ttu-id="3be0c-112">Wenn Sie einen Verweis auf die Zelle LockAspect aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3be0c-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3be0c-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="3be0c-113">Cell name:</span></span>  <br/> | <span data-ttu-id="3be0c-114">LockAspect</span><span class="sxs-lookup"><span data-stu-id="3be0c-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="3be0c-115">Wenn Sie einen Verweis auf die Zelle LockAspect aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="3be0c-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="3be0c-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="3be0c-116">Section index:</span></span>  <br/> |<span data-ttu-id="3be0c-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="3be0c-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="3be0c-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="3be0c-118">Row index:</span></span>  <br/> |<span data-ttu-id="3be0c-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="3be0c-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="3be0c-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="3be0c-120">Cell index:</span></span>  <br/> |<span data-ttu-id="3be0c-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="3be0c-121">**visLockAspect**</span></span> <br/> |
   

