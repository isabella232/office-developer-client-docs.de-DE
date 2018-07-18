---
title: ShapeShdwShow Cell (Fill Format Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ece6c889-9291-40ea-b55a-072acdcb8a52
description: Bestimmt, ob das Shape als eine ganze Zahl zwischen 0 und 2 einen Schatten angezeigt wird.
ms.openlocfilehash: 72077e60089acd3cd3f8a9349691e1468f6b1f9c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798044"
---
# <a name="shapeshdwshow-cell-fill-format-section"></a><span data-ttu-id="bd7cb-103">ShapeShdwShow Cell (Fill Format Section)</span><span class="sxs-lookup"><span data-stu-id="bd7cb-103">ShapeShdwShow Cell (Fill Format Section)</span></span>

<span data-ttu-id="bd7cb-104">Bestimmt, ob das Shape als eine ganze Zahl zwischen 0 und 2 einen Schatten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="bd7cb-104">Determines whether the shape displays a shadow, as an integer from 0 to 2.</span></span>
  
|<span data-ttu-id="bd7cb-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="bd7cb-105">**Value**</span></span>|<span data-ttu-id="bd7cb-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="bd7cb-106">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bd7cb-107">0</span><span class="sxs-lookup"><span data-stu-id="bd7cb-107">0</span></span>  <br/> |<span data-ttu-id="bd7cb-108">Den Schatten immer angezeigt, wenn Sie ein Schatten angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bd7cb-108">Always display the shadow if a shadow is specified.</span></span> <span data-ttu-id="bd7cb-109">Schatten für untergeordneten Shapes werden nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd7cb-109">The shadows for sub-shapes are not displayed.</span></span>  <br/> |
|<span data-ttu-id="bd7cb-110">1</span><span class="sxs-lookup"><span data-stu-id="bd7cb-110">1</span></span>  <br/> |<span data-ttu-id="bd7cb-111">Einen Schatten werden nicht gerendert werden, es sei denn, das Shape nicht über ein übergeordnetes Element verfügt.</span><span class="sxs-lookup"><span data-stu-id="bd7cb-111">Do not render a shadow unless the shape does not have a parent.</span></span> <span data-ttu-id="bd7cb-112">Verwenden Sie untergeordnetes Shape-Kontrollpunkte, wenn zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="bd7cb-112">Use sub-shape shadows if grouped together.</span></span>  <br/> |
|<span data-ttu-id="bd7cb-113">2</span><span class="sxs-lookup"><span data-stu-id="bd7cb-113">2</span></span>  <br/> |<span data-ttu-id="bd7cb-114">Einen Schatten immer angezeigt, wenn Sie ein Schatten angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="bd7cb-114">Always display a shadow if a shadow is specified.</span></span> <span data-ttu-id="bd7cb-115">Schatten für die untergeordneten Formen werden angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bd7cb-115">The shadows for sub-shapes are displayed.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bd7cb-116">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="bd7cb-116">Remarks</span></span>

<span data-ttu-id="bd7cb-117">Wenn Sie einen Verweis auf die Zelle **ShapeShdwShow** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="bd7cb-117">To get a reference to the **ShapeShdwShow** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd7cb-118">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="bd7cb-118">Cell name:</span></span>  <br/> | <span data-ttu-id="bd7cb-119">ShapeShdwShow</span><span class="sxs-lookup"><span data-stu-id="bd7cb-119">ShapeShdwShow</span></span>  <br/> |
   
<span data-ttu-id="bd7cb-120">Wenn Sie einen Verweis auf die Zelle **ShapeShdwShow** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="bd7cb-120">To get a reference to the **ShapeShdwShow** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="bd7cb-121">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="bd7cb-121">Section index:</span></span>  <br/> |<span data-ttu-id="bd7cb-122">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="bd7cb-122">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="bd7cb-123">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="bd7cb-123">Row index:</span></span>  <br/> |<span data-ttu-id="bd7cb-124">**visRowFill**</span><span class="sxs-lookup"><span data-stu-id="bd7cb-124">**visRowFill**</span></span> <br/> |
| <span data-ttu-id="bd7cb-125">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="bd7cb-125">Cell index:</span></span>  <br/> |<span data-ttu-id="bd7cb-126">**visFillShdwShow**</span><span class="sxs-lookup"><span data-stu-id="bd7cb-126">**visFillShdwShow**</span></span> <br/> |
   

