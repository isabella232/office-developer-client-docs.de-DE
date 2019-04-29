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
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="642be-105">Zelle "DynFeedback" (Abschnitt "Miscellaneous")</span><span class="sxs-lookup"><span data-stu-id="642be-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="642be-p102">Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.</span><span class="sxs-lookup"><span data-stu-id="642be-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="642be-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="642be-109">**Value**</span></span>|<span data-ttu-id="642be-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="642be-110">**Description**</span></span>|<span data-ttu-id="642be-111">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="642be-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="642be-112">0</span><span class="sxs-lookup"><span data-stu-id="642be-112">0</span></span>  <br/> | <span data-ttu-id="642be-113">Bleibt gerade (keine Abschnitte).</span><span class="sxs-lookup"><span data-stu-id="642be-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="642be-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="642be-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="642be-115">1</span><span class="sxs-lookup"><span data-stu-id="642be-115">1</span></span>  <br/> | <span data-ttu-id="642be-116">Zeigt beim Ziehen drei Abschnitte an.</span><span class="sxs-lookup"><span data-stu-id="642be-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="642be-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="642be-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="642be-118">2</span><span class="sxs-lookup"><span data-stu-id="642be-118">2</span></span>  <br/> | <span data-ttu-id="642be-119">Zeigt beim Ziehen fünf Abschnitte an.</span><span class="sxs-lookup"><span data-stu-id="642be-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="642be-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="642be-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="642be-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="642be-121">Remarks</span></span>

<span data-ttu-id="642be-122">Wenn Sie einen Verweis auf die Zelle Zelle DynFeedback aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="642be-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="642be-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="642be-123">Cell name:</span></span>  <br/> | <span data-ttu-id="642be-124">Zelle DynFeedback</span><span class="sxs-lookup"><span data-stu-id="642be-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="642be-125">Wenn Sie einen Verweis auf die Zelle Zelle DynFeedback aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="642be-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="642be-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="642be-126">Section index:</span></span>  <br/> |<span data-ttu-id="642be-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="642be-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="642be-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="642be-128">Row index:</span></span>  <br/> |<span data-ttu-id="642be-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="642be-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="642be-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="642be-130">Cell index:</span></span>  <br/> |<span data-ttu-id="642be-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="642be-131">**visDynFeedback**</span></span> <br/> |
   

