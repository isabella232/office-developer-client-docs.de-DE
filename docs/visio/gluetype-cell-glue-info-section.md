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
ms.openlocfilehash: 162827521cda6fe4a37d17a8f7d36d7a36718519
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797104"
---
# <a name="gluetype-cell-glue-info-section"></a><span data-ttu-id="6c14c-103">GlueType Cell (Glue Info Section)</span><span class="sxs-lookup"><span data-stu-id="6c14c-103">GlueType Cell (Glue Info Section)</span></span>

<span data-ttu-id="6c14c-104">Bestimmt, ob ein 1D-Shape statischen (Punkt-zu-Punkt) oder dynamischen (Shape-zu-Shape) Kleber verwendet, wenn es an ein anderes Shape geklebt wird.</span><span class="sxs-lookup"><span data-stu-id="6c14c-104">Determines whether a 1-D shape uses static (point-to-point) or dynamic (shape-to-shape) glue when it is glued to another shape.</span></span>
  
|<span data-ttu-id="6c14c-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="6c14c-105">**Value**</span></span>|<span data-ttu-id="6c14c-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="6c14c-106">**Description**</span></span>|<span data-ttu-id="6c14c-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="6c14c-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="6c14c-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="6c14c-108">&amp;H0</span></span>  <br/> | <span data-ttu-id="6c14c-p101">Standardeinstellung. Dynamischen Kleber nur für dynamische Verbinder zulassen, sonst statischen Kleber verwenden.</span><span class="sxs-lookup"><span data-stu-id="6c14c-p101">Default. Allow dynamic glue for the dynamic connector only; otherwise, use static glue.</span></span>  <br/> |<span data-ttu-id="6c14c-111">**visGlueTypeDefault**</span><span class="sxs-lookup"><span data-stu-id="6c14c-111">**visGlueTypeDefault**</span></span> <br/> |
| <span data-ttu-id="6c14c-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="6c14c-112">&amp;H1</span></span>  <br/> | <span data-ttu-id="6c14c-113">Dynamischen Kleber zulassen.</span><span class="sxs-lookup"><span data-stu-id="6c14c-113">Allow dynamic glue.</span></span>  <br/> | <span data-ttu-id="6c14c-114">Wird ab Visio 2002 nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c14c-114">Obsolete in Visio 2002</span></span>  <br/> |
| <span data-ttu-id="6c14c-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="6c14c-115">&amp;H2</span></span>  <br/> | <span data-ttu-id="6c14c-116">Dynamischen Kleber zulassen.</span><span class="sxs-lookup"><span data-stu-id="6c14c-116">Allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="6c14c-117">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="6c14c-117">**visGlueTypeWalking**</span></span> <br/> |
| <span data-ttu-id="6c14c-118">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="6c14c-118">&amp;H4</span></span>  <br/> | <span data-ttu-id="6c14c-119">Dynamischen Kleber nicht zulassen.</span><span class="sxs-lookup"><span data-stu-id="6c14c-119">Do not allow dynamic glue.</span></span>  <br/> |<span data-ttu-id="6c14c-120">**visGlueTypeNoWalking**</span><span class="sxs-lookup"><span data-stu-id="6c14c-120">**visGlueTypeNoWalking**</span></span> <br/> |
| <span data-ttu-id="6c14c-121">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="6c14c-121">&amp;H8</span></span>  <br/> | <span data-ttu-id="6c14c-122">Dieses 2D-Shape darf nicht mit dynamischem Kleber verbunden werden.</span><span class="sxs-lookup"><span data-stu-id="6c14c-122">Do not allow this 2-D shape to be connected to with dynamic glue.</span></span>  <br/> |<span data-ttu-id="6c14c-123">**visGlueTypeNoWalkingTo**</span><span class="sxs-lookup"><span data-stu-id="6c14c-123">**visGlueTypeNoWalkingTo**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6c14c-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6c14c-124">Remarks</span></span>

<span data-ttu-id="6c14c-125">Wenn diese Zelle den Wert 1, 2 oder 3 enthält, wird dynamischer Kleber verwendet, wenn eine der folgenden Bedingungen vorliegt:</span><span class="sxs-lookup"><span data-stu-id="6c14c-125">If this cell contains a value of 1, 2 or 3, dynamic glue will be established when either of the following occurs:</span></span>
  
- <span data-ttu-id="6c14c-126">Shapes werden auf der Benutzeroberfläche dynamisch verklebt.</span><span class="sxs-lookup"><span data-stu-id="6c14c-126">Shapes are dynamically glued in the user interface.</span></span>
    
- <span data-ttu-id="6c14c-127">Shapes werden an die Zelle PinX oder PinY eines anderen Shapes aus einem Programm geklebt.</span><span class="sxs-lookup"><span data-stu-id="6c14c-127">Shapes are glued to the PinX or PinY cell of another shape from a program.</span></span>
    
<span data-ttu-id="6c14c-128">Wenn Shapes von einem Programm an Shape-Zellen außer PinX oder PinY geklebt werden, wird statischer Kleber verwendet.</span><span class="sxs-lookup"><span data-stu-id="6c14c-128">If shapes are glued to shape cells other than PinX or PinY from a program, then static glue is used.</span></span>
  
<span data-ttu-id="6c14c-p102">Wenn Sie diesen Wert ändern, sodass dynamisches Kleben nicht mehr zulässig ist, werden bereits vorhandene dynamisch geklebte Verbindungen weder getrennt noch verändert. Programme können dynamischen Kleber verwenden, auch wenn das dynamische Kleben in der Zelle GlueType deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="6c14c-p102">Changing this value from allowing to not allowing dynamic glue does not sever or change existing dynamic glue. Programs can establish dynamic glue even if dynamic glue is disabled in the GlueType cell.</span></span>
  
<span data-ttu-id="6c14c-131">Wenn Sie einen Verweis auf die Zelle GlueType aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6c14c-131">To get a reference to the GlueType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c14c-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="6c14c-132">Cell name:</span></span>  <br/> | <span data-ttu-id="6c14c-133">GlueType</span><span class="sxs-lookup"><span data-stu-id="6c14c-133">GlueType</span></span>  <br/> |
   
<span data-ttu-id="6c14c-134">Wenn Sie einen Verweis auf die Zelle GlueType aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="6c14c-134">To get a reference to the GlueType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="6c14c-135">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="6c14c-135">Section index:</span></span>  <br/> |<span data-ttu-id="6c14c-136">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="6c14c-136">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="6c14c-137">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="6c14c-137">Row index:</span></span>  <br/> |<span data-ttu-id="6c14c-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="6c14c-138">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="6c14c-139">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="6c14c-139">Cell index:</span></span>  <br/> |<span data-ttu-id="6c14c-140">**visGlueType**</span><span class="sxs-lookup"><span data-stu-id="6c14c-140">**visGlueType**</span></span> <br/> |
   

