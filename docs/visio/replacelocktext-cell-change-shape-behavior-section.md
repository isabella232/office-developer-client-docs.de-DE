---
title: ReplaceLockText Cell (Change Shape Behavior Section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben. Die ReplaceLockText bestimmt, ob die Textanzeige auf das Master-Shape den Text der Form, die ersetzt werden überschrieben.
ms.openlocfilehash: 75fb0831e7361345f04d7912eb0a55959d9417cd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797858"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="b886d-104">ReplaceLockText Cell (Change Shape Behavior Section)</span><span class="sxs-lookup"><span data-stu-id="b886d-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="b886d-105">Gibt an, ob die Werte der angegebenen Zellen in einem master-Shape die Werte (einschließlich lokale Werte) eines Shapes, die ersetzt werden, während ein Shape Ersetzungsvorgang überschreiben.</span><span class="sxs-lookup"><span data-stu-id="b886d-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="b886d-106">Die **ReplaceLockText** bestimmt, ob die Textanzeige auf das Master-Shape den Text der Form, die ersetzt werden überschrieben.</span><span class="sxs-lookup"><span data-stu-id="b886d-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="b886d-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b886d-107">**Value**</span></span>|<span data-ttu-id="b886d-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b886d-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b886d-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="b886d-109">TRUE</span></span>  <br/> | <span data-ttu-id="b886d-110">Der Text auf das master-Shape überschreibt den Text auf dem alten Shape.</span><span class="sxs-lookup"><span data-stu-id="b886d-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="b886d-111">Darüber hinaus überschreibt das master-Shape der Werte von Zellen in den folgenden Abschnitten während einer Ersetzungsoperation Form:</span><span class="sxs-lookup"><span data-stu-id="b886d-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="b886d-112">Abschnitt " **Text Fields** "</span><span class="sxs-lookup"><span data-stu-id="b886d-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="b886d-113">Abschnitt " **Text Block Format** "</span><span class="sxs-lookup"><span data-stu-id="b886d-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="b886d-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="b886d-114">FALSE</span></span>  <br/> |<span data-ttu-id="b886d-115">Ersatz-Shapes enthält Text, Textfelder oder andere Texteigenschaften von der alten Form, die mit dem Shape hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b886d-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="b886d-116">Ersatz-Shapes Eigenschaften von der alten Form Text enthält, besitzt Ersatz-Shapes auch Werte in den Abschnitten **Zeichen-** und **Absatzformaten** der alten Form, wenn sie mehr als eine Zeile verfügen.</span><span class="sxs-lookup"><span data-stu-id="b886d-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="b886d-117">Wenn auf TRUE (1), die Werte des Master-Shapes die Werte der folgenden auf die zu ersetzende Form ersetzt:</span><span class="sxs-lookup"><span data-stu-id="b886d-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="b886d-118">Zelle "TheText" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="b886d-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="b886d-119">Zellen im [Abschnitt "Character"](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="b886d-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="b886d-120">Zellen im [Abschnitt "Paragraph"](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="b886d-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="b886d-121">Zellen im [Abschnitt "Tabs"](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="b886d-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b886d-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b886d-122">Remarks</span></span>

<span data-ttu-id="b886d-123">Wenn Sie einen Verweis auf die Zelle **ReplaceLockText** nach Namen aus, als Wert des Attributs **N** **ein Zellenelement** , einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b886d-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b886d-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b886d-124">Cell name:</span></span>  <br/> | <span data-ttu-id="b886d-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="b886d-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="b886d-126">Wenn Sie einen Verweis auf die Zelle **ReplaceLockText** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b886d-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b886d-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b886d-127">Section index:</span></span>  <br/> |<span data-ttu-id="b886d-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b886d-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b886d-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b886d-129">Row index:</span></span>  <br/> |<span data-ttu-id="b886d-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="b886d-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="b886d-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b886d-131">Cell index:</span></span>  <br/> |<span data-ttu-id="b886d-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="b886d-132">**visReplaceLockText**</span></span> <br/> |
   

