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
# <a name="objtype-cell-miscellaneous-section"></a><span data-ttu-id="72456-103">Zelle "ObjType" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="72456-103">ObjType Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="72456-104">Legt fest, ob Objekte in Diagrammen platzierbar oder umleitbar sind, wenn Shapes mithilfe des Dialogfelds **Layout konfigurieren** ausgerichtet werden.</span><span class="sxs-lookup"><span data-stu-id="72456-104">Determines whether objects are placeable or routable in diagrams when you use the **Configure Layout** dialog box to lay out shapes.</span></span> 
  
|<span data-ttu-id="72456-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="72456-105">**Value**</span></span>|<span data-ttu-id="72456-106">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="72456-106">**Description**</span></span>|<span data-ttu-id="72456-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="72456-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72456-108">&amp;H0</span><span class="sxs-lookup"><span data-stu-id="72456-108">&amp;H0</span></span>  <br/> |<span data-ttu-id="72456-109">Standardwert.</span><span class="sxs-lookup"><span data-stu-id="72456-109">Default.</span></span> <span data-ttu-id="72456-110">Die Anwendung entscheidet diesen Punkt abhängig vom Zeichnungskontext.</span><span class="sxs-lookup"><span data-stu-id="72456-110">The application decides based on the drawing context.</span></span>  <br/> |<span data-ttu-id="72456-111">**visLOFlagsVisDecides**</span><span class="sxs-lookup"><span data-stu-id="72456-111">**visLOFlagsVisDecides**</span></span> <br/> |
|<span data-ttu-id="72456-112">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="72456-112">&amp;H1</span></span>  <br/> |<span data-ttu-id="72456-113">Shape ist platzierbar.</span><span class="sxs-lookup"><span data-stu-id="72456-113">Shape is placeable.</span></span>  <br/> |<span data-ttu-id="72456-114">**visLOFlagsPlacable**</span><span class="sxs-lookup"><span data-stu-id="72456-114">**visLOFlagsPlacable**</span></span> <br/> |
|<span data-ttu-id="72456-115">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="72456-115">&amp;H2</span></span>  <br/> |<span data-ttu-id="72456-116">Shape ist umleitbar.</span><span class="sxs-lookup"><span data-stu-id="72456-116">Shape is routable.</span></span> <span data-ttu-id="72456-117">Es muss sich jedoch um ein eindimensionales Shape (1D-Shape) handeln.</span><span class="sxs-lookup"><span data-stu-id="72456-117">Must be a one-dimensional (1-D) shape.</span></span>  <br/> |<span data-ttu-id="72456-118">**visLOFlagsRoutable**</span><span class="sxs-lookup"><span data-stu-id="72456-118">**visLOFlagsRoutable**</span></span> <br/> |
|<span data-ttu-id="72456-119">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="72456-119">&amp;H4</span></span>  <br/> |<span data-ttu-id="72456-120">Shape ist weder platzierbar noch umleitbar.</span><span class="sxs-lookup"><span data-stu-id="72456-120">Shape is not placeable, not routable.</span></span>  <br/> |<span data-ttu-id="72456-121">**visLOFlagsDont**</span><span class="sxs-lookup"><span data-stu-id="72456-121">**visLOFlagsDont**</span></span> <br/> |
|<span data-ttu-id="72456-122">&amp;H8</span><span class="sxs-lookup"><span data-stu-id="72456-122">&amp;H8</span></span>  <br/> |<span data-ttu-id="72456-123">Gruppe enthält platzierbare oder umleitbare Shapes.</span><span class="sxs-lookup"><span data-stu-id="72456-123">Group contains placeable/routable shapes.</span></span>  <br/> |<span data-ttu-id="72456-124">**visLOFlagsPNRGroup**</span><span class="sxs-lookup"><span data-stu-id="72456-124">**visLOFlagsPNRGroup**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="72456-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="72456-125">Remarks</span></span>

<span data-ttu-id="72456-126">Standardmäßig ist die Zelle ObjType-Zelle auf keine Formel für eine Form festgelegt, die auf 0 ausgewertet wird, was bedeutet, dass die Anwendung bestimmt, ob das Shape abhängig vom Kontext platziert werden kann.</span><span class="sxs-lookup"><span data-stu-id="72456-126">By default, the ObjType cell is set to No Formula for a shape, which evaluates to 0, meaning that the application determines whether the shape can be placeable depending on its context.</span></span> <span data-ttu-id="72456-127">Wenn Sie beispielsweise ein einfaches Rechteck zeichnen, ist der Wert der Zelle ObjType-Zelle 0.</span><span class="sxs-lookup"><span data-stu-id="72456-127">For example, if you draw a simple rectangle, the value of its ObjType cell is 0.</span></span> <span data-ttu-id="72456-128">Wenn Sie das Rechteck mit \*\*\*\* einem anderen Shape verbinden, setzt Visio den Wert der Zelle Zelle ObjType des Rechtecks auf 1 (placeable) zurück.</span><span class="sxs-lookup"><span data-stu-id="72456-128">If you then use the **Connector** tool to connect the rectangle to another shape, Visio resets the value of the rectangle's ObjType cell to 1 (placeable).</span></span> 
  
<span data-ttu-id="72456-129">Der Wert der Zelle ObjType kann eine Kombination aus mehreren verschiedenen Werten sein.</span><span class="sxs-lookup"><span data-stu-id="72456-129">The value of the ObjType cell can be a combination of values.</span></span> <span data-ttu-id="72456-130">Wenn das nicht platzierte Bit (&amp;H4) festgelegt ist, hat es Vorrang vor anderen Werten mit Ausnahme des Group-Werts (&amp;H8).</span><span class="sxs-lookup"><span data-stu-id="72456-130">If the non-placeable bit is set (&amp;H4), however, it takes precedence over other values except the group value (&amp;H8).</span></span>
  
<span data-ttu-id="72456-131">Wenn Sie einen Verweis auf die Zelle Zelle ObjType aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="72456-131">To get a reference to the ObjType cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72456-132">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="72456-132">Cell name:</span></span>  <br/> |<span data-ttu-id="72456-133">Zelle ObjType</span><span class="sxs-lookup"><span data-stu-id="72456-133">ObjType</span></span>  <br/> |
   
<span data-ttu-id="72456-134">Wenn Sie einen Verweis auf die Zelle Zelle ObjType aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="72456-134">To get a reference to the ObjType cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="72456-135">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="72456-135">Section index:</span></span>  <br/> |<span data-ttu-id="72456-136">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="72456-136">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="72456-137">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="72456-137">Row index:</span></span>  <br/> |<span data-ttu-id="72456-138">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="72456-138">**visRowMisc**</span></span> <br/> |
|<span data-ttu-id="72456-139">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="72456-139">Cell index:</span></span>  <br/> |<span data-ttu-id="72456-140">**visLOFlags**</span><span class="sxs-lookup"><span data-stu-id="72456-140">**visLOFlags**</span></span> <br/> |
   

