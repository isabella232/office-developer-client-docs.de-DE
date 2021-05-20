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
ms.openlocfilehash: 867d36e27cb890509b0687500caf719362a711fb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439667"
---
# <a name="disabled-cell-action-tags-section"></a><span data-ttu-id="dcb5a-103">Zelle "Disabled" (Abschnitt "Action Tags")</span><span class="sxs-lookup"><span data-stu-id="dcb5a-103">Disabled Cell (Action Tags Section)</span></span>

<span data-ttu-id="dcb5a-104">Gibt an, ob das Aktionstag im Zeichnungsfenster angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-104">Indicates whether the action tag appears in the drawing window.</span></span>
  
> [!NOTE]
> <span data-ttu-id="dcb5a-105">In früheren Versionen von Microsoft Visio werden Aktionstags als Smarttags bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-105">In previous versions of Microsoft Visio, action tags are called smart tags.</span></span> 
  
|<span data-ttu-id="dcb5a-106">**Wert**</span><span class="sxs-lookup"><span data-stu-id="dcb5a-106">**Value**</span></span>|<span data-ttu-id="dcb5a-107">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dcb5a-107">**Description**</span></span>|
|:-----|:-----|
| <span data-ttu-id="dcb5a-108">TRUE</span><span class="sxs-lookup"><span data-stu-id="dcb5a-108">TRUE</span></span>  <br/> | <span data-ttu-id="dcb5a-109">Das Aktionstag ist deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-109">The action tag is disabled.</span></span>  <br/> |
| <span data-ttu-id="dcb5a-110">FALSE</span><span class="sxs-lookup"><span data-stu-id="dcb5a-110">FALSE</span></span>  <br/> | <span data-ttu-id="dcb5a-111">Das Aktionstag ist aktiviert (Standardeinstellung).</span><span class="sxs-lookup"><span data-stu-id="dcb5a-111">The action tag is enabled (the default).</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dcb5a-112">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dcb5a-112">Remarks</span></span>

<span data-ttu-id="dcb5a-113">Deaktivierte Aktionstags werden erst angezeigt, wenn sie wieder aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-113">When an action tag is disabled, it does not appear at all until it is re-enabled.</span></span> 
  
<span data-ttu-id="dcb5a-114">Verwenden Sie zum Erhalten eines Verweises auf die Zelle Disabled anhand des Namens aus einer anderen Formel oder aus einem Programm mithilfe der **CellsU-Eigenschaft:**</span><span class="sxs-lookup"><span data-stu-id="dcb5a-114">To get a reference to the Disabled cell by name from another formula, or from a program by using the **CellsU** property, use:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dcb5a-115">Zellenname:</span><span class="sxs-lookup"><span data-stu-id="dcb5a-115">Cell name:</span></span>  <br/> | <span data-ttu-id="dcb5a-116">SmartTags.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-116">SmartTags.</span></span>  <span data-ttu-id="dcb5a-117">*Name*  . Deaktiviert, wobei SmartTags.</span><span class="sxs-lookup"><span data-stu-id="dcb5a-117">*name*  .Disabled           where SmartTags.</span></span> <span data-ttu-id="dcb5a-118">*Name*  ist der Name der Aktionstagzeile</span><span class="sxs-lookup"><span data-stu-id="dcb5a-118">*name*  is the name of the action tag row</span></span>  <br/> |
   
<span data-ttu-id="dcb5a-119">Verwenden Sie die **CellsSRC-Eigenschaft** mit den folgenden Argumenten, um einen Verweis auf die Deaktivierte Zelle nach Index aus einem Programm zu erhalten:</span><span class="sxs-lookup"><span data-stu-id="dcb5a-119">To get a reference to the Disabled cell by index from a program, use the **CellsSRC** property with the following arguments:</span></span> 
  
|||
|:-----|:-----|
| <span data-ttu-id="dcb5a-120">Abschnittsindex:</span><span class="sxs-lookup"><span data-stu-id="dcb5a-120">Section index:</span></span>  <br/> |<span data-ttu-id="dcb5a-121">**visSectionSmartTag**</span><span class="sxs-lookup"><span data-stu-id="dcb5a-121">**visSectionSmartTag**</span></span> <br/> |
| <span data-ttu-id="dcb5a-122">Zeilenindex:</span><span class="sxs-lookup"><span data-stu-id="dcb5a-122">Row index:</span></span>  <br/> |<span data-ttu-id="dcb5a-123">**visRowSmartTag**  +   *i,* *wobei i* = 0, 1, 2...</span><span class="sxs-lookup"><span data-stu-id="dcb5a-123">**visRowSmartTag** +  *i*            where  *i*  = 0, 1, 2...</span></span>  <br/> |
| <span data-ttu-id="dcb5a-124">Zellenindex:</span><span class="sxs-lookup"><span data-stu-id="dcb5a-124">Cell index:</span></span>  <br/> |<span data-ttu-id="dcb5a-125">**visSmartTagDisabled**</span><span class="sxs-lookup"><span data-stu-id="dcb5a-125">**visSmartTagDisabled**</span></span> <br/> |
   

