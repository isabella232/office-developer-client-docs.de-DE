---
title: Zelle "ReplaceLockText" (Abschnitt "Shape-Verhalten ändern")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 31f43ebe-3758-4fd9-83b5-775041c5890f
description: Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird. Die ReplaceLockText bestimmt, ob der Text, der im Master angezeigt wird, den Text der Form überschreibt, die ersetzt wird.
ms.openlocfilehash: 299bd571ad935886879abb11108c3d0bd28e3183
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348202"
---
# <a name="replacelocktext-cell-change-shape-behavior-section"></a><span data-ttu-id="b20e5-104">Zelle "ReplaceLockText" (Abschnitt "Shape-Verhalten ändern")</span><span class="sxs-lookup"><span data-stu-id="b20e5-104">ReplaceLockText Cell (Change Shape Behavior Section)</span></span>

<span data-ttu-id="b20e5-105">Gibt an, ob die Werte der angegebenen Zellen in einem Master-Shape die Werte (einschließlich lokaler Werte) einer Form überschreiben, die während einer Form Ersetzung ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b20e5-105">Indicates whether the values of specified cells in a master shape overwrite the values (including local values) of a shape being replaced during a shape replacement operation.</span></span> <span data-ttu-id="b20e5-106">Die **ReplaceLockText** bestimmt, ob der Text, der im Master angezeigt wird, den Text der Form überschreibt, die ersetzt wird.</span><span class="sxs-lookup"><span data-stu-id="b20e5-106">The **ReplaceLockText** determines whether the text displayed on the Master overwrites the text of the shape being replaced.</span></span> 
  
|<span data-ttu-id="b20e5-107">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b20e5-107">**Value**</span></span>|<span data-ttu-id="b20e5-108">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b20e5-108">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="b20e5-109">TRUE</span><span class="sxs-lookup"><span data-stu-id="b20e5-109">TRUE</span></span>  <br/> | <span data-ttu-id="b20e5-110">Der Text im Master-Shape überschreibt den Text auf dem alten Shape.</span><span class="sxs-lookup"><span data-stu-id="b20e5-110">The text on the master shape overwrites the text on the old shape.</span></span> <span data-ttu-id="b20e5-111">Außerdem überschreibt das Master-Shape die Werte der Zellen in den folgenden Abschnitten während eines Form Ersetzungsvorgangs:</span><span class="sxs-lookup"><span data-stu-id="b20e5-111">In addition, the master shape overwrites the values of the cells in the following sections during a shape replacement operation:</span></span>  <br/> <span data-ttu-id="b20e5-112">Abschnitt " **Text Fields** "</span><span class="sxs-lookup"><span data-stu-id="b20e5-112">**Text Fields** section</span></span>  <br/> <span data-ttu-id="b20e5-113">Abschnitt " **Text Block Format** "</span><span class="sxs-lookup"><span data-stu-id="b20e5-113">**Text Block Format** section</span></span>  <br/> |
|<span data-ttu-id="b20e5-114">FALSE</span><span class="sxs-lookup"><span data-stu-id="b20e5-114">FALSE</span></span>  <br/> |<span data-ttu-id="b20e5-115">Die Ersatzform enthält Text, Textfelder oder andere Texteigenschaften aus dem alten Shape, die dem Shape hinzugefügt wurden.</span><span class="sxs-lookup"><span data-stu-id="b20e5-115">The replacement shape contains any text, text fields, or other text properties from the old shape that have been added to the shape.</span></span>  <br/> <span data-ttu-id="b20e5-116">Wenn die Ersatzform Texteigenschaften aus dem alten Shape enthält, weist die Ersatzform auch die Werte aus den **Zeichen** -und **Absatz** Abschnitten der alten Form auf, wenn Sie mehr als eine Zeile aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b20e5-116">When the replacement shape contains text properties from the old shape, the replacement shape also has the values from the **Character** and **Paragraph** sections of the old shape if they have more than one row.</span></span>  <br/> |
   
<span data-ttu-id="b20e5-117">Bei Festlegung auf "TRUE" (1) werden durch die Werte des Shape-Masters die folgenden Werte für das zu ersetzende Shape ersetzt:</span><span class="sxs-lookup"><span data-stu-id="b20e5-117">If set to TRUE (1), the values of the shape Master replaces the values of the following on the shape being replaced:</span></span>
  
- [<span data-ttu-id="b20e5-118">Zelle "TheText" (Abschnitt "Events")</span><span class="sxs-lookup"><span data-stu-id="b20e5-118">TheText Cell (Events Section)</span></span>](thetext-cell-events-section.md)
    
- <span data-ttu-id="b20e5-119">Zellen im [Abschnitt "Character"](character-section.md)</span><span class="sxs-lookup"><span data-stu-id="b20e5-119">Cells in the [Character Section](character-section.md)</span></span>
    
- <span data-ttu-id="b20e5-120">Zellen im [Abschnitt "Paragraph"](paragraph-section.md)</span><span class="sxs-lookup"><span data-stu-id="b20e5-120">Cells in the [Paragraph Section](paragraph-section.md)</span></span>
    
- <span data-ttu-id="b20e5-121">Zellen im [Abschnitt "Tabs"](tabs-section.md)</span><span class="sxs-lookup"><span data-stu-id="b20e5-121">Cells in the [Tabs Section](tabs-section.md)</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b20e5-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b20e5-122">Remarks</span></span>

<span data-ttu-id="b20e5-123">Wenn Sie einen Verweis auf die Zelle **ReplaceLockText** aus einer anderen Formel, nach dem Wert des **N** -Attributs eines **Cell** -Elements oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b20e5-123">To get a reference to the **ReplaceLockText** cell by name from another formula, by value of the **N** attribute of a **Cell** element, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b20e5-124">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b20e5-124">Cell name:</span></span>  <br/> | <span data-ttu-id="b20e5-125">ReplaceLockText</span><span class="sxs-lookup"><span data-stu-id="b20e5-125">ReplaceLockText</span></span>  <br/> |
   
<span data-ttu-id="b20e5-126">Wenn Sie einen Verweis auf die Zelle **ReplaceLockText** aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b20e5-126">To get a reference to the **ReplaceLockText** cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b20e5-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b20e5-127">Section index:</span></span>  <br/> |<span data-ttu-id="b20e5-128">**Konstanten visSectionObject**</span><span class="sxs-lookup"><span data-stu-id="b20e5-128">**visSectionObject**</span></span> <br/> |
| <span data-ttu-id="b20e5-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b20e5-129">Row index:</span></span>  <br/> |<span data-ttu-id="b20e5-130">**visRowReplaceBehaviors**</span><span class="sxs-lookup"><span data-stu-id="b20e5-130">**visRowReplaceBehaviors**</span></span> <br/> |
| <span data-ttu-id="b20e5-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b20e5-131">Cell index:</span></span>  <br/> |<span data-ttu-id="b20e5-132">**visReplaceLockText**</span><span class="sxs-lookup"><span data-stu-id="b20e5-132">**visReplaceLockText**</span></span> <br/> |
   

