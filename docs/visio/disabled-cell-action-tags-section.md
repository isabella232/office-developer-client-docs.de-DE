---
title: Zelle "Disabled" (Abschnitt "Action Tags")
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- vis_sdr.chm60038
localization_priority: Normal
ms.assetid: bf0a80c9-0fdb-e2cf-3ab0-74cb6338fdce
description: Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.
ms.openlocfilehash: 409327365f3daf78dba20b1874be5911a517df0f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19796849"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="2c6d5-103">Disabled Cell (Action Tags Section)</span><span class="sxs-lookup"><span data-stu-id="2c6d5-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="2c6d5-104">Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="2c6d5-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="2c6d5-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="2c6d5-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="2c6d5-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="2c6d5-106">**Value**</span></span>|<span data-ttu-id="2c6d5-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="2c6d5-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="2c6d5-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="2c6d5-108">TRUE</span></span>  <br/> | <span data-ttu-id="2c6d5-109">Das Aktionstag ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="2c6d5-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="2c6d5-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="2c6d5-110">FALSE</span></span>  <br/> | <span data-ttu-id="2c6d5-111">Das Aktionstag ist aktiviert (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="2c6d5-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="2c6d5-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="2c6d5-112">Remarks</span></span>

<span data-ttu-id="2c6d5-113">Deaktivierte Aktionstags werden erst angezeigt, wenn sie wieder aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="2c6d5-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="2c6d5-114">Wenn Sie einen Verweis auf die Zelle Disabled aus einer anderen Formel oder aus einem Programm mithilfe der CellsU-Eigenschaft nach Namen erhalten möchten, verwenden Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="2c6d5-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c6d5-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="2c6d5-115">Cell name:</span></span>  <br/> | <span data-ttu-id="2c6d5-116">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="2c6d5-116">SmartTags.</span></span>  <span data-ttu-id="2c6d5-117">*Name* . Wobei deaktiviert SmartTags.</span><span class="sxs-lookup"><span data-stu-id="2c6d5-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="2c6d5-118">*Name* ist der Name der Zeile Aktionstag</span><span class="sxs-lookup"><span data-stu-id="2c6d5-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="2c6d5-119">Wenn Sie einen Verweis auf die Zelle Disabled aus einem Programm heraus nach Index erhalten möchten, verwenden Sie die CellsSRC-Eigenschaft mit folgenden Argumenten:</span><span class="sxs-lookup"><span data-stu-id="2c6d5-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="2c6d5-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="2c6d5-120">Section index:</span></span>  <br/> |<span data-ttu-id="2c6d5-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="2c6d5-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="2c6d5-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="2c6d5-122">Row index:</span></span>  <br/> |<span data-ttu-id="2c6d5-123">**VisRowSmartTag** +  *i* wobei *i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="2c6d5-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="2c6d5-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="2c6d5-124">Cell index:</span></span>  <br/> |<span data-ttu-id="2c6d5-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="2c6d5-125">**visSmartTagDisabled**</span></span> <br/> |
   

