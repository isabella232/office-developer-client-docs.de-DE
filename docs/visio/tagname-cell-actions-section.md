---
title: Zelle "TagName" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60087
localization_priority: Normal
ms.assetid: e593e95d-f975-481d-69cd-619049d4427d
description: Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.
ms.openlocfilehash: e7bf5db940934d168ac2adb86d05b0374b0fd265
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412716"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="a59ba-103">Zelle "TagName" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="a59ba-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="a59ba-104">Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="a59ba-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="a59ba-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a59ba-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a59ba-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a59ba-106">Remarks</span></span>

<span data-ttu-id="a59ba-107">Über die Zellen TagName im Abschnitt Actions und im Abschnitt Action Tags erfolgt das Zuordnen eines Aktionstags zu den damit verknüpften Aktionen.</span><span class="sxs-lookup"><span data-stu-id="a59ba-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="a59ba-108">Wenn die Zelle TagName in einer Zeile Aktionen leer ist, wird die Aktion in einem Kontextmenü und nicht in einem aktionstagmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a59ba-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="a59ba-109">Wenn der Zellenwert TagName in der Zeile Actions mit dem Zellenwert TagName in einer Smarttag-Zeile übereinstimmt, wird die Aktion im Menü Aktionstag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a59ba-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="a59ba-110">Wenn die Zelle TagName einer Aktion einen Wert aufweist, aber nicht mit dem Wert TagName in einer beliebigen Shape-Tag-Zeile übereinstimmt, wird diese Aktion nicht in einem Aktionstag-oder Kontextmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a59ba-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="a59ba-111">Wenn mehrere Smarttag-Zeilen den gleichen Wert in der Zelle TagName aufweisen, wird überall die gleiche Aktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a59ba-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="a59ba-112">Wenn Sie einen Verweis auf die Zelle TagName aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a59ba-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a59ba-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a59ba-113">Cell name:</span></span>  <br/> |<span data-ttu-id="a59ba-114">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="a59ba-114">Actions.</span></span> <span data-ttu-id="a59ba-115">*Name* . Tagnamewobei-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="a59ba-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="a59ba-116">*Name* ist der Name der Zeile Actions.</span><span class="sxs-lookup"><span data-stu-id="a59ba-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a59ba-117">Wenn Sie einen Verweis auf die Zelle TagName aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a59ba-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a59ba-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a59ba-118">Section index:</span></span>  <br/> |<span data-ttu-id="a59ba-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a59ba-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a59ba-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a59ba-120">Row index:</span></span>  <br/> |<span data-ttu-id="a59ba-121">**visRowAction** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a59ba-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a59ba-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a59ba-122">Cell index:</span></span>  <br/> |<span data-ttu-id="a59ba-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="a59ba-123">**visActionTagName**</span></span> <br/> |
   

