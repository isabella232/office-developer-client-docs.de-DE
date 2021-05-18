---
title: Zelle "SketchAmount" (Abschnitt "Additional Effect Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 7c7353b7-f28e-4004-bf13-6e9714fbed37
description: Bestimmt den Umfang der Verzerrung für einen Skizziereffekt als ganze Zahl zwischen 0 und 25.
ms.openlocfilehash: fd9ee3390d05f24d81d9c6677160155b0f0f0d35
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404421"
---
# <a name="sketchamount-cell-additional-effect-properties-section"></a><span data-ttu-id="4d805-103">Zelle "SketchAmount" (Abschnitt "Additional Effect Properties")</span><span class="sxs-lookup"><span data-stu-id="4d805-103">SketchAmount Cell (Additional Effect Properties Section)</span></span>

<span data-ttu-id="4d805-104">Bestimmt den Umfang der Verzerrung für einen Skizziereffekt als ganze Zahl zwischen 0 und 25.</span><span class="sxs-lookup"><span data-stu-id="4d805-104">Determines the amount of distortion for a sketch effect, as an integer between 0 and 25.</span></span> 
  
|<span data-ttu-id="4d805-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4d805-105">**Value**</span></span>|<span data-ttu-id="4d805-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d805-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d805-107">0</span><span class="sxs-lookup"><span data-stu-id="4d805-107">0</span></span>  <br/> |<span data-ttu-id="4d805-108">Die Form hat keinen Skizzeseffekt, der auf sie angewendet wird.</span><span class="sxs-lookup"><span data-stu-id="4d805-108">The shape has no sketch effect applied to it.</span></span>  <br/> |
|<span data-ttu-id="4d805-109">1-25</span><span class="sxs-lookup"><span data-stu-id="4d805-109">1-25</span></span>  <br/> |<span data-ttu-id="4d805-110">Auf die Form wurde eine Zierzeichnung angewendet, wobei der Wert 1 die größte Verzerrung und 25 die geringste Verzerrung ist.</span><span class="sxs-lookup"><span data-stu-id="4d805-110">The shape has sketch distortion applied to it, where a value of 1 is the most distortion and 25 is the least.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d805-111">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4d805-111">Remarks</span></span>

<span data-ttu-id="4d805-112">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle SketchAmount** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="4d805-112">To get a reference to the **SketchAmount** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d805-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4d805-113">Cell name:</span></span>  <br/> | <span data-ttu-id="4d805-114">SketchAmount</span><span class="sxs-lookup"><span data-stu-id="4d805-114">SketchAmount</span></span>  <br/> |
   
<span data-ttu-id="4d805-115">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle SketchAmount** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="4d805-115">To get a reference to the **SketchAmount** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d805-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4d805-116">Section index:</span></span>  <br/> |<span data-ttu-id="4d805-117">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4d805-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4d805-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4d805-118">Row index:</span></span>  <br/> |<span data-ttu-id="4d805-119">**visRowOtherEffectProperties**</span><span class="sxs-lookup"><span data-stu-id="4d805-119">**visRowOtherEffectProperties**</span></span> <br/> |
| <span data-ttu-id="4d805-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4d805-120">Cell index:</span></span>  <br/> |<span data-ttu-id="4d805-121">**visSketchAmount**</span><span class="sxs-lookup"><span data-stu-id="4d805-121">**visSketchAmount**</span></span> <br/> |
   

