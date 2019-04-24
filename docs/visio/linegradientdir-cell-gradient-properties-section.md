---
title: Zelle "LineGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Bestimmt die Richtung des Linien Verlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350960"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="702ed-104">Zelle "LineGradientDir" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="702ed-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="702ed-105">Bestimmt die Richtung des Linien Verlaufs.</span><span class="sxs-lookup"><span data-stu-id="702ed-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="702ed-106">Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.</span><span class="sxs-lookup"><span data-stu-id="702ed-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="702ed-107">Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert (gemäß der **LineGradientDir** -Zelle) verwendet.</span><span class="sxs-lookup"><span data-stu-id="702ed-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="702ed-108">Alle anderen graduellen Richtungen haben vordefinierte Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="702ed-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="702ed-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="702ed-109">**Value**</span></span>|<span data-ttu-id="702ed-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="702ed-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="702ed-111">0</span><span class="sxs-lookup"><span data-stu-id="702ed-111">0</span></span>  <br/> |<span data-ttu-id="702ed-112">Linearer Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="702ed-112">Linear gradient.</span></span> <span data-ttu-id="702ed-113">Die **LineGradientAngle** -Zelle bestimmt die Richtung des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="702ed-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="702ed-114">1-7</span><span class="sxs-lookup"><span data-stu-id="702ed-114">1-7</span></span>  <br/> |<span data-ttu-id="702ed-115">Radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="702ed-115">Radial gradients.</span></span> <span data-ttu-id="702ed-116">Der Farbverlauf erstreckt sich von einem zentralen Punkt aus in einem Kreis.</span><span class="sxs-lookup"><span data-stu-id="702ed-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="702ed-117">8-12</span><span class="sxs-lookup"><span data-stu-id="702ed-117">8-12</span></span>  <br/> |<span data-ttu-id="702ed-118">Rechteckige Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="702ed-118">Rectangular gradients.</span></span> <span data-ttu-id="702ed-119">Der Farbverlauf erstreckt sich als richtungsachse von einem Ursprung mit einem rechteckigen verblassen.</span><span class="sxs-lookup"><span data-stu-id="702ed-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="702ed-120">13</span><span class="sxs-lookup"><span data-stu-id="702ed-120">13</span></span>  <br/> |<span data-ttu-id="702ed-121">Pfad Gradient.</span><span class="sxs-lookup"><span data-stu-id="702ed-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="702ed-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="702ed-122">Remarks</span></span>

<span data-ttu-id="702ed-123">Wenn Sie einen Verweis auf die Zelle **LineGradientDir** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="702ed-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="702ed-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="702ed-124">Cell name:</span></span>  <br/> | <span data-ttu-id="702ed-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="702ed-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="702ed-126">Wenn Sie einen Verweis auf die Zelle **LineGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="702ed-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="702ed-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="702ed-127">Section index:</span></span>  <br/> |<span data-ttu-id="702ed-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="702ed-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="702ed-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="702ed-129">Row index:</span></span>  <br/> |<span data-ttu-id="702ed-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="702ed-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="702ed-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="702ed-131">Cell index:</span></span>  <br/> |<span data-ttu-id="702ed-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="702ed-132">**visLineGradientDir**</span></span> <br/> |
   

