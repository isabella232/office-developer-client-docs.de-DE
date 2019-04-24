---
title: Zelle "ShapeFixedCode" (Abschnitt "Shape Layout")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm880
localization_priority: Normal
ms.assetid: a1736a5c-421c-2bdb-b164-76a8cd06cc3d
description: Definiert das Platzierungsverhalten für ein platzierbares Shape.
ms.openlocfilehash: eae44a0579129fbe8da1c0cc8c37318beb024563
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325732"
---
# <a name="shapefixedcode-cell-shape-layout-section"></a><span data-ttu-id="01f09-103">Zelle "ShapeFixedCode" (Abschnitt "Shape Layout")</span><span class="sxs-lookup"><span data-stu-id="01f09-103">ShapeFixedCode Cell (Shape Layout Section)</span></span>

<span data-ttu-id="01f09-104">Definiert das Platzierungsverhalten für ein platzierbares Shape.</span><span class="sxs-lookup"><span data-stu-id="01f09-104">Specifies placement behavior for a placeable shape.</span></span>
  
|<span data-ttu-id="01f09-105">**Wert**</span><span class="sxs-lookup"><span data-stu-id="01f09-105">**Value**</span></span>|<span data-ttu-id="01f09-106">**Auswahlmodus**</span><span class="sxs-lookup"><span data-stu-id="01f09-106">**Selection mode**</span></span>|<span data-ttu-id="01f09-107">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="01f09-107">**Automation constant**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="01f09-108">&amp;H1</span><span class="sxs-lookup"><span data-stu-id="01f09-108">&amp;H1</span></span>  <br/> |<span data-ttu-id="01f09-109">Verschieben Sie dieses Shape nicht, wenn Shapes mithilfe des Dialogfelds **Layout konfigurieren** festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="01f09-109">Don't move this shape when shapes are laid out by using the **Configure Layout** dialog box.</span></span>  <br/> |<span data-ttu-id="01f09-110">**visSLOFixedPlacement**</span><span class="sxs-lookup"><span data-stu-id="01f09-110">**visSLOFixedPlacement**</span></span> <br/> |
|<span data-ttu-id="01f09-111">&amp;H2</span><span class="sxs-lookup"><span data-stu-id="01f09-111">&amp;H2</span></span>  <br/> |<span data-ttu-id="01f09-112">Dieses Shape nicht verschieben und nicht zulassen, dass verschiebbare Shapes darüber platziert werden.</span><span class="sxs-lookup"><span data-stu-id="01f09-112">Don't move this shape and do not allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="01f09-113">**visSLOFixedPlow**</span><span class="sxs-lookup"><span data-stu-id="01f09-113">**visSLOFixedPlow**</span></span> <br/> |
|<span data-ttu-id="01f09-114">&amp;H4</span><span class="sxs-lookup"><span data-stu-id="01f09-114">&amp;H4</span></span>  <br/> |<span data-ttu-id="01f09-115">Dieses Shape nicht verschieben, aber zulassen, dass verschiebbare Shapes darüber platziert werden.</span><span class="sxs-lookup"><span data-stu-id="01f09-115">Don't move this shape and allow shapes that plow to be placed on top of it.</span></span>  <br/> |<span data-ttu-id="01f09-116">**visSLOFixedPermeablePlow**</span><span class="sxs-lookup"><span data-stu-id="01f09-116">**visSLOFixedPermeablePlow**</span></span> <br/> |
|<span data-ttu-id="01f09-117">&amp;H20 (32)</span><span class="sxs-lookup"><span data-stu-id="01f09-117">&amp;H20 (32)</span></span>  <br/> |<span data-ttu-id="01f09-118">Bei Weiterleitungen Verbindungspunktpositionen ignorieren.</span><span class="sxs-lookup"><span data-stu-id="01f09-118">Ignore connection point locations when being routed to.</span></span>  <br/> |<span data-ttu-id="01f09-119">**visSLOFixedConnPtsIgnore**</span><span class="sxs-lookup"><span data-stu-id="01f09-119">**visSLOFixedConnPtsIgnore**</span></span> <br/> |
|<span data-ttu-id="01f09-120">&amp;H40 (64)</span><span class="sxs-lookup"><span data-stu-id="01f09-120">&amp;H40 (64)</span></span>  <br/> |<span data-ttu-id="01f09-121">Nur die Weiterleitung zu Seiten mit Verbindungspunkten zulassen.</span><span class="sxs-lookup"><span data-stu-id="01f09-121">Only allow routing to sides with connection points.</span></span>  <br/> |<span data-ttu-id="01f09-122">**visSLOFixedConnPtsOnly**</span><span class="sxs-lookup"><span data-stu-id="01f09-122">**visSLOFixedConnPtsOnly**</span></span> <br/> |
|<span data-ttu-id="01f09-123">&amp;H80 (128)</span><span class="sxs-lookup"><span data-stu-id="01f09-123">&amp;H80 (128)</span></span>  <br/> |<span data-ttu-id="01f09-124">Keine Objekte an den Rand dieses Shapes kleben.</span><span class="sxs-lookup"><span data-stu-id="01f09-124">Don't glue to the perimeter of this shape.</span></span> <span data-ttu-id="01f09-125">Objekte stattdessen an das Ausrichtungsfeld des Shapes kleben.</span><span class="sxs-lookup"><span data-stu-id="01f09-125">Glue to the shape's alignment box instead.</span></span>  <br/> |<span data-ttu-id="01f09-126">**visSLOFixedNoFoldToShape**</span><span class="sxs-lookup"><span data-stu-id="01f09-126">**visSLOFixedNoFoldToShape**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="01f09-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01f09-127">Remarks</span></span>

