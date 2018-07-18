---
title: FillGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Bestimmt die Richtung des Farbverlaufs Füllung. Ein Farbverlauf kann linear, radial, rechteckigen verwendet werden, oder führen Sie einen Pfad.
ms.openlocfilehash: 9b4226892e70fcffe7a78d109bd852e6d4f93838
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796999"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="fcd60-104">FillGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="fcd60-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="fcd60-105">Bestimmt die Richtung des Farbverlaufs Füllung.</span><span class="sxs-lookup"><span data-stu-id="fcd60-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="fcd60-106">Ein Farbverlauf kann linear, radial, rechteckigen verwendet werden, oder führen Sie einen Pfad.</span><span class="sxs-lookup"><span data-stu-id="fcd60-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="fcd60-107">Ein linearer Farbverlauf ist die einzige Farbverlauf, der einen zusätzliche Angle-Wert (wie durch **FillGradientDir** Zelle festgelegt) akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="fcd60-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="fcd60-108">Alle anderen Farbverlauf Richtungen Voreinstellung Aufzählungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="fcd60-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="fcd60-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="fcd60-109">**Value**</span></span>|<span data-ttu-id="fcd60-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fcd60-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="fcd60-111">0</span><span class="sxs-lookup"><span data-stu-id="fcd60-111">0</span></span>  <br/> |<span data-ttu-id="fcd60-112">Linearer Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="fcd60-112">Linear gradient.</span></span> <span data-ttu-id="fcd60-113">Die Zelle **FillGradientAngle** bestimmt die Richtung des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="fcd60-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="fcd60-114">1 bis 7</span><span class="sxs-lookup"><span data-stu-id="fcd60-114">1-7</span></span>  <br/> |<span data-ttu-id="fcd60-115">Radial Verläufe.</span><span class="sxs-lookup"><span data-stu-id="fcd60-115">Radial gradients.</span></span> <span data-ttu-id="fcd60-116">In einem Kreis erweitert von einem zentralen Punkt nach außen des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="fcd60-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="fcd60-117">8 bis 12</span><span class="sxs-lookup"><span data-stu-id="fcd60-117">8-12</span></span>  <br/> |<span data-ttu-id="fcd60-118">Rechteckige Verläufe.</span><span class="sxs-lookup"><span data-stu-id="fcd60-118">Rectangular gradients.</span></span> <span data-ttu-id="fcd60-119">Der Farbverlauf erweitert als Richtungspfeile Linie vom Ursprung mit einem rechteckigen einblenden.</span><span class="sxs-lookup"><span data-stu-id="fcd60-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="fcd60-120">13</span><span class="sxs-lookup"><span data-stu-id="fcd60-120">13</span></span>  <br/> |<span data-ttu-id="fcd60-121">Pfadfarbverlauf.</span><span class="sxs-lookup"><span data-stu-id="fcd60-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fcd60-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fcd60-122">Remarks</span></span>

<span data-ttu-id="fcd60-123">Wenn Sie einen Verweis auf die Zelle **FillGradientDir** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fcd60-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fcd60-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="fcd60-124">Cell name:</span></span>  <br/> | <span data-ttu-id="fcd60-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="fcd60-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="fcd60-126">Wenn Sie einen Verweis auf die Zelle **FillGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="fcd60-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="fcd60-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="fcd60-127">Section index:</span></span>  <br/> |<span data-ttu-id="fcd60-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="fcd60-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="fcd60-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="fcd60-129">Row index:</span></span>  <br/> |<span data-ttu-id="fcd60-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="fcd60-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="fcd60-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="fcd60-131">Cell index:</span></span>  <br/> |<span data-ttu-id="fcd60-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="fcd60-132">**visFillGradientDir**</span></span> <br/> |
   

