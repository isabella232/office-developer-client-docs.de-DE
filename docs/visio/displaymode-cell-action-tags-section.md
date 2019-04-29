---
title: Wird Display Mode Cell (Action Tags section)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60039
localization_priority: Normal
ms.assetid: 0dfad40b-f97e-0c4a-2102-7344d1317b82
description: Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist, oder die ganze Zeit.
ms.openlocfilehash: 0254ad361c63dfdeddaf8a1c2173e99aa1c05398
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415817"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="b965e-103">Wird Display Mode Cell (Action Tags section)</span><span class="sxs-lookup"><span data-stu-id="b965e-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="b965e-104">Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist, oder die ganze Zeit.</span><span class="sxs-lookup"><span data-stu-id="b965e-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b965e-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b965e-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="b965e-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="b965e-106">**Value**</span></span>|<span data-ttu-id="b965e-107">**Anzeigemodus**</span><span class="sxs-lookup"><span data-stu-id="b965e-107">**Display Mode**</span></span>|<span data-ttu-id="b965e-108">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="b965e-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="b965e-109">0</span><span class="sxs-lookup"><span data-stu-id="b965e-109">0</span></span>  <br/> | <span data-ttu-id="b965e-110">Wird angezeigt, wenn die Maus über dem Tag angehalten wird (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="b965e-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="b965e-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="b965e-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="b965e-112">1</span><span class="sxs-lookup"><span data-stu-id="b965e-112">1</span></span>  <br/> | <span data-ttu-id="b965e-113">Wird angezeigt, wenn das Shape ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="b965e-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="b965e-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="b965e-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="b965e-115">2</span><span class="sxs-lookup"><span data-stu-id="b965e-115">2</span></span>  <br/> | <span data-ttu-id="b965e-116">Wird immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b965e-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="b965e-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="b965e-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b965e-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="b965e-118">Remarks</span></span>

<span data-ttu-id="b965e-119">Aktionstags werden nicht in gedruckten oder veröffentlichten Ausgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="b965e-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="b965e-120">Wenn für ein Zeichenblatt ein Aktionstag definiert ist und die Zelle den Wert 1 aufweist, wird das Tag nie angezeigt, weil ein Zeichenblatt nicht ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="b965e-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="b965e-121">Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="b965e-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b965e-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="b965e-122">Cell name:</span></span>  <br/> | <span data-ttu-id="b965e-123">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="b965e-123">SmartTags.</span></span>  <span data-ttu-id="b965e-124">*Name* . Wird Display Mode, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="b965e-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="b965e-125">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="b965e-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="b965e-126">Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="b965e-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="b965e-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="b965e-127">Section index:</span></span>  <br/> |<span data-ttu-id="b965e-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="b965e-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="b965e-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="b965e-129">Row index:</span></span>  <br/> |<span data-ttu-id="b965e-130">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="b965e-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="b965e-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="b965e-131">Cell index:</span></span>  <br/> |<span data-ttu-id="b965e-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="b965e-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

