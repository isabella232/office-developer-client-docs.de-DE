---
title: Zelle "Disabled" (Abschnitt "Actions")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- Vis_DSS.chm82251337
localization_priority: Normal
ms.assetid: ebf66729-d794-a398-268a-84d761bf06b6
description: Gibt an, ob ein Element in einem Kontext- oder Aktionstagmenü deaktiviert ist.
ms.openlocfilehash: ddf55f40056d7df7a2403e500bb4bae335930433
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431351"
---
# <a name="disabled-cell-actions-section"></a><span data-ttu-id="45563-103">Zelle "Disabled" (Abschnitt "Actions")</span><span class="sxs-lookup"><span data-stu-id="45563-103">Disabled Cell (Actions Section)</span></span>

<span data-ttu-id="45563-104">Gibt an, ob ein Element in einem Kontext- oder Aktionstagmenü deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="45563-104">Indicates whether an item on a shortcut or action tag menu is disabled.</span></span>
  
> [!NOTE]
> <span data-ttu-id="45563-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="45563-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="45563-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="45563-106">**Value**</span></span>|<span data-ttu-id="45563-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="45563-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="45563-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="45563-108">TRUE</span></span>  <br/> |<span data-ttu-id="45563-109">Befehlsnamen deaktivieren (abblenden).</span><span class="sxs-lookup"><span data-stu-id="45563-109">Disable (dim) command name.</span></span>  <br/> |
|<span data-ttu-id="45563-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="45563-110">FALSE</span></span>  <br/> |<span data-ttu-id="45563-111">Befehlsnamen aktivieren (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="45563-111">Enable the command name (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="45563-112">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="45563-112">Remarks</span></span>

<span data-ttu-id="45563-113">Wenn Sie einen Verweis auf die Zelle disabled aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU** -Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="45563-113">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45563-114">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="45563-114">Cell name:</span></span>  <br/> |<span data-ttu-id="45563-115">Aktionen.</span><span class="sxs-lookup"><span data-stu-id="45563-115">Actions.</span></span> <span data-ttu-id="45563-116">*Name* . Deaktiviert, wenn Aktionen.</span><span class="sxs-lookup"><span data-stu-id="45563-116">*name*  .Disabled           where Actions.</span></span> <span data-ttu-id="45563-117">*Name* ist der Name der Zeile Actions.</span><span class="sxs-lookup"><span data-stu-id="45563-117">*name*  is the name of the Actions row</span></span>  <br/> |
   
<span data-ttu-id="45563-118">Wenn Sie einen Verweis auf die Zelle disabled aus einem Programm nach Index erhalten möchten, verwenden Sie die **CellsSRC** -Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="45563-118">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="45563-119">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="45563-119">Section index:</span></span>  <br/> |<span data-ttu-id="45563-120">**visSectionAction**</span><span class="sxs-lookup"><span data-stu-id="45563-120">**visSectionAction**</span></span> <br/> |
|<span data-ttu-id="45563-121">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="45563-121">Row index:</span></span>  <br/> |<span data-ttu-id="45563-122">**visRowAction** +  *i* , wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="45563-122">**visRowAction** +  *i*           where  *i*  = 0, 1, 2...</span></span>  <br/> |
|<span data-ttu-id="45563-123">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="45563-123">Cell index:</span></span>  <br/> |<span data-ttu-id="45563-124">**visActionDisabled**</span><span class="sxs-lookup"><span data-stu-id="45563-124">**visActionDisabled**</span></span> <br/> |
   

