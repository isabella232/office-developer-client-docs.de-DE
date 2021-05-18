---
title: Zelle ReplaceLockText (Abschnitt "Change Shape Behavior")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird. Der ReplaceLockText bestimmt, ob der im Master angezeigte Text den Text der zu ersetzenden Form überschreibt.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411918"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="2f483-104">Zelle ReplaceLockText (Abschnitt "Change Shape Behavior")</span><span class="sxs-lookup"><span data-stu-id="2f483-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="2f483-105">Gibt an, ob die Werte der angegebenen Zellen in einer Masterform die Werte (einschließlich lokaler Werte) eines Shapes überschreiben, das während eines Shapeersetzungsvorgangs ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="2f483-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="2f483-106">Der **ReplaceLockText** bestimmt, ob der im Master angezeigte Text den Text der zu ersetzenden Form überschreibt.</span><span class="sxs-lookup"><span data-stu-id="2f483-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="2f483-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2f483-107">**Value**</span></span>|<span data-ttu-id="2f483-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2f483-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="2f483-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="2f483-109">TRUE</span></span>  <br/> | <span data-ttu-id="2f483-110">Der Text auf der Masterform überschreibt den Text auf der alten Form.</span><span class="sxs-lookup"><span data-stu-id="2f483-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="2f483-111">Darüber hinaus überschreibt die Masterform während eines Shapeersetzungsvorgangs die Werte der Zellen in den folgenden Abschnitten:</span><span class="sxs-lookup"><span data-stu-id="2f483-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="2f483-112">**Abschnitt "Text Fields"**</span><span class="sxs-lookup"><span data-stu-id="2f483-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="2f483-113">**Abschnitt "Text Block Format"**</span><span class="sxs-lookup"><span data-stu-id="2f483-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="2f483-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="2f483-114">FALSE</span></span>  <br/> |<span data-ttu-id="2f483-115">Die Ersetzungsform enthält beliebige Text-, Textfeld- oder andere Texteigenschaften aus der alten Form, die der Form hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="2f483-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="2f483-116">Wenn die Ersetzungsform Texteigenschaften aus der alten Form enthält, enthält die Ersetzungsform auch die Werte aus den Abschnitten **Character** und **Paragraph** der alten Form, wenn sie mehr als eine Zeile enthalten.</span><span class="sxs-lookup"><span data-stu-id="2f483-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="2f483-117">Wenn true (1) festgelegt ist, werden durch die Werte des ShapeMasters die folgenden Werte für die ersetzte Form ersetzt:</span><span class="sxs-lookup"><span data-stu-id="2f483-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="2f483-118">Zelle "TheText" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="2f483-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="2f483-119">Zellen im [Abschnitt "Character"](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f483-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="2f483-120">Zellen im [Abschnitt Absatz](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f483-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="2f483-121">Zellen im [Abschnitt Registerkarten](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="2f483-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2f483-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2f483-122">Remarks</span></span>

<span data-ttu-id="2f483-123">Um einen Verweis auf die **Zelle ReplaceLockText** anhand des Namens aus einer anderen Formel, nach dem Wert des **N-Attributs** eines **Cell-Elements** oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="2f483-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f483-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2f483-124">Cell name:</span></span>  <br/> | <span data-ttu-id="2f483-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="2f483-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="2f483-126">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die **Zelle ReplaceLockText** nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="2f483-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2f483-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2f483-127">Section index:</span></span>  <br/> |<span data-ttu-id="2f483-128">**visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="2f483-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="2f483-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2f483-129">Row index:</span></span>  <br/> |<span data-ttu-id="2f483-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="2f483-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="2f483-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2f483-131">Cell index:</span></span>  <br/> |<span data-ttu-id="2f483-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="2f483-132">**visReplaceLockText**</span></span> <br/> |
   

