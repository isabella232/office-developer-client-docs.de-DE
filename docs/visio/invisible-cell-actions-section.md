---
title: Zelle "Invisible" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60046
localization_priority: Normal
ms.assetid: 070b4468-c907-b201-1633-1d3e10ecc2b2
description: Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist.
ms.openlocfilehash: 69bc96e76f27a64d6e1443f045c27566f598c1db
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/23/2019
ms.locfileid: "32297242"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="a1fc8-103">Zelle "Invisible" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="a1fc8-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="a1fc8-104">Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a1fc8-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="a1fc8-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="a1fc8-106">**Value**</span></span>|<span data-ttu-id="a1fc8-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a1fc8-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a1fc8-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="a1fc8-108">TRUE</span></span>  <br/> |<span data-ttu-id="a1fc8-109">Die Aktion ist nicht im Menü sichtbar.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="a1fc8-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="a1fc8-110">FALSE</span></span>  <br/> |<span data-ttu-id="a1fc8-111">Die Aktion ist im Menü sichtbar (Standard).</span><span class="sxs-lookup"><span data-stu-id="a1fc8-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a1fc8-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a1fc8-112">Remarks</span></span>

<span data-ttu-id="a1fc8-113">Wenn Sie einen Verweis auf die Zelle inVisible aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a1fc8-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1fc8-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="a1fc8-114">Cell name:</span></span>  <br/> |<span data-ttu-id="a1fc8-115">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-115">Actions.</span></span> <span data-ttu-id="a1fc8-116">*Name* . Invisiblewobei-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="a1fc8-117">*Name* ist der Name der Zeile Actions.</span><span class="sxs-lookup"><span data-stu-id="a1fc8-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="a1fc8-118">Wenn Sie einen Verweis auf die unsichtbare Zelle aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="a1fc8-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1fc8-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="a1fc8-119">Section index:</span></span>  <br/> |<span data-ttu-id="a1fc8-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="a1fc8-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="a1fc8-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="a1fc8-121">Row index:</span></span>  <br/> |<span data-ttu-id="a1fc8-122">**visRowAction** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="a1fc8-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="a1fc8-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="a1fc8-123">Cell index:</span></span>  <br/> |<span data-ttu-id="a1fc8-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="a1fc8-124">**visActionInvisible**</span></span> <br/> |
   

