---
title: SketchAmount Cell (Additional Effect Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Bestimmt die Menge des Distortion für einen Effekt Skizze als ganze Zahl zwischen 0 und 25.
ms.openlocfilehash: d5ae954f2eab48722c48c9bc4b3f640403dbb3ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798125"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="9ddf4-103">SketchAmount Cell (Additional Effect Properties Section)</span><span class="sxs-lookup"><span data-stu-id="9ddf4-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="9ddf4-104">Bestimmt die Menge des Distortion für einen Effekt Skizze als ganze Zahl zwischen 0 und 25.</span><span class="sxs-lookup"><span data-stu-id="9ddf4-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="9ddf4-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9ddf4-105">**Value**</span></span>|<span data-ttu-id="9ddf4-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ddf4-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9ddf4-107">0</span><span class="sxs-lookup"><span data-stu-id="9ddf4-107">0</span></span>  <br/> |<span data-ttu-id="9ddf4-108">Das Shape ist wirkungslos Skizze angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="9ddf4-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="9ddf4-109">1-25</span><span class="sxs-lookup"><span data-stu-id="9ddf4-109">1-25</span></span>  <br/> |<span data-ttu-id="9ddf4-110">Die Form angewendet wird, wobei die meisten Distortion, wird ein Wert von 1 und 25 Skizze Distortion hat die geringste.</span><span class="sxs-lookup"><span data-stu-id="9ddf4-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ddf4-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="9ddf4-111">Remarks</span></span>

<span data-ttu-id="9ddf4-112">Wenn Sie einen Verweis auf die Zelle **SketchAmount** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="9ddf4-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ddf4-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9ddf4-113">Cell name:</span></span>  <br/> | <span data-ttu-id="9ddf4-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="9ddf4-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="9ddf4-115">Wenn Sie einen Verweis auf die Zelle **SketchAmount** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9ddf4-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9ddf4-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9ddf4-116">Section index:</span></span>  <br/> |<span data-ttu-id="9ddf4-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9ddf4-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9ddf4-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9ddf4-118">Row index:</span></span>  <br/> |<span data-ttu-id="9ddf4-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="9ddf4-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="9ddf4-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9ddf4-120">Cell index:</span></span>  <br/> |<span data-ttu-id="9ddf4-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="9ddf4-121">**visSketchAmount**</span></span> <br/> |
   

