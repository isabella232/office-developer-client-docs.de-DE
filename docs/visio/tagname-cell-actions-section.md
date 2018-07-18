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
ms.openlocfilehash: e1495a34769cbcfdd687491855d1f9c761de2b4e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798242"
---
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="84b5d-103">TagName Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="84b5d-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="84b5d-104">Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="84b5d-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="84b5d-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="84b5d-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="84b5d-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="84b5d-106">Remarks</span></span>

<span data-ttu-id="84b5d-107">Über die Zellen TagName im Abschnitt Actions und im Abschnitt Action Tags erfolgt das Zuordnen eines Aktionstags zu den damit verknüpften Aktionen.</span><span class="sxs-lookup"><span data-stu-id="84b5d-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="84b5d-108">Wenn in der Zeile Actions die Zelle TagName leer ist, wird die Aktion im Kontextmenü, nicht auf eine im Aktionstagmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84b5d-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="84b5d-109">Wenn ein Zellwert TagName in der Zeile Actions der Wert der TagName Zelle in einer Zeile Smart Tags entspricht, wird die Aktion auf im Aktionstagmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84b5d-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="84b5d-110">Zelle "TagName" eine Aktion verfügt über einen Wert, jedoch entspricht nicht den Wert in einer beliebigen Form-Tag-Zeile, wird diese Aktion nicht auf eine beliebige Aktionstag oder Kontextmenüs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84b5d-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="84b5d-111">Wenn mehrere Smarttag-Zeilen den gleichen Wert in der Zelle TagName aufweisen, wird überall die gleiche Aktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="84b5d-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="84b5d-112">Wenn Sie einen Verweis auf die Zelle TagName aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="84b5d-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84b5d-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="84b5d-113">Cell name:</span></span>  <br/> |<span data-ttu-id="84b5d-114">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="84b5d-114">Actions.</span></span> <span data-ttu-id="84b5d-115">*Name* . TagNamewhere Aktionen.</span><span class="sxs-lookup"><span data-stu-id="84b5d-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="84b5d-116">*Name* ist der Name der Zeile Actions</span><span class="sxs-lookup"><span data-stu-id="84b5d-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="84b5d-117">Wenn Sie einen Verweis auf die Zelle TagName aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="84b5d-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="84b5d-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="84b5d-118">Section index:</span></span>  <br/> |<span data-ttu-id="84b5d-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="84b5d-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="84b5d-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="84b5d-120">Row index:</span></span>  <br/> |<span data-ttu-id="84b5d-121">**VisRowAction** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="84b5d-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="84b5d-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="84b5d-122">Cell index:</span></span>  <br/> |<span data-ttu-id="84b5d-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="84b5d-123">**visActionTagName**</span></span> <br/> |
   

