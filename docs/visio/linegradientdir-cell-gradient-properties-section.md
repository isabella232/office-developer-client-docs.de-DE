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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417987"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="d71d7-104">Zelle "LineGradientDir" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="d71d7-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="d71d7-105">Bestimmt die Richtung des Linien Verlaufs.</span><span class="sxs-lookup"><span data-stu-id="d71d7-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="d71d7-106">Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.</span><span class="sxs-lookup"><span data-stu-id="d71d7-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="d71d7-107">Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert (gemäß der **LineGradientDir** -Zelle) verwendet.</span><span class="sxs-lookup"><span data-stu-id="d71d7-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="d71d7-108">Alle anderen graduellen Richtungen haben vordefinierte Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="d71d7-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="d71d7-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="d71d7-109">**Value**</span></span>|<span data-ttu-id="d71d7-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d71d7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="d71d7-111">0</span><span class="sxs-lookup"><span data-stu-id="d71d7-111">0</span></span>  <br/> |<span data-ttu-id="d71d7-112">Linearer Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="d71d7-112">Linear gradient.</span></span> <span data-ttu-id="d71d7-113">Die **LineGradientAngle** -Zelle bestimmt die Richtung des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="d71d7-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="d71d7-114">1-7</span><span class="sxs-lookup"><span data-stu-id="d71d7-114">1-7</span></span>  <br/> |<span data-ttu-id="d71d7-115">Radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="d71d7-115">Radial gradients.</span></span> <span data-ttu-id="d71d7-116">Der Farbverlauf erstreckt sich von einem zentralen Punkt aus in einem Kreis.</span><span class="sxs-lookup"><span data-stu-id="d71d7-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="d71d7-117">8-12</span><span class="sxs-lookup"><span data-stu-id="d71d7-117">8-12</span></span>  <br/> |<span data-ttu-id="d71d7-118">Rechteckige Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="d71d7-118">Rectangular gradients.</span></span> <span data-ttu-id="d71d7-119">Der Farbverlauf erstreckt sich als richtungsachse von einem Ursprung mit einem rechteckigen verblassen.</span><span class="sxs-lookup"><span data-stu-id="d71d7-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="d71d7-120">13 </span><span class="sxs-lookup"><span data-stu-id="d71d7-120">13</span></span>  <br/> |<span data-ttu-id="d71d7-121">Pfad Gradient.</span><span class="sxs-lookup"><span data-stu-id="d71d7-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d71d7-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d71d7-122">Remarks</span></span>

<span data-ttu-id="d71d7-123">Wenn Sie einen Verweis auf die Zelle **LineGradientDir** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d71d7-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d71d7-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="d71d7-124">Cell name:</span></span>  <br/> | <span data-ttu-id="d71d7-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="d71d7-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="d71d7-126">Wenn Sie einen Verweis auf die Zelle **LineGradientDir** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="d71d7-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="d71d7-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="d71d7-127">Section index:</span></span>  <br/> |<span data-ttu-id="d71d7-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="d71d7-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="d71d7-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="d71d7-129">Row index:</span></span>  <br/> |<span data-ttu-id="d71d7-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="d71d7-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="d71d7-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="d71d7-131">Cell index:</span></span>  <br/> |<span data-ttu-id="d71d7-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="d71d7-132">**visLineGradientDir**</span></span> <br/> |
   

