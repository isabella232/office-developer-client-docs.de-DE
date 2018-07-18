---
title: LineGradientDir Cell (Gradient Properties Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Bestimmt die Richtung des Farbverlaufs Linie. Ein Farbverlauf kann linear, radial, rechteckigen verwendet werden, oder führen Sie einen Pfad.
ms.openlocfilehash: 6243d7a6b470db0915ba6fc462f05b72a9814f66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797335"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="393c2-104">LineGradientDir Cell (Gradient Properties Section)</span><span class="sxs-lookup"><span data-stu-id="393c2-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="393c2-105">Bestimmt die Richtung des Farbverlaufs Linie.</span><span class="sxs-lookup"><span data-stu-id="393c2-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="393c2-106">Ein Farbverlauf kann linear, radial, rechteckigen verwendet werden, oder führen Sie einen Pfad.</span><span class="sxs-lookup"><span data-stu-id="393c2-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="393c2-107">Ein linearer Farbverlauf ist die einzige Farbverlauf, der einen zusätzliche Angle-Wert (wie durch **LineGradientDir** Zelle festgelegt) akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="393c2-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="393c2-108">Alle anderen Farbverlauf Richtungen Voreinstellung Aufzählungen enthalten.</span><span class="sxs-lookup"><span data-stu-id="393c2-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="393c2-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="393c2-109">**Value**</span></span>|<span data-ttu-id="393c2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="393c2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="393c2-111">0</span><span class="sxs-lookup"><span data-stu-id="393c2-111">0</span></span>  <br/> |<span data-ttu-id="393c2-112">Linearer Farbverlauf</span><span class="sxs-lookup"><span data-stu-id="393c2-112">Linear gradient.</span></span> <span data-ttu-id="393c2-113">Die Zelle **LineGradientAngle** bestimmt die Richtung des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="393c2-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="393c2-114">1 bis 7</span><span class="sxs-lookup"><span data-stu-id="393c2-114">1-7</span></span>  <br/> |<span data-ttu-id="393c2-115">Radial Verläufe.</span><span class="sxs-lookup"><span data-stu-id="393c2-115">Radial gradients.</span></span> <span data-ttu-id="393c2-116">In einem Kreis erweitert von einem zentralen Punkt nach außen des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="393c2-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="393c2-117">8 bis 12</span><span class="sxs-lookup"><span data-stu-id="393c2-117">8-12</span></span>  <br/> |<span data-ttu-id="393c2-118">Rechteckige Verläufe.</span><span class="sxs-lookup"><span data-stu-id="393c2-118">Rectangular gradients.</span></span> <span data-ttu-id="393c2-119">Der Farbverlauf erweitert als Richtungspfeile Linie vom Ursprung mit einem rechteckigen einblenden.</span><span class="sxs-lookup"><span data-stu-id="393c2-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="393c2-120">13</span><span class="sxs-lookup"><span data-stu-id="393c2-120">13</span></span>  <br/> |<span data-ttu-id="393c2-121">Pfadfarbverlauf.</span><span class="sxs-lookup"><span data-stu-id="393c2-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="393c2-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="393c2-122">Remarks</span></span>

<span data-ttu-id="393c2-123">Wenn Sie einen Verweis auf die Zelle **LineGradientDir** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="393c2-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="393c2-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="393c2-124">Cell name:</span></span>  <br/> | <span data-ttu-id="393c2-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="393c2-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="393c2-126">Wenn Sie einen Verweis auf die Zelle **LineGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="393c2-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="393c2-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="393c2-127">Section index:</span></span>  <br/> |<span data-ttu-id="393c2-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="393c2-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="393c2-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="393c2-129">Row index:</span></span>  <br/> |<span data-ttu-id="393c2-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="393c2-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="393c2-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="393c2-131">Cell index:</span></span>  <br/> |<span data-ttu-id="393c2-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="393c2-132">**visLineGradientDir**</span></span> <br/> |
   

