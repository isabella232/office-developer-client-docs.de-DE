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
ms.openlocfilehash: f45f22001a4d7275bb9367414c8b04ea3c0d9c6e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434235"
---
# <a name="readonly-cell-actions-section"></a><span data-ttu-id="9c4cb-103">Zelle "ReadOnly" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="9c4cb-103">ReadOnly Cell (Actions Section)</span></span>

<span data-ttu-id="9c4cb-104">Steuert, ob die Aktion in einem Aktionstag- oder Kontextmenü schreibgeschützt ist.</span><span class="sxs-lookup"><span data-stu-id="9c4cb-104">Controls whether the action on an action tag or shortcut menu is read-only.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="9c4cb-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="9c4cb-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="9c4cb-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="9c4cb-106">**Value**</span></span>|<span data-ttu-id="9c4cb-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9c4cb-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9c4cb-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="9c4cb-108">TRUE</span></span>  <br/> |<span data-ttu-id="9c4cb-109">Die Aktion wird im Menü angezeigt, ist aber schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="9c4cb-109">The action appears on the menu but is read-only.</span></span>  <br/> |
|<span data-ttu-id="9c4cb-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="9c4cb-110">FALSE</span></span>  <br/> |<span data-ttu-id="9c4cb-111">Die Aktion wird im Menü angezeigt und kann ausgewählt werden (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="9c4cb-111">The action appears on the menu and can be selected (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9c4cb-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c4cb-112">Remarks</span></span>

<span data-ttu-id="9c4cb-113">Wenn eine Aktion schreibgeschützt ist, wird sie im Aktionstag- oder Kontextmenü angezeigt, kann jedoch nicht ausgewählt werden.</span><span class="sxs-lookup"><span data-stu-id="9c4cb-113">When an action is read-only, it appears on the action tag or shortcut menu but you cannot select it.</span></span> <span data-ttu-id="9c4cb-114">Sie ist nicht grau unterlegt, wird aber wie eine Beschriftung vor einem farbigen Hintergrund angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9c4cb-114">It is not dimmed but rather appears on a colored background, like a label.</span></span> <span data-ttu-id="9c4cb-115">Wenn Sie das Menüelement grau unterlegt anzeigen lassen möchten, verwenden Sie die Zelle Disabled.</span><span class="sxs-lookup"><span data-stu-id="9c4cb-115">To make the menu item appear dimmed, use the Disabled cell.</span></span> 
  
<span data-ttu-id="9c4cb-116">Verwenden Sie zum Erhalten eines Verweises auf die Zelle ReadOnly anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="9c4cb-116">To get a reference to the ReadOnly cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c4cb-117">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="9c4cb-117">Cell name:</span></span>  <br/> |<span data-ttu-id="9c4cb-118">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="9c4cb-118">Actions.</span></span> <span data-ttu-id="9c4cb-119">*Name*  . ReadOnlywhere-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="9c4cb-119">*name*  .ReadOnlywhere Actions.</span></span>  <span data-ttu-id="9c4cb-120">*Name*  ist der Name der Zeile Aktionen</span><span class="sxs-lookup"><span data-stu-id="9c4cb-120">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="9c4cb-121">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle ReadOnly nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="9c4cb-121">To get a reference to the ReadOnly cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9c4cb-122">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="9c4cb-122">Section index:</span></span>  <br/> |<span data-ttu-id="9c4cb-123">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="9c4cb-123">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="9c4cb-124">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="9c4cb-124">Row index:</span></span>  <br/> |<span data-ttu-id="9c4cb-125">**visRowAction**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="9c4cb-125">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="9c4cb-126">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="9c4cb-126">Cell index:</span></span>  <br/> |<span data-ttu-id="9c4cb-127">**visActionReadOnly**</span><span class="sxs-lookup"><span data-stu-id="9c4cb-127">**visActionReadOnly**</span></span> <br/> |
   

