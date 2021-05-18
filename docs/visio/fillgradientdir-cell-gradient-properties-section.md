---
title: Zelle "FillGradientDir" (Abschnitt "Gradient Properties")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: e8156ff1-c540-44b8-8b69-ba4d54883260
description: Bestimmt die Richtung des Füllverlaufs. Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.
ms.openlocfilehash: 53aad056c7fc1674e00e142fd72a10134103b390
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406717"
---
# <a name="fillgradientdir-cell-gradient-properties-section"></a><span data-ttu-id="9cf36-104">Zelle "FillGradientDir" (Abschnitt "Gradient Properties")</span><span class="sxs-lookup"><span data-stu-id="9cf36-104">FillGradientDir Cell (Gradient Properties Section)</span></span>

<span data-ttu-id="9cf36-105">Bestimmt die Richtung des Füllverlaufs.</span><span class="sxs-lookup"><span data-stu-id="9cf36-105">Determines the direction of the fill gradient.</span></span> <span data-ttu-id="9cf36-106">Ein Farbverlauf kann linear, radial, rechteckig oder einem Pfad folgen.</span><span class="sxs-lookup"><span data-stu-id="9cf36-106">A gradient can be linear, radial, rectangular, or follow a path.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9cf36-107">Ein linearer Farbverlauf ist der einzige Farbverlauf, der einen zusätzlichen Winkelwert benötigt (wie durch die **FillGradientDir-Zelle** bestimmt).</span><span class="sxs-lookup"><span data-stu-id="9cf36-107">A linear gradient is the only gradient that takes an additional angle value (as determined by **FillGradientDir** cell).</span></span> <span data-ttu-id="9cf36-108">Alle anderen Verlaufsrichtungen verfügen über vordefinierte Enumerationen.</span><span class="sxs-lookup"><span data-stu-id="9cf36-108">All other gradient directions have preset enumerations.</span></span> 
  
****

|<span data-ttu-id="9cf36-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9cf36-109">**Value**</span></span>|<span data-ttu-id="9cf36-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9cf36-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9cf36-111">0</span><span class="sxs-lookup"><span data-stu-id="9cf36-111">0</span></span>  <br/> |<span data-ttu-id="9cf36-112">Linearer Farbverlauf.</span><span class="sxs-lookup"><span data-stu-id="9cf36-112">Linear gradient.</span></span> <span data-ttu-id="9cf36-113">Die **Zelle FillGradientAngle** bestimmt die Richtung des Farbverlaufs.</span><span class="sxs-lookup"><span data-stu-id="9cf36-113">The **FillGradientAngle** cell determines the direction of the gradient.</span></span>  <br/> |
|<span data-ttu-id="9cf36-114">1-7</span><span class="sxs-lookup"><span data-stu-id="9cf36-114">1-7</span></span>  <br/> |<span data-ttu-id="9cf36-115">Radiale Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="9cf36-115">Radial gradients.</span></span> <span data-ttu-id="9cf36-116">Der Farbverlauf erstreckt sich von einem zentralen Punkt aus nach außen in einem Kreis.</span><span class="sxs-lookup"><span data-stu-id="9cf36-116">The gradient extends outwards in a circle from a central point.</span></span>  <br/> |
|<span data-ttu-id="9cf36-117">8-12</span><span class="sxs-lookup"><span data-stu-id="9cf36-117">8-12</span></span>  <br/> |<span data-ttu-id="9cf36-118">Rechteckige Farbverläufe.</span><span class="sxs-lookup"><span data-stu-id="9cf36-118">Rectangular gradients.</span></span> <span data-ttu-id="9cf36-119">Der Farbverlauf erstreckt sich als richtungsförmige Linie von einem Ursprung mit einer rechteckigen Ausblendung.</span><span class="sxs-lookup"><span data-stu-id="9cf36-119">The gradient extends as a directional line from an origin with a rectangular-shaped fade.</span></span>  <br/> |
|<span data-ttu-id="9cf36-120">13</span><span class="sxs-lookup"><span data-stu-id="9cf36-120">13</span></span>  <br/> |<span data-ttu-id="9cf36-121">Pfadverlauf.</span><span class="sxs-lookup"><span data-stu-id="9cf36-121">Path gradient.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9cf36-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9cf36-122">Remarks</span></span>

<span data-ttu-id="9cf36-123">Verwenden Sie zum Erhalten eines Verweises auf die **FillGradientDir-Zelle** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="9cf36-123">To get a reference to the **FillGradientDir** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cf36-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9cf36-124">Cell name:</span></span>  <br/> | <span data-ttu-id="9cf36-125">FillGradientDir</span><span class="sxs-lookup"><span data-stu-id="9cf36-125">FillGradientDir</span></span>  <br/> |
   
<span data-ttu-id="9cf36-126">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **FillGradientDir-Zelle** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="9cf36-126">To get a reference to the **FillGradientDir** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="9cf36-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9cf36-127">Section index:</span></span>  <br/> |<span data-ttu-id="9cf36-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9cf36-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="9cf36-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9cf36-129">Row index:</span></span>  <br/> |<span data-ttu-id="9cf36-130">**visRowGradientProperties**</span><span class="sxs-lookup"><span data-stu-id="9cf36-130">**visRowGradientProperties**</span></span> <br/> |
| <span data-ttu-id="9cf36-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9cf36-131">Cell index:</span></span>  <br/> |<span data-ttu-id="9cf36-132">**visFillGradientDir**</span><span class="sxs-lookup"><span data-stu-id="9cf36-132">**visFillGradientDir**</span></span> <br/> |
   

