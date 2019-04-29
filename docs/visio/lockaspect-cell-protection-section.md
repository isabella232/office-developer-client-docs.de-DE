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
ms.openlocfilehash: 83ce1aaf555cfaaa0109423e74ae930450b4c1e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411582"
---
# <a name="lockaspect-cell-protection-section"></a><span data-ttu-id="6a183-103">Zelle "LockAspect" (Abschnitt "Protection")</span><span class="sxs-lookup"><span data-stu-id="6a183-103">LockAspect Cell (Protection Section)</span></span>

<span data-ttu-id="6a183-104">Sperrt das Seitenverhältnis des Shapes, sodass die Größe des Shapes nur proportional geändert werden kann. Die Größe kann nicht in einer einzelnen Dimension geändert werden.</span><span class="sxs-lookup"><span data-stu-id="6a183-104">Locks the aspect ratio of the shape so that the shape can only be sized proportionally; it cannot be sized in a single dimension.</span></span>
  
|<span data-ttu-id="6a183-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6a183-105">**Value**</span></span>|<span data-ttu-id="6a183-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6a183-106">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="6a183-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="6a183-107">TRUE</span></span>  <br/> | <span data-ttu-id="6a183-108">Seitenverhältnis ist gesperrt.</span><span class="sxs-lookup"><span data-stu-id="6a183-108">Aspect ratio is locked.</span></span>  <br/> |
| <span data-ttu-id="6a183-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="6a183-109">FALSE</span></span>  <br/> | <span data-ttu-id="6a183-110">Seitenverhältnis ist nicht gesperrt.</span><span class="sxs-lookup"><span data-stu-id="6a183-110">Aspect ratio is not locked.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6a183-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6a183-111">Remarks</span></span>

<span data-ttu-id="6a183-112">Wenn Sie einen Verweis auf die Zelle Zelle LockAspect aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6a183-112">To get a reference to the LockAspect cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a183-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6a183-113">Cell name:</span></span>  <br/> | <span data-ttu-id="6a183-114">Zelle LockAspect</span><span class="sxs-lookup"><span data-stu-id="6a183-114">LockAspect</span></span>  <br/> |
   
<span data-ttu-id="6a183-115">Wenn Sie einen Verweis auf die Zelle Zelle LockAspect aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6a183-115">To get a reference to the LockAspect cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6a183-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6a183-116">Section index:</span></span>  <br/> |<span data-ttu-id="6a183-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6a183-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6a183-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6a183-118">Row index:</span></span>  <br/> |<span data-ttu-id="6a183-119">**visRowLock**</span><span class="sxs-lookup"><span data-stu-id="6a183-119">**visRowLock**</span></span> <br/> |
| <span data-ttu-id="6a183-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6a183-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6a183-121">**visLockAspect**</span><span class="sxs-lookup"><span data-stu-id="6a183-121">**visLockAspect**</span></span> <br/> |
   

