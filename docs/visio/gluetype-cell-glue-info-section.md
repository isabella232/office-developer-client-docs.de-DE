---
title: Zelle "GlueType" (Abschnitt "Glue Info")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm420
localization_priority: Normal
ms.assetid: fffbefd6-8b0b-0023-6b03-026d1c6e885e
description: Bestimmt, ob ein 1D-Shape statischen (Punkt-zu-Punkt) oder dynamischen (Shape-zu-Shape) Kleber verwendet, wenn es an ein anderes Shape geklebt wird.
ms.openlocfilehash: ae4eddf17c6e7b5e56cb3397f03d0721d965c9b7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410672"
---
# <a name="gluetype-cell-glue-info-section"></a><span data-ttu-id="b311a-103">Zelle "GlueType" (Abschnitt "Glue Info")</span><span class="sxs-lookup"><span data-stu-id="b311a-103">GlueType Cell (Glue Info Section)</span></span>

<span data-ttu-id="b311a-104">Bestimmt, ob ein 1D-Shape statischen (Punkt-zu-Punkt) oder dynamischen (Shape-zu-Shape) Kleber verwendet, wenn es an ein anderes Shape geklebt wird.</span><span class="sxs-lookup"><span data-stu-id="b311a-104">Determines whether a 1-D shape uses static (point-to-point) or dynamic (shape-to-shape) glue when it is glued to another shape.</span></span>
  
|<span data-ttu-id="b311a-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b311a-105">**Value**</span></span>|<span data-ttu-id="b311a-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b311a-106">**Description**</span></span>|<span data-ttu-id="b311a-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="b311a-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b311a-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="b311a-108">&amp;H0</span></span>  <br/> | <span data-ttu-id="b311a-p101">Standardeinstellung. Dynamischen Kleber nur für dynamische Verbinder zulassen, sonst statischen Kleber verwenden.</span><span class="sxs-lookup"><span data-stu-id="b311a-p101">Default. Allow dynamic glue for the dynamic connector only; otherwise, use static glue.</span></span>  <br/> |<span data-ttu-id="b311a-111">**visGlueTypeDefault**</span><span class="sxs-lookup"><span data-stu-id="b311a-111">**visGlueTypeDefault**</span></span> <br/> |
| <span data-ttu-id="b311a-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="b311a-112">&amp;H1</span></span>  <br/> | <span data-ttu-id="b311a-113">Dynamischen Kleber zulassen.</span><span class="sxs-lookup"><span data-stu-id="b311a-113">Allow dynamic glue.</span></span>  <br/> | <span data-ttu-id="b311a-114">Wird ab Visio 2002 nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="b311a-114">Obsolete in Visio 2002</span></span>  <br/> |
| <span data-ttu-id="b311a-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="b311a-115">&amp;H2</span></span>  <br/> | <span data-ttu-id="b311a-116">Dynamischen Kleber zulassen.</span><span class="sxs-lookup"><span data-stu-id="b311a-116">Allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="b311a-117">**visGlueTypeWalking**</span><span class="sxs-lookup"><span data-stu-id="b311a-117">**visGlueTypeWalking**</span></span> <br/> |
| <span data-ttu-id="b311a-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="b311a-118">&amp;H4</span></span>  <br/> | <span data-ttu-id="b311a-119">Dynamischen Kleber nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="b311a-119">Do not allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="b311a-120">**visGlueTypeNoWalking**</span><span class="sxs-lookup"><span data-stu-id="b311a-120">**visGlueTypeNoWalking**</span></span> <br/> |
| <span data-ttu-id="b311a-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="b311a-121">&amp;H8</span></span>  <br/> | <span data-ttu-id="b311a-122">Dieses 2D-Shape darf nicht mit dynamischem Kleber verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="b311a-122">Do not allow this 2-D shape to be connected to with dynamic glue.</span></span>  <br/> |<span data-ttu-id="b311a-123">**visGlueTypeNoWalkingTo**</span><span class="sxs-lookup"><span data-stu-id="b311a-123">**visGlueTypeNoWalkingTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b311a-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b311a-124">Remarks</span></span>

<span data-ttu-id="b311a-125">Wenn diese Zelle den Wert 1, 2 oder 3 enthält, wird dynamischer Kleber verwendet, wenn eine der folgenden Bedingungen vorliegt:</span><span class="sxs-lookup"><span data-stu-id="b311a-125">If this cell contains a value of 1, 2 or 3, dynamic glue will be established when either of the following occurs:</span></span>
  
- <span data-ttu-id="b311a-126">Shapes werden auf der Benutzeroberfläche dynamisch verklebt.</span><span class="sxs-lookup"><span data-stu-id="b311a-126">Shapes are dynamically glued in the user interface.</span></span>
    
- <span data-ttu-id="b311a-127">Shapes werden an die Zelle PinX oder PinY eines anderen Shapes aus einem Programm geklebt.</span><span class="sxs-lookup"><span data-stu-id="b311a-127">Shapes are glued to the PinX or PinY cell of another shape from a program.</span></span>
    
<span data-ttu-id="b311a-128">Wenn Shapes von einem Programm an Shape-Zellen außer PinX oder PinY geklebt werden, wird statischer Kleber verwendet.</span><span class="sxs-lookup"><span data-stu-id="b311a-128">If shapes are glued to shape cells other than PinX or PinY from a program, then static glue is used.</span></span>
  
<span data-ttu-id="b311a-p102">Wenn Sie diesen Wert ändern, sodass dynamisches Kleben nicht mehr zulässig ist, werden bereits vorhandene dynamisch geklebte Verbindungen weder getrennt noch verändert. Programme können dynamischen Kleber verwenden, auch wenn das dynamische Kleben in der Zelle GlueType deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="b311a-p102">Changing this value from allowing to not allowing dynamic glue does not sever or change existing dynamic glue. Programs can establish dynamic glue even if dynamic glue is disabled in the GlueType cell.</span></span>
  
<span data-ttu-id="b311a-131">Um einen Verweis auf die Zelle GlueType anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="b311a-131">To get a reference to the GlueType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b311a-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b311a-132">Cell name:</span></span>  <br/> | <span data-ttu-id="b311a-133">GlueType</span><span class="sxs-lookup"><span data-stu-id="b311a-133">GlueType</span></span>  <br/> |
   
<span data-ttu-id="b311a-134">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle GlueType nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="b311a-134">To get a reference to the GlueType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b311a-135">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b311a-135">Section index:</span></span>  <br/> |<span data-ttu-id="b311a-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b311a-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b311a-137">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b311a-137">Row index:</span></span>  <br/> |<span data-ttu-id="b311a-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="b311a-138">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="b311a-139">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b311a-139">Cell index:</span></span>  <br/> |<span data-ttu-id="b311a-140">**visGlueType**</span><span class="sxs-lookup"><span data-stu-id="b311a-140">**visGlueType**</span></span> <br/> |
   