<span data-ttu-id="01f09-128">Sie können den Wert dieser Zelle auch im Dialogfeld **Verhalten** auf der Registerkarte **Platzierung** festlegen (wenn ein Shape ausgewählt ist, klicken Sie auf der Registerkarte [Entwicklertools](run-in-developer-mode-display-the-developer-tab.md) in der Gruppe **Shape-Design** auf **Verhalten**, und klicken Sie dann auf die Registerkarte **Platzierung** ).</span><span class="sxs-lookup"><span data-stu-id="01f09-128">You can also set the value of this cell on the **Placement** tab in the **Behavior** dialog box (with a shape selected, on the [Developer](run-in-developer-mode-display-the-developer-tab.md) tab, in the **Shape Design** group, click **Behavior**, and then click the **Placement** tab).</span></span> 
  
<span data-ttu-id="01f09-129">Sie können für diese Zelle jede beliebige Kombination dieser Werte festlegen.</span><span class="sxs-lookup"><span data-stu-id="01f09-129">You can set any combination of these values for this cell.</span></span> <span data-ttu-id="01f09-130">Sie können beispielsweise den Wert 3&amp;(H3) eingeben, der beim Layout von Shapes mithilfe des Dialogfelds **Layout konfigurieren** (Klicken Sie auf der Registerkarte **Entwurf** in der Gruppe **Layout** auf **Seite neu Layout**), und klicken Sie dann auf \*\* Weitere Layoutoptionen\*\* ) und wenn andere Platzierungs Formen auf oder in der Nähe der Form platziert werden.</span><span class="sxs-lookup"><span data-stu-id="01f09-130">For example, you can enter the value 3 (&amp;H3), which eliminates movement when you lay out shapes by using the **Configure Layout** dialog box (on the **Design** tab, in the **Layout** group, click **Re-Layout Page**, and then click **More Layout Options** ) and when other placeable shapes are placed on or near the shape.</span></span> 
  
<span data-ttu-id="01f09-131">In Versionen vor Microsoft Visio 2000 wird dieses Verhalten in der Zelle ObjInterakt im Abschnitt Miscellaneous festgelegt.</span><span class="sxs-lookup"><span data-stu-id="01f09-131">In versions earlier than Visio 2000, you set this behavior using the ObjInteract cell in the Miscellaneous section.</span></span> 
  
<span data-ttu-id="01f09-132">Wenn Sie einen Verweis auf die Zelle Zelle ShapeFixedCode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="01f09-132">To get a reference to the ShapeFixedCode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f09-133">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="01f09-133">Cell name:</span></span>  <br/> |<span data-ttu-id="01f09-134">Zelle ShapeFixedCode</span><span class="sxs-lookup"><span data-stu-id="01f09-134">ShapeFixedCode</span></span>  <br/> |
   
<span data-ttu-id="01f09-135">Wenn Sie einen Verweis auf die Zelle Zelle ShapeFixedCode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="01f09-135">To get a reference to the ShapeFixedCode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="01f09-136">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="01f09-136">Section index:</span></span>  <br/> |<span data-ttu-id="01f09-137">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="01f09-137">**visSectionObject**</span></span> <br/> |
|<span data-ttu-id="01f09-138">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="01f09-138">Row index:</span></span>  <br/> |<span data-ttu-id="01f09-139">**visRowShapeLayout**</span><span class="sxs-lookup"><span data-stu-id="01f09-139">**visRowShapeLayout**</span></span> <br/> |
|<span data-ttu-id="01f09-140">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="01f09-140">Cell index:</span></span>  <br/> |<span data-ttu-id="01f09-141">**visSLOFixedCode**</span><span class="sxs-lookup"><span data-stu-id="01f09-141">**visSLOFixedCode**</span></span> <br/> |
   

