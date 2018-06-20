---
title: Zelle "ReadOnly" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm60071
localization_priority: Normal
ms.assetid: 158b4188-570c-3817-bf34-8dc0c64befa5
description: Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist.
ms.openlocfilehash: bf2d0f7e50a3126611662af8e068485986c26a13
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19797768"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="7103a-103">Zelle "ReadOnly" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="7103a-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="7103a-104">Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="7103a-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7103a-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7103a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="7103a-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7103a-106">**Value**</span></span>|<span data-ttu-id="7103a-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7103a-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7103a-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="7103a-108">TRUE</span></span>  <br/> |<span data-ttu-id="7103a-109">Die Aktion wird im Menü angezeigt, ist aber schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="7103a-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="7103a-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="7103a-110">FALSE</span></span>  <br/> |<span data-ttu-id="7103a-111">Die Aktion wird im Menü angezeigt und kann ausgewählt werden (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="7103a-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7103a-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="7103a-112">Remarks</span></span>

<span data-ttu-id="7103a-113">Wenn eine Aktion schreibgeschützt ist, wird auf das Aktionsmenü Aktionstag- oder Kontextmenü angezeigt, aber nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="7103a-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="7103a-114">Es ist nicht abgeblendet, aber vielmehr auf einem farbigen Hintergrund, wie eine Beschriftung angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7103a-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="7103a-115">Damit das Menüelement abgeblendet angezeigt wird, verwenden Sie die Zelle Disabled aus.</span><span class="sxs-lookup"><span data-stu-id="7103a-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="7103a-116">Zum Abrufen eines Verweises auf die Zelle ReadOnly nach Namen aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="7103a-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7103a-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7103a-117">Cell name:</span></span>  <br/> |<span data-ttu-id="7103a-118">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="7103a-118">Actions.</span></span> <span data-ttu-id="7103a-119">*Name* . ReadOnlywhere Aktionen.</span><span class="sxs-lookup"><span data-stu-id="7103a-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="7103a-120">*Name* ist der Name der Zeile Actions</span><span class="sxs-lookup"><span data-stu-id="7103a-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="7103a-121">Wenn Sie einen Verweis auf die Zelle ReadOnly aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="7103a-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7103a-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7103a-122">Section index:</span></span>  <br/> |<span data-ttu-id="7103a-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="7103a-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="7103a-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7103a-124">Row index:</span></span>  <br/> |<span data-ttu-id="7103a-125">**VisRowAction** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7103a-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7103a-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7103a-126">Cell index:</span></span>  <br/> |<span data-ttu-id="7103a-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="7103a-127">**visActionReadOnly**</span></span> <br/> |
   

