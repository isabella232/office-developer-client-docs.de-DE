---
title: Zelle "SortKey" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm1027286
localization_priority: Normal
ms.assetid: c0c4b668-f31b-336f-4434-e94a4804ff7c
description: Eine Zahl, mit der die Reihenfolge von Aktionen bestimmt wird, die in einem Kontext- oder Aktionstagmenü angezeigt werden.
ms.openlocfilehash: 5a5db1276d1f2544b5b2b76301c30a2bedd4be63
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19798185"
---
# <a name="sortkey-cell-actions-section"></a><span data-ttu-id="e1267-103">SortKey Cell (Actions Section)</span><span class="sxs-lookup"><span data-stu-id="e1267-103">SortKey Cell (Actions Section)</span></span>

<span data-ttu-id="e1267-104">Eine Zahl, mit der die Reihenfolge von Aktionen bestimmt wird, die in einem Kontext- oder Aktionstagmenü angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="e1267-104">A number that determines the order of actions that appear on a shortcut or action tag menu.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e1267-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="e1267-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="e1267-106">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e1267-106">Remarks</span></span>

<span data-ttu-id="e1267-p101">Die Aktionen in einem Aktionstag- oder Kontextmenü werden im Menü mit der niedrigsten Nummer ganz oben in aufsteigender Reihenfolge angezeigt. Wenn zwei Aktionszeilen den gleichen Wert in der Zelle SortKey aufweisen, wird die Reihenfolge durch die Reihenfolge der Zeilen bestimmt. Der Standardwert ist 0.</span><span class="sxs-lookup"><span data-stu-id="e1267-p101">The actions on an action tag or shortcut menu appear on the menu sorted from lowest to highest, with lower numbers appearing at the top of the menu. If two action rows have the same SortKey cell value, the order is determined by physical row order. The default is 0 (zero).</span></span>
  
<span data-ttu-id="e1267-110">Wenn Sie einen Verweis auf die Zelle SortKey aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="e1267-110">To get a reference to the SortKey cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1267-111">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="e1267-111">Cell name:</span></span>  <br/> |<span data-ttu-id="e1267-112">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="e1267-112">Actions.</span></span> <span data-ttu-id="e1267-113">*Name* . SortKeywhere Aktionen.</span><span class="sxs-lookup"><span data-stu-id="e1267-113">*name*  .SortKeywhere Actions.</span></span>  <span data-ttu-id="e1267-114">*Name* ist der Name der Zeile Actions</span><span class="sxs-lookup"><span data-stu-id="e1267-114">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="e1267-115">Wenn Sie einen Verweis auf die Zelle SortKey aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="e1267-115">To get a reference to the SortKey cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e1267-116">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="e1267-116">Section index:</span></span>  <br/> |<span data-ttu-id="e1267-117">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="e1267-117">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="e1267-118">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="e1267-118">Row index:</span></span>  <br/> |<span data-ttu-id="e1267-119">**VisRowAction** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="e1267-119">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="e1267-120">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="e1267-120">Cell index:</span></span>  <br/> |<span data-ttu-id="e1267-121">**visActionSortKey**</span><span class="sxs-lookup"><span data-stu-id="e1267-121">**visActionSortKey**</span></span> <br/> |
   

