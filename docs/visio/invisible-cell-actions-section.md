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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423874"
---
# <a name="invisible-cell-actions-section"></a><span data-ttu-id="7da73-103">Zelle "Invisible" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="7da73-103">Invisible Cell (Actions Section)</span></span>

<span data-ttu-id="7da73-104">Zeigt an, ob die Aktion im Aktionstag- oder Kontextmenü sichtbar ist.</span><span class="sxs-lookup"><span data-stu-id="7da73-104">Indicates whether the action is visible on the action tag or shortcut menu.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="7da73-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="7da73-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="7da73-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="7da73-106">**Value**</span></span>|<span data-ttu-id="7da73-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7da73-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7da73-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="7da73-108">TRUE</span></span>  <br/> |<span data-ttu-id="7da73-109">Die Aktion ist nicht im Menü sichtbar.</span><span class="sxs-lookup"><span data-stu-id="7da73-109">The action is not visible on the menu.</span></span>  <br/> |
|<span data-ttu-id="7da73-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="7da73-110">FALSE</span></span>  <br/> |<span data-ttu-id="7da73-111">Die Aktion ist im Menü sichtbar (Standard).</span><span class="sxs-lookup"><span data-stu-id="7da73-111">The action is visible on the menu (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7da73-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7da73-112">Remarks</span></span>

<span data-ttu-id="7da73-113">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Invisible anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="7da73-113">To get a reference to the Invisible cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7da73-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="7da73-114">Cell name:</span></span>  <br/> |<span data-ttu-id="7da73-115">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="7da73-115">Actions.</span></span> <span data-ttu-id="7da73-116">*Name*  . Invisiblewhere-Aktionen.</span><span class="sxs-lookup"><span data-stu-id="7da73-116">*name*  .Invisiblewhere Actions.</span></span>  <span data-ttu-id="7da73-117">*Name*  ist der Name der Zeile Aktionen</span><span class="sxs-lookup"><span data-stu-id="7da73-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="7da73-118">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Zelle Invisible nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="7da73-118">To get a reference to the Invisible cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="7da73-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="7da73-119">Section index:</span></span>  <br/> |<span data-ttu-id="7da73-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="7da73-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="7da73-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="7da73-121">Row index:</span></span>  <br/> |<span data-ttu-id="7da73-122">**visRowAction**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="7da73-122">**visRowAction** +  *i*  where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="7da73-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="7da73-123">Cell index:</span></span>  <br/> |<span data-ttu-id="7da73-124">**visActionInvisible**</span><span class="sxs-lookup"><span data-stu-id="7da73-124">**visActionInvisible**</span></span> <br/> |
   

