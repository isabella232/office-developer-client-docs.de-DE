---
title: SketchAmount Cell (Additional Effect Properties section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Bestimmt die Verzerrung für einen skizzeneffekt als ganze Zahl zwischen 0 und 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32314770"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="6f597-103">SketchAmount Cell (Additional Effect Properties section)</span><span class="sxs-lookup"><span data-stu-id="6f597-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="6f597-104">Bestimmt die Verzerrung für einen skizzeneffekt als ganze Zahl zwischen 0 und 25.</span><span class="sxs-lookup"><span data-stu-id="6f597-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="6f597-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6f597-105">**Value**</span></span>|<span data-ttu-id="6f597-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6f597-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="6f597-107">0</span><span class="sxs-lookup"><span data-stu-id="6f597-107">0</span></span>  <br/> |<span data-ttu-id="6f597-108">Auf die Form wurde kein skizzeneffekt angewendet.</span><span class="sxs-lookup"><span data-stu-id="6f597-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="6f597-109">1-25</span><span class="sxs-lookup"><span data-stu-id="6f597-109">1-25</span></span>  <br/> |<span data-ttu-id="6f597-110">Die Form hat eine Skizzen Verzerrung, die auf Sie angewendet wurde, wobei der Wert 1 die meisten Verzerrungen und 25 die geringste ist.</span><span class="sxs-lookup"><span data-stu-id="6f597-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6f597-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="6f597-111">Remarks</span></span>

<span data-ttu-id="6f597-112">Wenn Sie einen Verweis auf die Zelle **SketchAmount** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6f597-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f597-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6f597-113">Cell name:</span></span>  <br/> | <span data-ttu-id="6f597-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="6f597-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="6f597-115">Wenn Sie einen Verweis auf die Zelle **SketchAmount** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6f597-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6f597-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6f597-116">Section index:</span></span>  <br/> |<span data-ttu-id="6f597-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6f597-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6f597-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6f597-118">Row index:</span></span>  <br/> |<span data-ttu-id="6f597-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="6f597-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="6f597-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6f597-120">Cell index:</span></span>  <br/> |<span data-ttu-id="6f597-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="6f597-121">**visSketchAmount**</span></span> <br/> |
   

