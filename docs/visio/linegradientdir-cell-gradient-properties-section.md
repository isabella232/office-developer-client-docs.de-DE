---
title: Zelle "LineGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c603f9a5-f887-47ce-90bb-d41ec2d1a6a1
description: Bestimmt die Richtung des Linienverlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 05dcc6904a4e67d97c632dba44635936b1c14049
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417987"
---
# <a name="linegradientdir-cell-gradient-properties-section"></a><span data-ttu-id="e8424-104">Zelle "LineGradientDir" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="e8424-104">LineGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="e8424-105">Bestimmt die Richtung des Linienverlaufs.</span><span class="sxs-lookup"><span data-stu-id="e8424-105">Determines the direction of the line gradient.</span></span> <span data-ttu-id="e8424-106">Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.</span><span class="sxs-lookup"><span data-stu-id="e8424-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e8424-107">Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert benötigt (wie durch die **LineGradientDir-Zelle** bestimmt).</span><span class="sxs-lookup"><span data-stu-id="e8424-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **LineGradientDir** cell).</span></span> <span data-ttu-id="e8424-108">Alle anderen Verlaufsrichtungen verfügen über vordefinierte Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="e8424-108">All other gradient directions have preset enumerations.</span></span> 
  
|<span data-ttu-id="e8424-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="e8424-109">**Value**</span></span>|<span data-ttu-id="e8424-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e8424-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e8424-111">0</span><span class="sxs-lookup"><span data-stu-id="e8424-111">0</span></span>  <br/> |<span data-ttu-id="e8424-112">Linearer Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="e8424-112">Linear gradient.</span></span> <span data-ttu-id="e8424-113">Die **Zelle LineGradientAngle** bestimmt die Richtung des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="e8424-113">The **LineGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="e8424-114">1-7</span><span class="sxs-lookup"><span data-stu-id="e8424-114">1-7</span></span>  <br/> |<span data-ttu-id="e8424-115">Radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="e8424-115">Radial gradients.</span></span> <span data-ttu-id="e8424-116">Der Farbverlauf erstreckt sich von einem zentralen Punkt aus nach außen in einem Kreis.</span><span class="sxs-lookup"><span data-stu-id="e8424-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="e8424-117">8-12</span><span class="sxs-lookup"><span data-stu-id="e8424-117">8-12</span></span>  <br/> |<span data-ttu-id="e8424-118">Rechteckige Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="e8424-118">Rectangular gradients.</span></span> <span data-ttu-id="e8424-119">Der Farbverlauf erstreckt sich als richtungsförmige Linie von einem Ursprung mit einer rechteckigen Ausblendung.</span><span class="sxs-lookup"><span data-stu-id="e8424-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="e8424-120">13</span><span class="sxs-lookup"><span data-stu-id="e8424-120">13</span></span>  <br/> |<span data-ttu-id="e8424-121">Pfadverlauf.</span><span class="sxs-lookup"><span data-stu-id="e8424-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e8424-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e8424-122">Remarks</span></span>

<span data-ttu-id="e8424-123">Verwenden Sie zum Erhalten eines Verweises auf die **Zelle LineGradientDir** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="e8424-123">To get a reference to the **LineGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8424-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e8424-124">Cell name:</span></span>  <br/> | <span data-ttu-id="e8424-125">LineGradientDir</span><span class="sxs-lookup"><span data-stu-id="e8424-125">LineGradientDir</span></span>  <br/> |
   
<span data-ttu-id="e8424-126">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **LineGradientDir-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="e8424-126">To get a reference to the **LineGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="e8424-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e8424-127">Section index:</span></span>  <br/> |<span data-ttu-id="e8424-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="e8424-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="e8424-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e8424-129">Row index:</span></span>  <br/> |<span data-ttu-id="e8424-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="e8424-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="e8424-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e8424-131">Cell index:</span></span>  <br/> |<span data-ttu-id="e8424-132">**visLineGradientDir**</span><span class="sxs-lookup"><span data-stu-id="e8424-132">**visLineGradientDir**</span></span> <br/> |
   

