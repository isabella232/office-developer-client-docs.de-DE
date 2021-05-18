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
# <a name="tagname-cell-actions-section"></a><span data-ttu-id="45316-103">Zelle "TagName" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="45316-103">TagName Cell (Actions Section)</span></span>

<span data-ttu-id="45316-104">Enthält den Namen des Aktionstags, mit dem diese Aktion verknüpft ist.</span><span class="sxs-lookup"><span data-stu-id="45316-104">Contains the name of the action tag that this action is associated with.</span></span>
  
> [!NOTE]
> <span data-ttu-id="45316-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="45316-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="45316-106">Hinweise</span><span class="sxs-lookup"><span data-stu-id="45316-106">Remarks</span></span>

<span data-ttu-id="45316-107">Über die Zellen TagName im Abschnitt Actions und im Abschnitt Action Tags erfolgt das Zuordnen eines Aktionstags zu den damit verknüpften Aktionen.</span><span class="sxs-lookup"><span data-stu-id="45316-107">The TagName cell in the Actions section works together with the TagName cell in the Action Tags section to associate an action tag with its actions.</span></span> 
  
- <span data-ttu-id="45316-108">Wenn die Zelle TagName in einer Actions-Zeile leer ist, wird die Aktion in einem Kontextmenü und nicht in einem Aktionstagmenü angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45316-108">If the TagName cell in an Actions row is blank, the action appears on a shortcut menu, not on an action tag menu.</span></span>
    
- <span data-ttu-id="45316-109">Wenn ein TagName-Zellwert in der Zeile Aktionen mit dem TagName-Zellwert in einer SmartTags-Zeile entspricht, wird die Aktion im Menü Aktionstag angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45316-109">If a TagName cell value in the Actions row matches the TagName cell value in a Smart Tags row, the action appears on the action tag menu.</span></span>
    
- <span data-ttu-id="45316-110">Wenn die TagName-Zelle einer Aktion über einen Wert verfügt, sie jedoch nicht mit dem TagName-Wert in einer Shape-Tag-Zeile übereinstimmen, wird diese Aktion nicht in Aktionstagmenüs oder Kontextmenüs angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45316-110">If an action's TagName cell has a value but it does not match the TagName value in any shape tag row, that action does not appear on any action tag menus or shortcut menus.</span></span>
    
- <span data-ttu-id="45316-111">Wenn mehrere Smarttag-Zeilen den gleichen Wert in der Zelle TagName aufweisen, wird überall die gleiche Aktion angezeigt.</span><span class="sxs-lookup"><span data-stu-id="45316-111">If several smart tag rows have the same TagName value, they will all show the same actions.</span></span>
    
<span data-ttu-id="45316-112">Um einen Verweis auf die TagName-Zelle anhand des Namens aus einer anderen Formel oder aus einem Programm mit der **CellsU-Eigenschaft** zu erhalten, verwenden Sie:</span><span class="sxs-lookup"><span data-stu-id="45316-112">To get a reference to the TagName cell by name from another formula, or from a program using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45316-113">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="45316-113">Cell name:</span></span>  <br/> |<span data-ttu-id="45316-114">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="45316-114">Actions.</span></span> <span data-ttu-id="45316-115">*Name*  . TagNamewhere-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="45316-115">*name*  .TagNamewhere Actions.</span></span>  <span data-ttu-id="45316-116">*Name*  ist der Name der Zeile Aktionen</span><span class="sxs-lookup"><span data-stu-id="45316-116">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="45316-117">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die TagName-Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="45316-117">To get a reference to the TagName cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45316-118">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="45316-118">Section index:</span></span>  <br/> |<span data-ttu-id="45316-119">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="45316-119">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="45316-120">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="45316-120">Row index:</span></span>  <br/> |<span data-ttu-id="45316-121">**visRowAction**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="45316-121">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="45316-122">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="45316-122">Cell index:</span></span>  <br/> |<span data-ttu-id="45316-123">**visActionTagName**</span><span class="sxs-lookup"><span data-stu-id="45316-123">**visActionTagName**</span></span> <br/> |
   

