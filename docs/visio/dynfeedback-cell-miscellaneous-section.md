---
title: Zelle "DynFeedback" (Abschnitt "Miscellaneous")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251317
localization_priority: Normal
ms.assetid: 44017319-7146-3431-e476-fbb1a40341ca
description: Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.
ms.openlocfilehash: 823b8db4dc6afe94a5fdac1f62aaa48d7e1b0d80
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404799"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="c7281-105">Zelle "DynFeedback" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="c7281-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="c7281-p102">Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.</span><span class="sxs-lookup"><span data-stu-id="c7281-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="c7281-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="c7281-109">**Value**</span></span>|<span data-ttu-id="c7281-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c7281-110">**Description**</span></span>|<span data-ttu-id="c7281-111">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="c7281-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="c7281-112">0</span><span class="sxs-lookup"><span data-stu-id="c7281-112">0</span></span>  <br/> | <span data-ttu-id="c7281-113">Bleibt gerade (keine Abschnitte).</span><span class="sxs-lookup"><span data-stu-id="c7281-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="c7281-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="c7281-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="c7281-115">1</span><span class="sxs-lookup"><span data-stu-id="c7281-115">1</span></span>  <br/> | <span data-ttu-id="c7281-116">Zeigt beim Ziehen drei Abschnitte an.</span><span class="sxs-lookup"><span data-stu-id="c7281-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="c7281-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="c7281-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="c7281-118">2</span><span class="sxs-lookup"><span data-stu-id="c7281-118">2</span></span>  <br/> | <span data-ttu-id="c7281-119">Zeigt beim Ziehen fünf Abschnitte an.</span><span class="sxs-lookup"><span data-stu-id="c7281-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="c7281-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="c7281-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c7281-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c7281-121">Remarks</span></span>

<span data-ttu-id="c7281-122">Verwenden Sie zum Erhalten eines Verweises auf die DynFeedback-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="c7281-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7281-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="c7281-123">Cell name:</span></span>  <br/> | <span data-ttu-id="c7281-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="c7281-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="c7281-125">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die DynFeedback-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="c7281-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="c7281-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="c7281-126">Section index:</span></span>  <br/> |<span data-ttu-id="c7281-127">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="c7281-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="c7281-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="c7281-128">Row index:</span></span>  <br/> |<span data-ttu-id="c7281-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="c7281-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="c7281-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="c7281-130">Cell index:</span></span>  <br/> |<span data-ttu-id="c7281-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="c7281-131">**visDynFeedback**</span></span> <br/> |
   

