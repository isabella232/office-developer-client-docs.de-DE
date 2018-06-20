---
title: Zelle "ObjType" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm745
localization_priority: Normal
ms.assetid: 3afee07b-e91a-a91c-fba2-0e3251dd6385
description: Bestimmt, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Sie das Dialogfeld Layout konfigurieren zum Ausrichten von Shapes verwenden.
ms.openlocfilehash: 23887e1d265e9e5ac1dfa9750bab65e8428b1c76
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797572"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="75c28-103">ObjType Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="75c28-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="75c28-104">Bestimmt, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Sie das Dialogfeld **Layout konfigurieren** zum Ausrichten von Shapes verwenden.</span><span class="sxs-lookup"><span data-stu-id="75c28-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="75c28-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="75c28-105">**Value**</span></span>|<span data-ttu-id="75c28-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75c28-106">**Description**</span></span>|<span data-ttu-id="75c28-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="75c28-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="75c28-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="75c28-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="75c28-p101">Standardeinstellung. Die Anwendung entscheidet diesen Punkt abhängig vom Zeichnungskontext.</span><span class="sxs-lookup"><span data-stu-id="75c28-p101">Default. The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="75c28-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="75c28-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="75c28-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="75c28-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="75c28-113">Shape ist platzierbar.</span><span class="sxs-lookup"><span data-stu-id="75c28-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="75c28-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="75c28-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="75c28-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="75c28-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="75c28-p102">Shape ist umleitbar. Es muss sich jedoch um ein eindimensionales Shape (1D-Shape) handeln.</span><span class="sxs-lookup"><span data-stu-id="75c28-p102">Shape is routable. Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="75c28-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="75c28-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="75c28-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="75c28-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="75c28-120">Shape ist weder platzierbar noch umleitbar.</span><span class="sxs-lookup"><span data-stu-id="75c28-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="75c28-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="75c28-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="75c28-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="75c28-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="75c28-123">Gruppe enthält platzierbare oder umleitbare Shapes.</span><span class="sxs-lookup"><span data-stu-id="75c28-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="75c28-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="75c28-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75c28-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="75c28-125">Remarks</span></span>

<span data-ttu-id="75c28-126">Standardmäßig wird die Zelle ObjType festgelegt, No Formula für ein Shape, 0, was bedeutet, dass die Anwendung bestimmt, ob das Shape in Abhängigkeit von seinem Kontext platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="75c28-126">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context.</span></span> <span data-ttu-id="75c28-127">Wenn Sie ein einfaches Rechteck zeichnen, ist der Wert der Zelle ObjType beispielsweise 0.</span><span class="sxs-lookup"><span data-stu-id="75c28-127">For example, if you draw a simple rectangle, the value of its ObjType cell is 0.</span></span> <span data-ttu-id="75c28-128">Wenn Sie für die Verbindung des Rechtecks an ein anderes Shape klicken Sie dann das **Verbinder** -Tool verwenden, setzt Visio den Wert des Rechtecks ObjType Zelle auf 1 (platzierbare).</span><span class="sxs-lookup"><span data-stu-id="75c28-128">If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="75c28-129">Der Wert der Zelle ObjType kann eine Kombination von Werten sein.</span><span class="sxs-lookup"><span data-stu-id="75c28-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="75c28-130">Wenn das nicht platzierbare Bit festgelegt ist (&amp;H4), jedoch, er hat Vorrang vor anderen Werten mit Ausnahme der Gruppenwert (&amp;H8).</span><span class="sxs-lookup"><span data-stu-id="75c28-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="75c28-131">Wenn Sie einen Verweis auf die Zelle ObjType nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="75c28-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75c28-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="75c28-132">Cell name:</span></span>  <br/> |<span data-ttu-id="75c28-133">ObjType</span><span class="sxs-lookup"><span data-stu-id="75c28-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="75c28-134">Wenn Sie einen Verweis auf die Zelle ObjType aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="75c28-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="75c28-135">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="75c28-135">Section index:</span></span>  <br/> |<span data-ttu-id="75c28-136">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="75c28-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="75c28-137">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="75c28-137">Row index:</span></span>  <br/> |<span data-ttu-id="75c28-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="75c28-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="75c28-139">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="75c28-139">Cell index:</span></span>  <br/> |<span data-ttu-id="75c28-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="75c28-140">**visLOFlags**</span></span> <br/> |
   

