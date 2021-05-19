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
description: Legt fest, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Shapes mithilfe des Dialogfelds Layout konfigurieren ausgerichtet werden.
ms.openlocfilehash: 7a607fdb53ad569e84976b6f9911fbd89f7f2628
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425729"
---
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="9ac06-103">Zelle "ObjType" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="9ac06-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="9ac06-104">Legt fest, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Shapes mithilfe des Dialogfelds **Layout konfigurieren** ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="9ac06-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="9ac06-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9ac06-105">**Value**</span></span>|<span data-ttu-id="9ac06-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9ac06-106">**Description**</span></span>|<span data-ttu-id="9ac06-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="9ac06-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9ac06-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="9ac06-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="9ac06-p101">Standardeinstellung. Die Anwendung entscheidet diesen Punkt abhängig vom Zeichnungskontext.</span><span class="sxs-lookup"><span data-stu-id="9ac06-p101">Default. The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="9ac06-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="9ac06-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="9ac06-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="9ac06-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="9ac06-113">Shape ist platzierbar.</span><span class="sxs-lookup"><span data-stu-id="9ac06-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="9ac06-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="9ac06-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="9ac06-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="9ac06-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="9ac06-p102">Shape ist umleitbar. Es muss sich jedoch um ein eindimensionales Shape (1D-Shape) handeln.</span><span class="sxs-lookup"><span data-stu-id="9ac06-p102">Shape is routable. Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="9ac06-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="9ac06-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="9ac06-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="9ac06-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="9ac06-120">Shape ist weder platzierbar noch umleitbar.</span><span class="sxs-lookup"><span data-stu-id="9ac06-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="9ac06-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="9ac06-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="9ac06-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="9ac06-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="9ac06-123">Gruppe enthält platzierbare oder umleitbare Shapes.</span><span class="sxs-lookup"><span data-stu-id="9ac06-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="9ac06-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="9ac06-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9ac06-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9ac06-125">Remarks</span></span>

<span data-ttu-id="9ac06-126">Standardmäßig ist die Zelle ObjType auf Keine Formel für eine Form festgelegt, die auf 0 ausgewertet wird, was bedeutet, dass die Anwendung bestimmt, ob das Shape je nach Kontext platzierbar sein kann.</span><span class="sxs-lookup"><span data-stu-id="9ac06-126">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context.</span></span> <span data-ttu-id="9ac06-127">Wenn Sie beispielsweise ein einfaches Rechteck zeichnen, ist der Wert der Zelle ObjType 0.</span><span class="sxs-lookup"><span data-stu-id="9ac06-127">For example, if you draw a simple rectangle, the value of its ObjType cell is 0.</span></span> <span data-ttu-id="9ac06-128">Wenn Sie dann  das Connector-Tool verwenden, um das Rechteck mit einer anderen Form zu verbinden, setzt Visio den Wert der Zelle ObjType des Rechtecks auf 1 (platzierbar) zurück.</span><span class="sxs-lookup"><span data-stu-id="9ac06-128">If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="9ac06-129">Der Wert der Zelle ObjType kann eine Kombination aus mehreren verschiedenen Werten sein.</span><span class="sxs-lookup"><span data-stu-id="9ac06-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="9ac06-130">Wenn das nicht platzierbare Bit festgelegt ist ( H4), hat es jedoch Vorrang vor anderen Werten mit Ausnahme des &amp; Gruppenwerts ( &amp; H8).</span><span class="sxs-lookup"><span data-stu-id="9ac06-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="9ac06-131">Um einen Verweis auf die Zelle ObjType anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="9ac06-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ac06-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9ac06-132">Cell name:</span></span>  <br/> |<span data-ttu-id="9ac06-133">ObjType</span><span class="sxs-lookup"><span data-stu-id="9ac06-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="9ac06-134">Um einen Verweis auf die Zelle ObjType nach Index aus einem Programm zu erhalten, verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="9ac06-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9ac06-135">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9ac06-135">Section index:</span></span>  <br/> |<span data-ttu-id="9ac06-136">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="9ac06-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="9ac06-137">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9ac06-137">Row index:</span></span>  <br/> |<span data-ttu-id="9ac06-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="9ac06-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="9ac06-139">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9ac06-139">Cell index:</span></span>  <br/> |<span data-ttu-id="9ac06-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="9ac06-140">**visLOFlags**</span></span> <br/> |
   

