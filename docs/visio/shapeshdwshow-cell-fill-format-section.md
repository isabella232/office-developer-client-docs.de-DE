---
title: ShapeShdwShow Cell (Fill Format section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Bestimmt, ob die Form einen Schatten anzeigt, als ganze Zahl zwischen 0 und 2.
ms.openlocfilehash: 1da52c20acaa19eab79970a751fad2c225e212ae
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32349147"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="79137-103">ShapeShdwShow Cell (Fill Format section)</span><span class="sxs-lookup"><span data-stu-id="79137-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="79137-104">Bestimmt, ob die Form einen Schatten anzeigt, als ganze Zahl zwischen 0 und 2.</span><span class="sxs-lookup"><span data-stu-id="79137-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="79137-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="79137-105">**Value**</span></span>|<span data-ttu-id="79137-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="79137-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="79137-107">0</span><span class="sxs-lookup"><span data-stu-id="79137-107">0</span></span>  <br/> |<span data-ttu-id="79137-108">Der Schatten wird immer angezeigt, wenn ein Schatten angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="79137-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="79137-109">Die Schatten für unter Formen werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79137-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="79137-110">1</span><span class="sxs-lookup"><span data-stu-id="79137-110">1</span></span>  <br/> |<span data-ttu-id="79137-111">Rendern Sie keinen Schatten, es sei denn, das Shape hat kein übergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="79137-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="79137-112">Verwenden Sie subshape-Schatten, wenn Sie gruppiert werden.</span><span class="sxs-lookup"><span data-stu-id="79137-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="79137-113">2</span><span class="sxs-lookup"><span data-stu-id="79137-113">2</span></span>  <br/> |<span data-ttu-id="79137-114">Wenn ein Schatten angegeben wird, wird immer ein Schatten angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79137-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="79137-115">Die Schatten für unter Formen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="79137-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="79137-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="79137-116">Remarks</span></span>

<span data-ttu-id="79137-117">Wenn Sie einen Verweis auf die Zelle **ShapeShdwShow** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="79137-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="79137-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="79137-118">Cell name:</span></span>  <br/> | <span data-ttu-id="79137-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="79137-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="79137-120">Wenn Sie einen Verweis auf die Zelle **ShapeShdwShow** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="79137-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="79137-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="79137-121">Section index:</span></span>  <br/> |<span data-ttu-id="79137-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="79137-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="79137-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="79137-123">Row index:</span></span>  <br/> |<span data-ttu-id="79137-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="79137-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="79137-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="79137-125">Cell index:</span></span>  <br/> |<span data-ttu-id="79137-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="79137-126">**visFillShdwShow**</span></span> <br/> |
   

