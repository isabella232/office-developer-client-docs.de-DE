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
ms.openlocfilehash: 858d98c8ee55eb49f58bbe98491ddc8752e75504
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796921"
---
# <a name="dynfeedback-cell-miscellaneous-section"></a><span data-ttu-id="4d4f3-105">DynFeedback Cell (Miscellaneous Section)</span><span class="sxs-lookup"><span data-stu-id="4d4f3-105">DynFeedback Cell (Miscellaneous Section)</span></span>

<span data-ttu-id="4d4f3-p102">Ändert die Art des visuellen Feedbacks, das Benutzern angezeigt wird, wenn sie einen Verbinder mit der Maus verschieben. Wenn die Maustaste losgelassen wird, ist das daraus resultierende Verbinder-Shape von dieser Einstellung nicht betroffen. Diese Einstellung gilt nicht für umleitbare Verbinder.</span><span class="sxs-lookup"><span data-stu-id="4d4f3-p102">Changes the type of visual feedback provided to users when they drag a connector. When the mouse button is released, the resulting connector shape is not affected by this setting. This setting does not apply to routable connectors.</span></span>
  
|<span data-ttu-id="4d4f3-109">**Wert**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-109">**Value**</span></span>|<span data-ttu-id="4d4f3-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-110">**Description**</span></span>|<span data-ttu-id="4d4f3-111">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-111">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="4d4f3-112">0</span><span class="sxs-lookup"><span data-stu-id="4d4f3-112">0</span></span>  <br/> | <span data-ttu-id="4d4f3-113">Bleibt gerade (keine Abschnitte).</span><span class="sxs-lookup"><span data-stu-id="4d4f3-113">Remains straight (no legs).</span></span>  <br/> |<span data-ttu-id="4d4f3-114">**visDynFBDefault**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-114">**visDynFBDefault**</span></span> <br/> |
| <span data-ttu-id="4d4f3-115">1</span><span class="sxs-lookup"><span data-stu-id="4d4f3-115">1</span></span>  <br/> | <span data-ttu-id="4d4f3-116">Zeigt beim Ziehen drei Abschnitte an.</span><span class="sxs-lookup"><span data-stu-id="4d4f3-116">Shows three legs when dragged.</span></span>  <br/> |<span data-ttu-id="4d4f3-117">**visDynFBUCon3Leg**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-117">**visDynFBUCon3Leg**</span></span> <br/> |
| <span data-ttu-id="4d4f3-118">2</span><span class="sxs-lookup"><span data-stu-id="4d4f3-118">2</span></span>  <br/> | <span data-ttu-id="4d4f3-119">Zeigt beim Ziehen fünf Abschnitte an.</span><span class="sxs-lookup"><span data-stu-id="4d4f3-119">Shows five legs when dragged.</span></span>  <br/> |<span data-ttu-id="4d4f3-120">**visDynFBUCon5Leg**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-120">**visDynFBUCon5Leg**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d4f3-121">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4d4f3-121">Remarks</span></span>

<span data-ttu-id="4d4f3-122">Wenn Sie einen Verweis auf die Zelle DynFeedback aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="4d4f3-122">To get a reference to the DynFeedback cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d4f3-123">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="4d4f3-123">Cell name:</span></span>  <br/> | <span data-ttu-id="4d4f3-124">DynFeedback</span><span class="sxs-lookup"><span data-stu-id="4d4f3-124">DynFeedback</span></span>  <br/> |
   
<span data-ttu-id="4d4f3-125">Wenn Sie einen Verweis auf die Zelle DynFeedback aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="4d4f3-125">To get a reference to the DynFeedback cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="4d4f3-126">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="4d4f3-126">Section index:</span></span>  <br/> |<span data-ttu-id="4d4f3-127">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-127">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="4d4f3-128">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="4d4f3-128">Row index:</span></span>  <br/> |<span data-ttu-id="4d4f3-129">**visRowMisc**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-129">**visRowMisc**</span></span> <br/> |
| <span data-ttu-id="4d4f3-130">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="4d4f3-130">Cell index:</span></span>  <br/> |<span data-ttu-id="4d4f3-131">**visDynFeedback**</span><span class="sxs-lookup"><span data-stu-id="4d4f3-131">**visDynFeedback**</span></span> <br/> |
   

