---
title: Zelle "FillGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Bestimmt die Richtung des Füll Verlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322463"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="10a3f-104">Zelle "FillGradientDir" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="10a3f-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="10a3f-105">Bestimmt die Richtung des Füll Verlaufs.</span><span class="sxs-lookup"><span data-stu-id="10a3f-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="10a3f-106">Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.</span><span class="sxs-lookup"><span data-stu-id="10a3f-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="10a3f-107">Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert (gemäß der **FillGradientDir** -Zelle) verwendet.</span><span class="sxs-lookup"><span data-stu-id="10a3f-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="10a3f-108">Alle anderen graduellen Richtungen haben vordefinierte Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="10a3f-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="10a3f-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="10a3f-109">**Value**</span></span>|<span data-ttu-id="10a3f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="10a3f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="10a3f-111">0</span><span class="sxs-lookup"><span data-stu-id="10a3f-111">0</span></span>  <br/> |<span data-ttu-id="10a3f-112">Linearer Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="10a3f-112">Linear gradient.</span></span> <span data-ttu-id="10a3f-113">Die **FillGradientAngle** -Zelle bestimmt die Richtung des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="10a3f-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="10a3f-114">1-7</span><span class="sxs-lookup"><span data-stu-id="10a3f-114">1-7</span></span>  <br/> |<span data-ttu-id="10a3f-115">Radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="10a3f-115">Radial gradients.</span></span> <span data-ttu-id="10a3f-116">Der Farbverlauf erstreckt sich von einem zentralen Punkt aus in einem Kreis.</span><span class="sxs-lookup"><span data-stu-id="10a3f-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="10a3f-117">8-12</span><span class="sxs-lookup"><span data-stu-id="10a3f-117">8-12</span></span>  <br/> |<span data-ttu-id="10a3f-118">Rechteckige Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="10a3f-118">Rectangular gradients.</span></span> <span data-ttu-id="10a3f-119">Der Farbverlauf erstreckt sich als richtungsachse von einem Ursprung mit einem rechteckigen verblassen.</span><span class="sxs-lookup"><span data-stu-id="10a3f-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="10a3f-120">13</span><span class="sxs-lookup"><span data-stu-id="10a3f-120">13</span></span>  <br/> |<span data-ttu-id="10a3f-121">Pfad Gradient.</span><span class="sxs-lookup"><span data-stu-id="10a3f-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="10a3f-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="10a3f-122">Remarks</span></span>

<span data-ttu-id="10a3f-123">Wenn Sie einen Verweis auf die Zelle **FillGradientDir** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="10a3f-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10a3f-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="10a3f-124">Cell name:</span></span>  <br/> | <span data-ttu-id="10a3f-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="10a3f-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="10a3f-126">Wenn Sie einen Verweis auf die Zelle **FillGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="10a3f-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="10a3f-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="10a3f-127">Section index:</span></span>  <br/> |<span data-ttu-id="10a3f-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="10a3f-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="10a3f-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="10a3f-129">Row index:</span></span>  <br/> |<span data-ttu-id="10a3f-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="10a3f-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="10a3f-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="10a3f-131">Cell index:</span></span>  <br/> |<span data-ttu-id="10a3f-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="10a3f-132">**visFillGradientDir**</span></span> <br/> |
   

