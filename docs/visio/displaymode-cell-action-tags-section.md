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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332732"
---
# <a name="displaymode-cell-action-tags-section"></a><span data-ttu-id="61876-103">Wird Display Mode Cell (Action Tags section)</span><span class="sxs-lookup"><span data-stu-id="61876-103">DisplayMode Cell (Action Tags Section)</span></span>

<span data-ttu-id="61876-104">Bestimmt, ob das Aktionstag angezeigt wird, wenn der Benutzer den Mauszeiger über das Tag bewegt, wenn das Shape ausgewählt ist, oder die ganze Zeit.</span><span class="sxs-lookup"><span data-stu-id="61876-104">Determines whether the action tag appears when the user moves the pointer over the tag, when the shape is selected, or all the time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="61876-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="61876-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="61876-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="61876-106">**Value**</span></span>|<span data-ttu-id="61876-107">**Anzeigemodus**</span><span class="sxs-lookup"><span data-stu-id="61876-107">**Display Mode**</span></span>|<span data-ttu-id="61876-108">**Automatisierungskonstante**</span><span class="sxs-lookup"><span data-stu-id="61876-108">**Automation constant**</span></span>|
|:-----|:-----|:-----|
| <span data-ttu-id="61876-109">0</span><span class="sxs-lookup"><span data-stu-id="61876-109">0</span></span>  <br/> | <span data-ttu-id="61876-110">Wird angezeigt, wenn die Maus über dem Tag angehalten wird (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="61876-110">Appears when the mouse is paused over the tag (the default).</span></span>  <br/> |<span data-ttu-id="61876-111">**visSmartTagDispModeMouseOver**</span><span class="sxs-lookup"><span data-stu-id="61876-111">**visSmartTagDispModeMouseOver**</span></span> <br/> |
| <span data-ttu-id="61876-112">1</span><span class="sxs-lookup"><span data-stu-id="61876-112">1</span></span>  <br/> | <span data-ttu-id="61876-113">Wird angezeigt, wenn das Shape ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="61876-113">Appears while the shape is selected.</span></span>  <br/> |<span data-ttu-id="61876-114">**visSmartTagDispModeShapeSelected**</span><span class="sxs-lookup"><span data-stu-id="61876-114">**visSmartTagDispModeShapeSelected**</span></span> <br/> |
| <span data-ttu-id="61876-115">2</span><span class="sxs-lookup"><span data-stu-id="61876-115">2</span></span>  <br/> | <span data-ttu-id="61876-116">Wird immer angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61876-116">Appears all the time.</span></span>  <br/> |<span data-ttu-id="61876-117">**visSmartTagDispModeAlways**</span><span class="sxs-lookup"><span data-stu-id="61876-117">**visSmartTagDispModeAlways**</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="61876-118">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="61876-118">Remarks</span></span>

<span data-ttu-id="61876-119">Aktionstags werden nicht in gedruckten oder veröffentlichten Ausgaben angezeigt.</span><span class="sxs-lookup"><span data-stu-id="61876-119">Action tags do not appear on printed or published output.</span></span> 
  
<span data-ttu-id="61876-120">Wenn für ein Zeichenblatt ein Aktionstag definiert ist und die Zelle den Wert 1 aufweist, wird das Tag nie angezeigt, weil ein Zeichenblatt nicht ausgewählt werden kann.</span><span class="sxs-lookup"><span data-stu-id="61876-120">If an action tag is defined for a page, and this cell contains a value of 1, the tag never appears because a page cannot be selected.</span></span> 
  
<span data-ttu-id="61876-121">Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="61876-121">To get a reference to the DisplayMode cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61876-122">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="61876-122">Cell name:</span></span>  <br/> | <span data-ttu-id="61876-123">Smarttags.</span><span class="sxs-lookup"><span data-stu-id="61876-123">SmartTags.</span></span>  <span data-ttu-id="61876-124">*Name* . Wird Display Mode, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="61876-124">*name*  .DisplayMode           where SmartTags.</span></span> <span data-ttu-id="61876-125">*Name* ist der Name der Zeile mit dem Aktionstag.</span><span class="sxs-lookup"><span data-stu-id="61876-125">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="61876-126">Wenn Sie einen Verweis auf die Zelle wird Display Mode aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="61876-126">To get a reference to the DisplayMode cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="61876-127">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="61876-127">Section index:</span></span>  <br/> |<span data-ttu-id="61876-128">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="61876-128">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="61876-129">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="61876-129">Row index:</span></span>  <br/> |<span data-ttu-id="61876-130">**visRowSmartTag** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="61876-130">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="61876-131">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="61876-131">Cell index:</span></span>  <br/> |<span data-ttu-id="61876-132">**visSmartTagDisplayMode**</span><span class="sxs-lookup"><span data-stu-id="61876-132">**visSmartTagDisplayMode**</span></span> <br/> |
   

