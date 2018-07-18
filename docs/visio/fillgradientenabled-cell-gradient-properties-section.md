---
title: FillGradientEnabled Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 80db9c0c-13c6-47de-967f-ade6e5899f14
description: Bestimmt, ob für dieses Shape ein Farbverlauf aktiviert ist.
ms.openlocfilehash: 20a38d4c45af163bc00364a45dc31269bf97251f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797012"
---
# <a name="fillgradientenabled-cell-gradient-properties-section"></a><span data-ttu-id="95360-103">FillGradientEnabled Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="95360-103">FillGradientEnabled Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="95360-104">Bestimmt, ob für dieses Shape ein Farbverlauf aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="95360-104">Determines whether a fill gradient is enabled for this shape.</span></span> 
  
|<span data-ttu-id="95360-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="95360-105">**Value**</span></span>|<span data-ttu-id="95360-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="95360-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="95360-107">TRUE</span><span class="sxs-lookup"><span data-stu-id="95360-107">TRUE</span></span>  <br/> |<span data-ttu-id="95360-108">Graduelle Füllung wird auf dem Shape angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95360-108">Gradient fill is displayed on the shape.</span></span>  <br/> |
|<span data-ttu-id="95360-109">FALSE</span><span class="sxs-lookup"><span data-stu-id="95360-109">FALSE</span></span>  <br/> |<span data-ttu-id="95360-110">Gradientenfüllungen werden nicht auf dem Shape angezeigt.</span><span class="sxs-lookup"><span data-stu-id="95360-110">Gradient fills are not displayed on the shape.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="95360-111">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="95360-111">Remarks</span></span>

<span data-ttu-id="95360-112">Wenn Sie einen Verweis auf die Zelle **FillGradientEnabled** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="95360-112">To get a reference to the **FillGradientEnabled** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95360-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="95360-113">Cell name:</span></span>  <br/> | <span data-ttu-id="95360-114">FillGradientEnabled</span><span class="sxs-lookup"><span data-stu-id="95360-114">FillGradientEnabled</span></span>  <br/> |
   
<span data-ttu-id="95360-115">Wenn Sie einen Verweis auf die Zelle **FillGradientEnabled** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="95360-115">To get a reference to the **FillGradientEnabled** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="95360-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="95360-116">Section index:</span></span>  <br/> |<span data-ttu-id="95360-117">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="95360-117">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="95360-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="95360-118">Row index:</span></span>  <br/> |<span data-ttu-id="95360-119">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="95360-119">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="95360-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="95360-120">Cell index:</span></span>  <br/> |<span data-ttu-id="95360-121">** VisFillGradientEnabled **</span><span class="sxs-lookup"><span data-stu-id="95360-121">**visFillGradientEnabled **</span></span> <br/> |
   

